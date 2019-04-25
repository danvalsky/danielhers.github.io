# Content Differences in Syntactic and Semantic Representations

This page provides detailed examples to accompany the following <a href="../divergences.pdf">paper</a>:

    @InProceedings{hershcovich2019content,
      author    = {Hershcovich, Daniel  and  Abend, Omri  and  Rappoport, Ari},
      title     = {Content Differences in Syntactic and Semantic Representations},
      booktitle = {Proc. of NAACL},
      year      = {2019}
    }

Content will be available soon.

~~~ conllu
# I wrote the letter with a quill.
1   Я         ja         PRON   _   Case=Nom|Number=Sing|Person=1|PronType=Prs        2   nsubj   _   I
2   написал   napisat'   VERB   _   Gender=Masc|Number=Sing|VerbForm=Part|Voice=Act   0   root    _   wrote
3   письмо    pis'mo     NOUN   _   Case=Acc|Gender=Neut|Number=Sing                  2   obj     _   the-letter
4   пером     pero       NOUN   _   Case=Ins|Gender=Neut|Number=Sing                  2   nmod    _   with-a-quill
~~~