---
layout: base
title:  'Content Differences in Syntactic and Semantic Representations'
---

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
# sent_id = reviews-305187-0005
# text = Wine was excellent.
1       Wine    wine    NOUN    NN      Number=Sing     3       nsubj   3:nsubj _
2       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   3       cop     3:cop   _
3       excellent       excellent       ADJ     JJ      Degree=Pos      0       root    0:root  SpaceAfter=No
4       .       .       PUNCT   .       _       3       punct   3:punct _
~~~

~~~ conllu
# sent_id = reviews-079007-0002
# text = But service is very poor.
1       But     but     CCONJ   CC      _       5       cc      5:cc    _
2       service service NOUN    NN      Number=Sing     5       nsubj   5:nsubj _
3       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   5       cop     5:cop   _
4       very    very    ADV     RB      _       5       advmod  5:advmod        _
5       poor    poor    ADJ     JJ      Degree=Pos      0       root    0:root  SpaceAfter=No
6       .       .       PUNCT   .       _       5       punct   5:punct _
~~~