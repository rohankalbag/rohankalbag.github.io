---
layout: post
title: Implementation of Stop-and-Wait Algorithm
---

[Click for more details about project](https://github.com/rohankalbag/stop-and-wait-algorithm)

*This project involved the development of a UDP-based Stop-and-Wait algorithm for reliable data transfer. The sender created UDP sockets for communication with the receiver. It meticulously managed packet transmission and retransmission based on acknowledgments from the receiver, ensuring data integrity. The code featured a sophisticated timeout mechanism, utilizing the `select()` function for precise timeout management. This approach enabled the sender to monitor responses and handle packet loss scenarios effectively. On the receiver side, the system continuously listened for incoming packets. It introduced a probabilistic packet drop simulation mechanism, where packets were randomly dropped based on a user-defined probability, enabling the examination of the protocol's robustness in the face of potential data loss. The receiver meticulously tracked the sequence numbers of incoming packets, allowing it to acknowledge correctly received packets and request retransmissions when necessary. This project delved into the intricacies of network communication, demonstrating the implementation of a reliable communication protocol with advanced timeout handling and packet loss simulation.*