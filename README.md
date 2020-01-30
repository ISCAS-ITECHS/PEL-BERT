# PEL-BERT
PEL-BERT: A Joint Model for Protocol Entity Linking
## Abstract    
Internet protocol analysis is an advanced computer networking topic that uses a packet analyzer to capture, view, and understand Internet protocols. Due to the long period, not uniform format, and strong domain-specific of the RFC document context, it is a challenging issue to identify and link the field entities in RFC document protocol using the current methods. The pre-trained models, such as BERT, are widely used in NLP tasks and are fine-tuned to improve the performance of various natural language processing tasks consistently. Nevertheless, the fine-tuned BERT model trained on our protocol corpus still has a weak performance on the entity linking mission. In this paper, we propose a model that joints a fine-tuned language model with an RFC Domain Model to link named entities in the protocols to categories in the protocol knowledge base. Firstly, we design a protocol knowledge base as the schema for protocol entity linking. Secondly, we use the heuristic methods to identify the protocol entities and infer the descriptions from the nearby contexts of its header field using the Zero-Shot Learning method. Finally, we conduct comprehensive experiments on the RFC dataset by using our joint model and baseline methods to make protocol entity linking. Experimental results demonstrate that our model achieves state-of-the-art performance in entity linking on our annotated dataset, outperforming all the baselines. Besides, we release a data set of entity linking in the field of computer networks, RFC-EL-2020, which provides help for researchers to fine-grained analyze and utilize protocols.    

![image](https://github.com/ISCAS-ITECHS/PEL-BERT/blob/master/data/example.png)  

![image](https://github.com/ISCAS-ITECHS/PEL-BERT/blob/master/data/overview.png)  

![image](https://github.com/ISCAS-ITECHS/PEL-BERT/blob/master/data/model.png)  



