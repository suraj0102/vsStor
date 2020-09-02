# vsStor

Analyst firm Markets and Markets reports the video surveillance market was valued at $30.37 billion in 2016 and is estimated that it will hit $75.64 billion by 2022, at a compound annual growth rate of 15.4% between 2017 and 2022. As data continues to grow at a fast rate, 
the needs for changes in the design of video surveillance storage systems are growing. Therefore, there are practical needs to set up a video storage system to satisfy those needs.
This project presents vsStor, a large-scale video surveillance storage system which is used for receiving and storing thousands of concurrent video streams.
It allows users to use erasure coding to adjust data redundancy levels. vsStor is a not traditional (i.e. POSIX-compliant) filesystem, therefore, 
it’s not designed to provide normal file services for existing and legacy applications.
Instead, vsStor runs on traditional filesystems (e.g. ext4, xfs), so it is easier to implement and less error-prone.
At this stage, vsStor is content agnostic: it does not analyze the content of the video, all streams are treated as binary data. 
The main contributions of this project are:
1) Design and implement a video storage system which is able to handle thousands of video streams concurrently.
2) A network based data striping strategy to achieve high throughput and high reliability.
3) Storage of metadata in database and on disks allows the system to scale to PB-level which is crucial in Big Data environment.
Characteristics of Video Storage Systems:
Frequent write (append only), seldom read
Storage requirement predictable
Near real time playback
Reliability and Availability
