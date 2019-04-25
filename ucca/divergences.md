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

The full content will be available soon.

## Scene/Non-Scene
### Participant nsubj:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-305187-0005
# text = Wine was excellent.
1       Wine    wine    NOUN    NN      Number=Sing     3       nsubj   _ _
2       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   3       cop     _   _
3       excellent       excellent       ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
4       .       .       PUNCT   .       _       3       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Wine was excellent .
T2	ParallelScene 0 20	Wine was excellent .
T4	Participant 0 4	Wine
T5	Function 5 8	was
T6	State 9 18	excellent
</div>
</td></tr></tbody>
</table>

### Process nsubj:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-079007-0002
# text = But service is very poor.
1       But     but     CCONJ   CC      _       5       cc      _    _
2       service service NOUN    NN      Number=Sing     5       nsubj   _ _
3       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   5       cop     _   _
4       very    very    ADV     RB      _       5       advmod  _        _
5       poor    poor    ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
6       .       .       PUNCT   .       _       5       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
But service is very poor .
T2	Linker 0 3	But
T3	ParallelScene 4 26	service is very poor .
T6	Process 4 11	service
T7	Function 12 14	is
T8	Adverbial 15 26	very poor .
T9	Elaborator 15 19	very
T10	Center 20 24	poor
</div>
</td></tr></tbody>
</table>

### Linker nsubj:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-295491-0007
# text = Overall, Joe is a happy camper who has found a great spot.
1       Overall overall ADV     RB      _       7       advmod  7:advmod        SpaceAfter=No
2       ,       ,       PUNCT   ,       _       7       punct   7:punct _
3       Joe     Joe     PROPN   NNP     Number=Sing     7       nsubj   7:nsubj _
4       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   7       cop     7:cop   _
5       a       a       DET     DT      Definite=Ind|PronType=Art       7       det     7:det   _
6       happy   happy   ADJ     JJ      Degree=Pos      7       amod    7:amod  _
7       camper  camper  NOUN    NN      Number=Sing     0       root    10:nsubj        _
8       who     who     PRON    WP      PronType=Rel    10      nsubj   7:ref   _
9       has     have    AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   10      aux     10:aux  _
10      found   find    VERB    VBN     Tense=Past|VerbForm=Part        7       acl:relcl       7:acl:relcl     _
11      a       a       DET     DT      Definite=Ind|PronType=Art       13      det     13:det  _
12      great   great   ADJ     JJ      Degree=Pos      13      amod    13:amod _
13      spot    spot    NOUN    NN      Number=Sing     10      obj     10:obj  SpaceAfter=No
14      .       .       PUNCT   .       _       7       punct   7:punct _
</div>
</td><td width="600">
Overall , Joe is a happy camper who has found a great spot .
T2	Linker 0 7	Overall
T3	ParallelScene 10 31	Joe is a happy camper
T4	Linker 32 35	who
T5	ParallelScene 36 60	has found a great spot .
T7	Function 36 39	has
T8	Process 40 45	found
T9	Participant 46 60	a great spot .
T10	Function 46 47	a
T11	Elaborator 48 53	great
T12	Center 54 58	spot
R1	Participant parent:T11 child:T12
T14	State 48 53	great
T15	Participant 10 13	Joe
R2	Participant parent:T5 child:T15
T16	Function 14 16	is
T17	Process 17 18;25 31	a camper
T18	Adverbial 19 24	happy
T19	Function 17 18	a
T20	Center 25 31	camper
</div>
</td></tr></tbody>
</table>


## General

<table>
<tbody><tr><td width="600">
</td><td width="600">
UCCA:
<div class="ann-annotation">
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
</div>
</td></tr></tbody>
</table>
