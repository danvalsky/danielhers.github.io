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

## Scene/Non-Scene
### Participant nsubj:
UD:
~~~ conllu
# sent_id = reviews-305187-0005
# text = Wine was excellent.
1       Wine    wine    NOUN    NN      Number=Sing     3       nsubj   _ _
2       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   3       cop     _   _
3       excellent       excellent       ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
4       .       .       PUNCT   .       _       3       punct   _ _
~~~

UCCA:
~~~ ann
Wine was excellent .
T2	ParallelScene 0 20	Wine was excellent .
T4	Participant 0 4	Wine
T5	Function 5 8	was
T6	State 9 18	excellent
~~~

### Process nsubj:
UD:
~~~ conllu
# sent_id = reviews-079007-0002
# text = But service is very poor.
1       But     but     CCONJ   CC      _       5       cc      _    _
2       service service NOUN    NN      Number=Sing     5       nsubj   _ _
3       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   5       cop     _   _
4       very    very    ADV     RB      _       5       advmod  _        _
5       poor    poor    ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
6       .       .       PUNCT   .       _       5       punct   _ _
~~~

UCCA:
~~~ ann
But service is very poor .
T2	Linker 0 3	But
T3	ParallelScene 4 26	service is very poor .
T6	Process 4 11	service
T7	Function 12 14	is
T8	Adverbial 15 26	very poor .
T9	Elaborator 15 19	very
T10	Center 20 24	poor
~~~


## General

UCCA:
~~~ ann
After graduation , Mary moved to New York City .
T2	Linker 0 5	After
T3	ParallelScene 6 16	graduation
T4	Process 6 16	graduation
T6	ParallelScene 19 46	Mary moved to New York City
T7	Participant 19 23	Mary
R1	Participant parent:T3 child:T7
T8	Process 24 29	moved
T9	Participant 30 46	to New York City
T10	Relator 30 32	to
T11	Center 33 46	New York City
~~~