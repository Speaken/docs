
|Endpoint|Description|
|--------|-----------|
|[POST /lemmas](#create-lemma)| Create a new lemma|

## POST /lemmas

Create a new lemma and automatically add the lemma to all activity_type (with due_date=J+1 and revision_count=0) for the current user


### Parameters

|Name|Required|Type|Description|
|----|--------|----|-----------|
|```lemma[:lemma]```|required|string|value of the lemma|
|```lemma[:phonetic]```|required|string|Phonetic of the lemma|
|```lemma[:pronunciation_uk_url]```|required|string|Url of the UK pronunciation|
|```lemma[:pronunciation_us_url]```|required|string|Url of the US pronunciation|
|```lemma[:qa_meanings_attributes][:definition]```|required|array|Definition of the word|
|```lemma[:qa_meanings_attributes][:k_list]```|required|string|k_list of the word|
|```lemma[:qa_meanings_attributes][:level]```|required|enum|level of the word. Can be beginner, elementary, intermediate, fluent, advanced, native|
|```lemma[:qa_meanings_attributes][:part_of_speech]```|required|enum|Part_of_speech of the word. Can be adj, adp, adv, aux, conj, cconj, det, intj, noun, num, part, pron, propn, punct, sconj, sym, verb, x, space|
|```lemma[:qa_meanings_attributes][:entity]```|required|enum|Entity of the word. Can be person, norp, fac, org, gpe, loc, product, event, work_of_art, law, language, date, time, percent, money, quantity, ordinal, cardinal|

### Example Request

```curl -X POST https://api.speaken.com/api/v1/qa/lemmas```



