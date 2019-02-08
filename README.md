# fake-video-corpus
This is the first, to our knowledge, annotated dataset of debunked and verified user-generated videos (UGVs), along with multiple near-duplicate reposted versions of them. For details refer to [Fake Video Corpus](https://mklab.iti.gr/results/fake-video-corpus/).

The dataset comprises videos from a variety of event categories, such as politics, sports, natural disasters, accidents, wars, etc. Currently, it consists of 200 unique debunked videos (for simplicity also referred to as fake) and 180 unique verified videos (also referred to as real). In particular, different types of fake video are included:

- Staged videos where actors perform scripted actions under direction.
- Videos where contextual information is false (e.g. the claimed video location is wrong).
- Past videos presented as UGV from breaking events.
- Videos of which the visual or audio content has been altered through editing.
- Computer-generated Imagery (CGI) posing as real.

The dataset was extended following a largely automatic systematic process that combines text search and near-duplicate video retrieval, followed by manual annotation using a set of guidelines. More specifically:

1. For each video in the original set, the video title was used as input.
2. The title was reformulated to a more general form (called the “event title”). For example, a video with title “Video Tornado IRMA en Florida EEUU Video impactante” was assigned to event “Tornado IRMA at Florida”.
3. The event title was translated from English into four major languages: Russian, Arabic, French, and German using Google Translate. These languages were selected after preliminary tests indicated that near-duplicate videos appear with increased frequency in these languages.
4. The video title, event title, and the four translations were used as separate queries to the three target platforms: YouTube, Facebook, Twitter. All returned videos were aggregated in a common pool.
5. A near-duplicate retrieval algorithm was used to search within this pool for near-duplicates of the video.
6. After manual inspection, erroneous results were removed and only actual near-duplicates were retained.

**The overall dataset consist of 3957 videos annotated as fake and 2458 annotated as real.**

| Categories for near-duplicates of fake videos include | Categories for near-duplicates of real videos include |
| ------------- |:-------------:| 
|Fake: those that reproduce the same false claims | Real: those that reproduce the same factual claims|
|Uncertain: those that express doubts on the veracity of the claim | Uncertain: those that express doubts on the veracity of the claim|
|Debunk: those that attempt to debunk the original claim | Debunk: those that attempt to debunk their claims as false|
|Parody: those that use the content for fun/entertainment | Parody: those that use the content for fun/entertainment|
|Real: those that contain the earlier, original source from which the fake was made| |

Facebook videos that were relevant to the dataset but were published by individual users (and thus could not be accessed through the API) were excluded from this dataset.

**Dataset**

The initial 200 fake and 180 real videos are contained in FVC.csv.

The near duplicates are contained in FVC_dup.csv.

The text queries for retrieving the near duplicates are contained in FVC_text_queries.csv.

**License and acknowledgement**

The video dataset is provided under the Attribution-NonCommercial-ShareAlike 4.0 International [(CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/).

The video dataset is supported by the [InVID project](https://www.invid-project.eu/), which is funded by the European Commission under contract number 687786.

If you use this video dataset for your research, please include a citation to the following paper: Papadopoulou, O., Zampoglou, M., Papadopoulos, S., & Kompatsiaris, Y. (2018). [A Corpus of Debunked and Verified User-Generated Videos](https://mklab.iti.gr/results/fake-video-corpus/OIR.pdf). Online Information Review. Accepted for publication.

    @article{papadopoulou2018corpus,
      author = "Papadopoulou, Olga and Zampoglou, Markos and Papadopoulos, Symeon and Kompatsiaris, Ioannis",
      title = "A corpus of debunked and verified user-generated videos",
      journal = "Online Information Review",
      doi = "10.1108/OIR-03-2018-0101",
      year={2018},
      publisher={Emerald Publishing Limited}
    }


If you encounter any issues in this process, please get in touch with Olga Papadopoulou <olgapapa@iti.gr>.
