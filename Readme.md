# WNUT 2020: Named Entity Extraction 


WNUT 2020 shared task is designed on the wet lab protocol data. All of the protocols were collected from [protocols.io](https://www.protocols.io/) using their public APIs. The full protocol-dump is also available as json format in their [github repository](https://github.com/protocolsio/protocols). For this shared task, we provide the annotation of 615 protocols. The brat styled annotated protocols can be visulalized in: http://bit.ly/WNUT2020



## Data

Wet Lab Protocol (WLP) dataset is reuses the 623 protocols from [Kulkarni et al.](https://cocoxu.github.io/publications/NAACL_2018_wet_lab_protocols.pdf). We removed 8 duplicate protocols from the collection and re annotated all the 615 uniqe protocols in brat. The re-annotation task added the missing entity-relations and also corrected the incosistencies. The updated dataset is provided in the [data directory](./data/Readme.md) in both StandOff and CoNLL format. The data is divided in 3 sub-directories as below:

1) [train_data](./data/train_data/): 370 protocols with 8436 sentences
2) [dev_data](./data/dev_data/): 122 protocols  with 2838 sentences
3) [test_data](./data/test_data/): 123 protocols  with 2813 sentences

## Baselines

We have provided a feature based [Linear CRF tagger](./code/baseline_CRF/) for the Named Entity Recognition Task.


## Evaluation

The participants are required to produce predictions on the protocols as [StandOff format](../../data/Readme.md##-The-standoff-format:), which will be compared with the gold data using the [evalution script](./code/eval/).


## RELEVANT PAPERS 

 Paper about the dataset:
   
	@inproceedings{kulkarni2018wetlab,
	  author     = {Kulkarni, Chaitanya and Xu, Wei and Ritter, Alan and Machiraju, Raghu},
	  title      = {An Annotated Corpus for Machine Reading of Instructions in Wet Lab Protocols},
	  booktitle = {Proceedings of the 2018 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (NAACL)},
	  year       = {2018}
	} 

  