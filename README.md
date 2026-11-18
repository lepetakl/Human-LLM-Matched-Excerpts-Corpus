# Human-LLM-Matched-Excerpts-Corpus
A collection of English literary excerpts containing 298 human-authored texts and four corresponding sets of LLM-generated texts, produced by models from OpenAI, Google, Mistral, and Anthropic.

The human-authored corpus was derived from the English collection of the [refcor repository](https://github.com/cophi-wue/refcor).

## Dataset overview

| Corpus | Excerpts |
| --- | ---: |
| Human | 298 |
| GPT-6 Sol | 298 |
| Gemini 3.1 Pro | 298 |
| Mistral Large 4 | 298 |
| Claude Sonnet 5.5 | 298 |
| **Total**| **1,490** |

The corpora were designed to be comparable in **number of excerpts, approximate length, literary genre, and topic**. Each excerpt contains approximately **1,500 tokens** (although, actual lengths may vary).

### LLM-generated corpora

For each sampled human excerpt, three topic words were extracted using **TF-IDF**, excluding function words, pronouns, proper nouns, and named entities.

#### Prompt used

```text
Write an original excerpt of English literary prose.
The style should be consistent with a novel published between 1838-1921.
The excerpt should revolve around the following general themes: {themes}.
Length requirement: {target_length} words.
Maintain coherent paragraph structure and continuous prose.
Do not quote, paraphrase, or imitate any specific existing work.
Do not use specific character names from known literary works.
```

#### Generation settings

Generation settings were matched as closely as each providers' controls allowed, with temperature set to **1** and **disabled reasoning** (with an exception of Gemini, for which the setting was set to low).
