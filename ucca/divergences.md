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
1       Overall overall ADV     RB      _       7       advmod  _        SpaceAfter=No
2       ,       ,       PUNCT   ,       _       7       punct   _ _
3       Joe     Joe     PROPN   NNP     Number=Sing     7       nsubj   _ _
4       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   7       cop     _   _
5       a       a       DET     DT      Definite=Ind|PronType=Art       7       det     _   _
6       happy   happy   ADJ     JJ      Degree=Pos      7       amod    _  _
7       camper  camper  NOUN    NN      Number=Sing     0       root    1_        _
8       who     who     PRON    WP      PronType=Rel    10      nsubj   _   _
9       has     have    AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   10      aux     1_  _
10      found   find    VERB    VBN     Tense=Past|VerbForm=Part        7       acl:relcl       _:relcl     _
11      a       a       DET     DT      Definite=Ind|PronType=Art       13      det     1_  _
12      great   great   ADJ     JJ      Degree=Pos      13      amod    1_ _
13      spot    spot    NOUN    NN      Number=Sing     10      obj     1_  SpaceAfter=No
14      .       .       PUNCT   .       _       7       punct   _ _
</div>
</td><td width="600">
UCCA:
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

### Adverbial amod:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-305187-0007
# text = A perfect place for a romantic dinner.
1       A       a       DET     DT      Definite=Ind|PronType=Art       3       det     _   _
2       perfect perfect ADJ     JJ      Degree=Pos      3       amod    _  _
3       place   place   NOUN    NN      Number=Sing     0       root    _  _
4       for     for     ADP     IN      _       7       case    _  _
5       a       a       DET     DT      Definite=Ind|PronType=Art       7       det     _   _
6       romantic        romantic        ADJ     JJ      Degree=Pos      7       amod    _  _
7       dinner  dinner  NOUN    NN      Number=Sing     3       nmod    _:for      SpaceAfter=No
8       .       .       PUNCT   .       _       3       punct   _ _
</div>
</td><td width="600">
UCCA:
A perfect place for a romantic dinner .
T2	ParallelScene 0 15	A perfect place
T3	Linker 16 19	for
T4	ParallelScene 20 39	a romantic dinner .
T6	Process 20 21;31 39	a dinner .
T7	Adverbial 22 30	romantic
T8	Function 20 21	a
T9	Center 31 37	dinner
T10	Participant 0 1;10 15	A place
T11	State 2 9	perfect
T12	Function 0 1	A
T13	Center 10 15	place
</div>
</td></tr></tbody>
</table>

### State amod:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-073356-0001
# text = Beautiful hotel!
1       Beautiful       beautiful       ADJ     JJ      Degree=Pos      2       amod    _  _
2       hotel   hotel   NOUN    NN      Number=Sing     0       root    _  SpaceAfter=No
3       !       !       PUNCT   .       _       2       punct   _ _
</div>
</td><td width="600">
UCCA:
Beautiful hotel !
T2	ParallelScene 0 17	Beautiful hotel !
T4	State 0 9	Beautiful
T5	Participant 10 15	hotel
</div>
</td></tr></tbody>
</table>


<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-303922-0005
# text = Such a convenient location as well with coffee shop and bradley food and beverage right around corner.
1       Such    such    DET     PDT     _       4       det:predet      _:predet    _
2       a       a       DET     DT      Definite=Ind|PronType=Art       4       det     _   _
3       convenient      convenient      ADJ     JJ      Degree=Pos      4       amod    _  _
4       location        location        NOUN    NN      Number=Sing     0       root    _  _
5       as      as      ADV     RB      _       4       advmod  _        _
6       well    well    ADV     RB      Degree=Pos      5       fixed   _ _
7       with    with    SCONJ   IN      _       9       case    _  _
8       coffee  coffee  NOUN    NN      Number=Sing     9       compound        _      _
9       shop    shop    NOUN    NN      Number=Sing     4       nmod    _:with     _
10      and     and     CCONJ   CC      _       12      cc      1_   _
11      bradley bradley PROPN   NNP     Number=Sing     12      compound        1_     _
12      food    food    PROPN   NNP     Number=Sing     9       conj    _:with|_:and  _
13      and     and     CCONJ   CC      _       14      cc      1_   _
14      beverage        beverage        PROPN   NNP     Number=Sing     12      conj    1_:and     _
15      right   right   ADV     RB      _       17      advmod  1_       _
16      around  around  ADP     IN      _       17      case    1_ _
17      corner  corner  NOUN    NN      Number=Sing     9       nmod    _:around   SpaceAfter=No
18      .       .       PUNCT   .       _       4       punct   _ _
</div>
</td><td width="600">
UCCA:
Such a convenient location as well with coffee shop and bradley food and beverage right around corner .
T2	ParallelScene 0 34	Such a convenient location as well
T3	Linker 35 39	with
T4	ParallelScene 40 103	coffee shop and bradley food and beverage right around corner .
T5	Participant 40 81	coffee shop and bradley food and beverage
T6	Adverbial 82 87	right
T7	State 88 94	around
T8	Participant 95 101	corner
T10	Center 40 51	coffee shop
T11	Connector 52 55	and
T12	Center 56 81	bradley food and beverage
T13	Elaborator 40 46	coffee
T14	Center 47 51	shop
T15	Adverbial 0 4	Such
T16	Participant 5 6;18 26	a location
T17	State 7 17	convenient
T18	Adverbial 27 34	as well
T19	Function 5 6	a
T20	Center 18 26	location
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
