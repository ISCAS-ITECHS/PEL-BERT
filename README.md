# PEL-BERT
PEL-BERT: A Joint Model for Protocol Entity Linking
## Abstract    
Internet protocol analysis is an advanced computer networking topic that uses a packet analyzer to capture, view, and understand Internet protocols. Due to the long period, not uniform format, and strong domain-specific of the RFC document context, it is a challenging issue to identify and link the field entities in RFC document protocol using the current methods. The pre-trained models, such as BERT, are widely used in NLP tasks and are fine-tuned to improve the performance of various natural language processing tasks consistently. Nevertheless, the fine-tuned BERT model trained on our protocol corpus still has a weak performance on the entity linking mission. In this paper, we propose a model that joints a fine-tuned language model with an RFC Domain Model to link named entities in the protocols to categories in the protocol knowledge base. Firstly, we design a protocol knowledge base as the schema for protocol entity linking. Secondly, we use the heuristic methods to identify the protocol entities and infer the descriptions from the nearby contexts of its header field using the Zero-Shot Learning method. Finally, we conduct comprehensive experiments on the RFC dataset by using our joint model and baseline methods to make protocol entity linking. Experimental results demonstrate that our model achieves state-of-the-art performance in entity linking on our annotated dataset, outperforming all the baselines. Besides, we release a data set of entity linking in the field of computer networks, RFC-EL-2020, which provides help for researchers to fine-grained analyze and utilize protocols.    

![image](https://github.com/ISCAS-ITECHS/PEL-BERT/blob/master/data/example.png)  

![image](https://github.com/ISCAS-ITECHS/PEL-BERT/blob/master/data/overview.png)  

![image](https://github.com/ISCAS-ITECHS/PEL-BERT/blob/master/data/model.png)  

## RFC-EL-2020 dataset 
file is RFC-EL-2020_v1.0.tsv,format is tsv.  

|  rfc-no   | Header-Field | Description-Text | Class |
|  ----     | ----         |----              |----   |
|760|	Version|	The Version field indicates the format of the internet header . This document describes version 4 .|	220|
760	IHL	Internet Header Length is the length of the internet header in 32 bit words , and thus points to the beginning of the data . Note that the minimum value for a correct header is 5 .	100
760	Type of Service	The Type of Service provides an indication of the abstract parameters of the quality of service desired . These parameters are to be used to guide the selection of the actual service parameters when transmitting a datagram through a particular network . Several networks offer service precedence , which somehow treats high precedence traffic as more important than other traffic . A few networks offer a Stream service , whereby one can achieve a smoother service at some cost . Typically this involves the reservation of resources within the network . Another choice involves a low-delay vs . high-reliability trade off . Typically networks invoke more complex ( and delay producing ) mechanisms as the need for reliability increases . 	240
760	Total Length	Total Length is the length of the datagram , measured in octets , including internet header and data . This field allows the length of a datagram to be up to 65,535 octets . Such long datagrams are impractical for most hosts and networks . All hosts must be prepared to accept datagrams of up to 576 octets ( whether they arrive whole	100
760	Identification	An identifying value assigned by the sender to aid in assembling the fragments of a datagram . 	400
760	Flags	Flags : 3 bits	231
760	Fragment Offset	This field indicates where in the datagram this fragment belongs . The fragment offset is measured in units of 8 octets ( 64 bits ). The first fragment has offset zero .	110
760	Time to Live	This field indicates the maximum time the datagram is allowed to remain the internet system . If this field contains the value zero , then the datagram should be destroyed . This field is modified in internet header processing . The time is measured in units of seconds . The intention is to cause undeliverable datagrams to be discarded . 	122
760	Protocol	This field indicates the next level protocol used in the data portion of the internet datagram . The values for various protocols are specified in reference [ 6 ].	231
760	Header Checksum	A checksum on the header only . Since some header fields may change ( e.g ., time to live ), this is recomputed and verified at each point that the internet header is processed . 	301
760	Source Address	The source address . The first octet is the Source Network , and the following three octets are the Source Local Address . 	230
760	Destination Address	The destination address . The first octet is the Destination Network , and the following three octets are the Destination Local Address . 	230
760	Options	The option field is variable in length . There may be zero or more options . There are two cases for the format of an option : 	400
760	Version	Version : Same as the datagram in error . IHL : As computed . Type of Service : Zero . Total Length : As computed . Identification : A new identification is selected . Flags : Zero . Fragment Offset : Zero . Time to Live : Sixty . Protocol : Same as the datagram in error . Header Checksum : As computed . Source Address : Address of the error reporting module . Destination Address : Source address of the datagram in error . Options : The General Error Report Option . Padding : As needed . 	110


