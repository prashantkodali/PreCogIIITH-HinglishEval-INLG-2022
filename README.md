# code-mix-quality-shared-task


## ToDos

	- Adding new Features
		- [ ] Sentence Length
		- [ ] Feature Vectors distance - monolingual and code-mix sentence
		- [ ] XLM-R, mBERT Perplexity scores - [MLM-scoring Repo](https://github.com/kanishkamisra/minicons)
		- [ ] Syntactic Features of monolingual sentences - tree heights, num of nodes. 
		- [ ] Semantic Features Vectors distance - monolingual and code-mix sentence
	
	- Continuted pre-training on code-mix data

## Features and File Structure

	- Notebooks
		- feature-computation.ipynb : code for generating all features listed below
		- modelling.ipyng : code for simple Linear Regression , MLPRegressor

	- Dataset folder 
		- contians the orgingial files shared by organisers
		- jsons for dataframe with all features. trandf.json, valdf.json . use pd.read_json
		- Features
		
			- Read from dataset files shared by organisers
				- 'English' : English sentence,
				- 'Hindi' : Hindi sentence, 
				- 'Hinglish', 
				- 'Average rating',
				- 'Disagreement', 
				- 'hum_gen' - list of hum generated code-mix samples for correspoding English and Hindi sentence, 

			- features computed by us
				- 'Hinglish_csnliop' - [CSNLI](https://github.com/devanshg27/csnli) output for Hinglish sentence, 
				- 'hum_gen_csnliop' - same as above , but for hum_gen column. list of list,
				- 'Hinglish_norm' - extracted from csnli output. list of normalised tokens. , 
				- 'Hinglish_lid' - extracted from csnli output. list of LID - en, hi, univ, ne, acro, 
				- 'hum_gen_norm' - , 
				- 'hum_gen_lid',
				- 'Hinglish_pos' - output of pos tagger - [Model](https://huggingface.co/prakod/en-hi-pos-tagger-symcom), 
				- 'hum_gen_pos', 
				- 'Hinglish_cmi_scores' - CMI scores,
				- 'Hinglish_burstiness_scores' - burstiness scores, 
				- 'Hinglish_sp_scores' - switching points scores, 
				- 'symcom_scores_pos' - SyMCoM Scores - all PoS tags. dictionary ,
				- 'symcom_scores_sent' - SyMCoM for sentence, 
				- 'NOUN_symcom' - extracted from symcom_scores_pos dictionary, 
				- 'AUX_symcom', 
				- 'CCONJ_symcom',
				- 'ADP_symcom', 
				- 'NUM_symcom', 
				- 'PRON_symcom', 
				- 'PART_symcom', 
				- 'VERB_symcom',
				- 'PROPN_symcom', 
				- 'SCONJ_symcom', 
				- 'ADV_symcom', 
				- 'INTJ_symcom',
				- 'DET_symcom', 
				- 'ADJ_symcom', 
				- 'symcom_+1_count' - num of postags with score +1, 
				- 'symcom_-1_count' - num of postags with score -1,
				- 'symcom_na_count' - num of postags with NaN score,
				- 'symcom_others' - num of postags with score between -1 and +1



	
