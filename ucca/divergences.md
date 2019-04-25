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
7       camper  camper  NOUN    NN      Number=Sing     0       root    _        _
8       who     who     PRON    WP      PronType=Rel    10      nsubj   _   _
9       has     have    AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   10      aux     _  _
10      found   find    VERB    VBN     Tense=Past|VerbForm=Part        7       acl:relcl       _     _
11      a       a       DET     DT      Definite=Ind|PronType=Art       13      det     _  _
12      great   great   ADJ     JJ      Degree=Pos      13      amod    _ _
13      spot    spot    NOUN    NN      Number=Sing     10      obj     _  SpaceAfter=No
14      .       .       PUNCT   .       _       7       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
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
7       dinner  dinner  NOUN    NN      Number=Sing     3       nmod    _      SpaceAfter=No
8       .       .       PUNCT   .       _       3       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
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
<div class="ann-annotation">
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
1       Such    such    DET     PDT     _       4       det:predet      _    _
2       a       a       DET     DT      Definite=Ind|PronType=Art       4       det     _   _
3       convenient      convenient      ADJ     JJ      Degree=Pos      4       amod    _  _
4       location        location        NOUN    NN      Number=Sing     0       root    _  _
5       as      as      ADV     RB      _       4       advmod  _        _
6       well    well    ADV     RB      Degree=Pos      5       fixed   _ _
7       with    with    SCONJ   IN      _       9       case    _  _
8       coffee  coffee  NOUN    NN      Number=Sing     9       compound        _      _
9       shop    shop    NOUN    NN      Number=Sing     4       nmod    _     _
10      and     and     CCONJ   CC      _       12      cc      _   _
11      bradley bradley PROPN   NNP     Number=Sing     12      compound        _     _
12      food    food    PROPN   NNP     Number=Sing     9       conj    _  _
13      and     and     CCONJ   CC      _       14      cc      _   _
14      beverage        beverage        PROPN   NNP     Number=Sing     12      conj    _     _
15      right   right   ADV     RB      _       17      advmod  _       _
16      around  around  ADP     IN      _       17      case    _ _
17      corner  corner  NOUN    NN      Number=Sing     9       nmod    _   SpaceAfter=No
18      .       .       PUNCT   .       _       4       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
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


### Elaborator amod:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-071650-0007
# text = Back to my poor rating - I was excepted to medical school and went in to cancel my membership as I was told I could do since I was moving away.
1       Back    back    ADV     RB      _       0       root    _  _
2       to      to      ADP     IN      _       5       case    _  _
3       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      5       nmod:poss       _     _
4       poor    poor    ADJ     JJ      Degree=Pos      5       amod    _  _
5       rating  rating  NOUN    NN      Number=Sing     1       obl     _        _
6       -       -       PUNCT   ,       _       1       punct   _ _
7       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      9       nsubj:pass      _      _
8       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=1|Tense=Past|VerbForm=Fin   9       aux:pass        _      _
9       excepted        accept  VERB    VBN     Tense=Past|Typo=Yes|VerbForm=Part|Voice=Pass    1       parataxis       _     _
10      to      to      ADP     IN      _       12      case    _ _
11      medical medical ADJ     JJ      Degree=Pos      12      amod    _ _
12      school  school  NOUN    NN      Number=Sing     9       obl     _        _
13      and     and     CCONJ   CC      _       14      cc      _   _
14      went    go      VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        9       conj    _      _
15      in      in      ADV     RB      _       14      advmod  _       _
16      to      to      PART    TO      _       17      mark    _ _
17      cancel  cancel  VERB    VB      VerbForm=Inf    14      advcl   _     _
18      my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      19      nmod:poss       _    _
19      membership      membership      NOUN    NN      Number=Sing     17      obj     _  _
20      as      as      SCONJ   IN      _       23      mark    _ _
21      I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      23      nsubj:pass      _   _
22      was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=1|Tense=Past|VerbForm=Fin   23      aux:pass        _     _
23      told    tell    VERB    VBN     Tense=Past|VerbForm=Part|Voice=Pass     17      advcl   _     _
24      I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      26      nsubj   _        _
25      could   could   AUX     MD      VerbForm=Fin    26      aux     _  _
26      do      do      VERB    VB      VerbForm=Inf    23      ccomp   _        _
27      since   since   SCONJ   IN      _       30      mark    _ _
28      I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      30      nsubj   _        _
29      was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=1|Tense=Past|VerbForm=Fin   30      aux     _  _
30      moving  move    VERB    VBG     Tense=Pres|VerbForm=Part        23      ccomp   _        _
31      away    away    ADV     RB      _       30      advmod  _       SpaceAfter=No
32      .       .       PUNCT   .       _       1       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Back to my poor rating - I was excepted to medical school and went in to cancel my membership as I was told I could do since I was moving away .
T2	ParallelScene 0 22	Back to my poor rating
T3	ParallelScene 25 57	I was excepted to medical school
T4	Linker 58 61	and
T5	ParallelScene 62 93	went in to cancel my membership
T6	Linker 94 96	as
T7	ParallelScene 97 118	I was told I could do
T8	Linker 119 124	since
T9	ParallelScene 125 144	I was moving away .
T12	Participant 125 126	I
T13	Function 127 130	was
T14	Process 131 137	moving
T15	Adverbial 138 142	away
T16	Participant 97 98	I
T17	Function 99 102	was
T18	Process 103 107	told
T19	Participant 108 118	I could do
T20	Participant 108 109	I
T21	Adverbial 110 115	could
T22	Process 116 118	do
T24	Process 62 66	went
T25	Participant 67 69	in
T26	Participant 70 93	to cancel my membership
T27	Function 70 72	to
T28	Process 73 79	cancel
T29	Participant 80 93	my membership
T30	Participant 80 82	my
T31	State 83 93	membership
T33	Relator 67 69	in
T34	Participant 25 26	I
R1	Participant parent:T26 child:T34
T35	Function 27 30	was
T36	Process 31 39	excepted
T37	Participant 40 57	to medical school
T38	Relator 40 42	to
T39	Elaborator 43 50	medical
T40	Center 51 57	school
T41	Adverbial 0 4	Back
T42	Function 5 7	to
T43	Participant 8 10	my
T44	Adverbial 11 15	poor
T45	Process 16 22	rating
</div>
</td></tr></tbody>
</table>


### Participant nmod:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-247226-0005
# text = Going back after graduating your told you get a discount on services nope you dont.
1       Going   go      VERB    VBG     VerbForm=Ger    7       advcl   _ _
2       back    back    ADV     RB      _       1       advmod  _        _
3       after   after   SCONJ   IN      _       4       mark    _  _
4       graduating      graduate        VERB    VBG     VerbForm=Ger    1       advcl   _   _
5       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  7       nsubj:pass      _    SpaceAfter=No
6       r       be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        7       aux:pass        _      _
7       told    tell    VERB    VBN     Tense=Past|VerbForm=Part|Voice=Pass     0       root    _  _
8       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  9       nsubj   _ _
9       get     get     VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        7       ccomp   _ _
10      a       a       DET     DT      Definite=Ind|PronType=Art       11      det     _  _
11      discount        discount        NOUN    NN      Number=Sing     9       obj     _   _
12      on      on      ADP     IN      _       13      case    _ _
13      services        service NOUN    NNS     Number=Plur     11      nmod    _      _
14      nope    nope    INTJ    UH      _       16      discourse       _    _
15      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  16      nsubj   _        _
16      do      do      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        7       parataxis       _     SpaceAfter=No
17      nt      not     PART    RB      _       16      advmod  _       SpaceAfter=No
18      .       .       PUNCT   .       _       7       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Going back after graduating you r told you get a discount on services nope you do nt .
T2	ParallelScene 0 10	Going back
T3	ParallelScene 11 27	after graduating
T4	ParallelScene 28 69	you r told you get a discount on services
T5	ParallelScene 70 86	nope you do nt .
T7	Ground 70 74	nope
T8	Participant 75 78	you
T9	Function 79 81	do
T10	Adverbial 82 84	nt
T12	Participant 28 31	you
T13	Function 32 33	r
T14	Process 34 38	told
T15	Participant 39 69	you get a discount on services
T16	Participant 39 42	you
T17	Process 43 46	get
R1	Process parent:T5 child:T17
T18	Participant 47 57	a discount
T19	Participant 58 69	on services
T20	Relator 58 60	on
T21	Process 61 69	services
T22	Function 47 48	a
T23	Center 49 57	discount
T25	Relator 11 16	after
T26	Process 17 27	graduating
T29	Process 0 5	Going
T30	Adverbial 6 10	back
</div>
</td></tr></tbody>
</table>

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-095040-0004
# text = Stephanie's knowledge of the market and properties in our price range, made us feel secure in our decision to buy when we did.
1       Stephanie       Stephanie       PROPN   NNP     Number=Sing     3       nmod:poss       _     SpaceAfter=No
2       's      's      PART    POS     _       1       case    _  _
3       knowledge       knowledge       NOUN    NN      Number=Sing     14      nsubj   _        _
4       of      of      ADP     IN      _       6       case    _  _
5       the     the     DET     DT      Definite=Def|PronType=Art       6       det     _   _
6       market  market  NOUN    NN      Number=Sing     3       nmod    _       _
7       and     and     CCONJ   CC      _       8       cc      _    _
8       properties      property        NOUN    NNS     Number=Plur     6       conj    _    _
9       in      in      ADP     IN      _       12      case    _ _
10      our     we      PRON    PRP$    Number=Plur|Person=1|Poss=Yes|PronType=Prs      12      nmod:poss       _    _
11      price   price   NOUN    NN      Number=Sing     12      compound        _     _
12      range   range   NOUN    NN      Number=Sing     8       nmod    _       SpaceAfter=No
13      ,       ,       PUNCT   ,       _       14      punct   _        _
14      made    make    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
15      us      we      PRON    PRP     Case=Acc|Number=Plur|Person=1|PronType=Prs      14      obj     _  _
16      feel    feel    VERB    VB      VerbForm=Inf    15      xcomp   _        _
17      secure  secure  ADJ     JJ      Degree=Pos      16      xcomp   _        _
18      in      in      ADP     IN      _       20      case    _ _
19      our     we      PRON    PRP$    Number=Plur|Person=1|Poss=Yes|PronType=Prs      20      nmod:poss       _    _
20      decision        decision        NOUN    NN      Number=Sing     17      obl     _       _
21      to      to      PART    TO      _       22      mark    _ _
22      buy     buy     VERB    VB      VerbForm=Inf    20      acl     _       _
23      when    when    ADV     WRB     PronType=Int    25      mark    _ _
24      we      we      PRON    PRP     Case=Nom|Number=Plur|Person=1|PronType=Prs      25      nsubj   _        _
25      did     do      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        22      advcl   _   SpaceAfter=No
26      .       .       PUNCT   .       _       14      punct   _        _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Stephanie 's knowledge of the market and properties in our price range , made us feel secure in our decision to buy when we did .
T2	ParallelScene 0 115	Stephanie 's knowledge of the market and properties in our price range , made us feel secure in our decision to buy
T3	Linker 116 120	when
T4	ParallelScene 121 129	we did .
T6	Participant 121 123	we
T7	Function 124 127	did
T8	Participant 0 70	Stephanie 's knowledge of the market and properties in our price range
T9	Adverbial 73 77	made
T10	Participant 78 80	us
T11	State 81 85	feel
T12	Adverbial 86 92	secure
T13	Participant 93 115	in our decision to buy
T15	Relator 93 95	in
T16	Participant 96 99	our
T17	Adverbial 100 108	decision
T18	Function 109 111	to
T19	Process 112 115	buy
R1	Process parent:T4 child:T19
T20	Participant 0 12	Stephanie 's
T21	State 13 22	knowledge
T22	Participant 23 70	of the market and properties in our price range
T23	Relator 23 25	of
T24	Center 26 36	the market
T25	Connector 37 40	and
T26	Center 41 70	properties in our price range
T27	Center 41 51	properties
T28	Elaborator 52 70	in our price range
T29	Relator 52 54	in
T30	Elaborator 55 58	our
T31	Elaborator 59 64	price
T32	Center 65 70	range
T33	Function 26 29	the
T34	Center 30 36	market
T35	Center 0 9	Stephanie
T36	Relator 10 12	's
</div>
</td></tr></tbody>
</table>

### Elaborator nmod/acl:
<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-295288-0006
# text = Now my cars gears and brakes have never run so well... ever its like driving a new car.
1       Now     now     ADV     RB      _       10      advmod  _       _
2       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      3       nmod:poss       _     _
3       car     car     NOUN    NN      Number=Sing     5       nmod:poss       _     SpaceAfter=No
4       s       's      PART    POS     _       3       case    _  _
5       gears   gear    NOUN    NNS     Number=Plur     10      nsubj   _        _
6       and     and     CCONJ   CC      _       7       cc      _    _
7       brakes  brake   NOUN    NNS     Number=Plur     5       conj    _     _
8       have    have    AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        10      aux     _  _
9       never   never   ADV     RB      _       10      advmod  _       _
10      run     run     VERB    VBN     Tense=Past|VerbForm=Part        0       root    _  _
11      so      so      ADV     RB      _       12      advmod  _       _
12      well    well    ADV     RB      Degree=Pos      10      advmod  _       SpaceAfter=No
13      ...     ...     PUNCT   ,       _       10      punct   _        _
14      ever    ever    ADV     RB      _       10      advmod  _       _
15      it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  16      nsubj   _        SpaceAfter=No
16      s       be      VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   10      parataxis       _    _
17      like    like    SCONJ   IN      _       18      mark    _ _
18      driving drive   VERB    VBG     VerbForm=Ger    16      advcl   _   _
19      a       a       DET     DT      Definite=Ind|PronType=Art       21      det     _  _
20      new     new     ADJ     JJ      Degree=Pos      21      amod    _ _
21      car     car     NOUN    NN      Number=Sing     18      obj     _  SpaceAfter=No
22      .       .       PUNCT   .       _       10      punct   _        _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Now my car s gears and brakes have never run so well ... ever it s like driving a new car .
T2	Linker 0 3	Now
T3	ParallelScene 4 61	my car s gears and brakes have never run so well ... ever
T4	ParallelScene 62 66;72 91	it s driving a new car .
T5	Linker 67 71	like
T7	Participant 62 64	it
T8	Function 65 66	s
T9	Process 72 79	driving
T10	Participant 80 91	a new car .
T11	Function 80 81	a
T12	Elaborator 82 85	new
T13	Center 86 89	car
R1	Participant parent:T12 child:T13
T14	State 82 85	new
T15	Participant 4 29	my car s gears and brakes
T16	Function 30 34	have
T17	Time 35 40	never
T18	Process 41 44	run
T19	Adverbial 45 52	so well
T20	Ground 57 61	ever
T22	Elaborator 45 47	so
T23	Center 48 52	well
T24	Elaborator 4 12	my car s
T25	Center 13 29	gears and brakes
T26	Center 13 18	gears
T27	Connector 19 22	and
T28	Center 23 29	brakes
T29	Elaborator 4 6	my
T30	Center 7 10	car
R2	Participant parent:T29 child:T30
T31	Relator 11 12	s
T32	State 4 6	my
</div>
</td></tr></tbody>
</table>


<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-241739-0005
# text = Some of the younger kids that work there are a bit sub par, but if you wait for Nick... you'll be good.
1       Some    some    DET     DT      _       13      nsubj   _        _
2       of      of      ADP     IN      _       5       case    _  _
3       the     the     DET     DT      Definite=Def|PronType=Art       5       det     _   _
4       younger younger ADJ     JJR     Degree=Cmp      5       amod    _  _
5       kids    kid     NOUN    NNS     Number=Plur     1       nmod    _       _
6       that    that    PRON    WDT     PronType=Rel    7       nsubj   _   _
7       work    work    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        5       acl:relcl       _     _
8       there   there   ADV     RB      PronType=Dem    7       advmod  _        _
9       are     be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        13      cop     _  _
10      a       a       DET     DT      Definite=Ind|PronType=Art       11      det     _  _
11      bit     bit     NOUN    NN      Number=Sing     13      obl:npmod       _    _
12      sub     sub     X       AFX     _       13      advmod  _       _
13      par     par     ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
14      ,       ,       PUNCT   ,       _       25      punct   _        _
15      but     but     CCONJ   CC      _       25      cc      _   _
16      if      if      SCONJ   IN      _       18      mark    _ _
17      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  18      nsubj   _        _
18      wait    wait    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        25      advcl   _     _
19      for     for     ADP     IN      _       20      case    _ _
20      Nick    Nick    PROPN   NNP     Number=Sing     18      obl     _      SpaceAfter=No
21      ...     ...     PUNCT   ,       _       25      punct   _        _
22      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  25      nsubj   _        SpaceAfter=No
23      'll     will    AUX     MD      VerbForm=Fin    25      aux     _  _
24      be      be      AUX     VB      VerbForm=Inf    25      cop     _  _
25      good    good    ADJ     JJ      Degree=Pos      13      conj    _     SpaceAfter=No
26      .       .       PUNCT   .       _       13      punct   _        _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Some of the younger kids that work there are a bit sub par , but if you wait for Nick ... you 'll be good .
T2	ParallelScene 0 58	Some of the younger kids that work there are a bit sub par
T3	Linker 61 64	but
T4	Linker 65 67	if
T5	ParallelScene 68 85	you wait for Nick
T6	ParallelScene 90 107	you 'll be good .
T9	Participant 90 93	you
T10	Function 94 97	'll
T11	Function 98 100	be
T12	State 101 105	good
T14	Participant 68 71	you
T15	Process 72 76	wait
T16	Participant 77 85	for Nick
T17	Relator 77 80	for
T18	Center 81 85	Nick
T19	Participant 0 40	Some of the younger kids that work there
T20	Function 41 44	are
T21	Adverbial 45 50	a bit
T22	State 51 58	sub par
T23	Elaborator 51 54	sub
T24	Center 55 58	par
T25	Quantifier 0 7	Some of
T26	Function 8 11	the
T27	Elaborator 12 19	younger
T28	Center 20 24	kids
R1	Participant parent:T29 child:T28
T29	Elaborator 25 40	that work there
T30	Relator 25 29	that
T31	Process 30 34	work
T32	Participant 35 40	there
T33	Center 0 4	Some
T34	Relator 5 7	of
</div>
</td></tr></tbody>
</table>


### Unmatched acl

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-024385-0004
# text = The prices were worth what I got.
1       The     the     DET     DT      Definite=Def|PronType=Art       2       det     _   _
2       prices  price   NOUN    NNS     Number=Plur     4       nsubj   _ _
3       were    be      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        4       cop     _   _
4       worth   worth   ADJ     JJ      Degree=Pos      0       root    _  _
5       what    what    PRON    WP      PronType=Int    4       obj     _   _
6       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      7       nsubj   _ _
7       got     get     VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        4       acl:relcl       _     SpaceAfter=No
8       .       .       PUNCT   .       _       4       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
The prices were worth what I got .
T2	ParallelScene 0 34	The prices were worth what I got .
T4	Participant 0 10	The prices
T5	Function 11 15	were
T6	State 16 21	worth
T7	Participant 22 34	what I got .
T8	Participant 22 26	what
T9	Participant 27 28	I
T10	Process 29 32	got
T11	Function 0 3	The
T12	Center 4 10	prices
</div>
</td></tr></tbody>
</table>

### Relator case

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-303922-0003
# text = The team at Bradley Chevron kept my car running for well past its expected death!
1       The     the     DET     DT      Definite=Def|PronType=Art       2       det     _   _
2       team    team    NOUN    NN      Number=Sing     6       nsubj   _ _
3       at      at      ADP     IN      _       5       case    _  _
4       Bradley Bradley PROPN   NNP     Number=Sing     5       compound        _      _
5       Chevron Chevron PROPN   NNP     Number=Sing     2       nmod    _       _
6       kept    keep    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
7       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      8       nmod:poss       _     _
8       car     car     NOUN    NN      Number=Sing     6       obj     _   _
9       running run     VERB    VBG     VerbForm=Ger    6       advcl   _ _
10      for     for     ADP     IN      _       15      case    _ _
11      well    well    ADV     RB      Degree=Pos      15      advmod  _       _
12      past    past    ADP     IN      _       15      case    _ _
13      its     its     PRON    PRP$    Gender=Neut|Number=Sing|Person=3|Poss=Yes|PronType=Prs  15      nmod:poss       _    _
14      expected        expect  VERB    VBN     Tense=Past|VerbForm=Part        15      amod    _ _
15      death   death   NOUN    NN      Number=Sing     9       obl     _      SpaceAfter=No
16      !       !       PUNCT   .       _       6       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
The team at Bradley Chevron kept my car running for well past its expected death !
T2	ParallelScene 0 47	The team at Bradley Chevron kept my car running
T3	Linker 48 51	for
T4	ParallelScene 52 82	well past its expected death !
T6	Time 52 61	well past
T7	Participant 62 65	its
T8	Adverbial 66 74	expected
T9	Process 75 80	death
T10	Elaborator 52 56	well
T11	Center 57 61	past
T12	Participant 0 27	The team at Bradley Chevron
T13	Adverbial 28 32	kept
T14	Participant 33 39	my car
T15	Process 40 47	running
T16	Elaborator 33 35	my
T17	Center 36 39	car
R1	Participant parent:T16 child:T17
T18	State 33 35	my
T19	Function 0 3	The
T20	Center 4 8	team
T21	Elaborator 9 27	at Bradley Chevron
T22	Relator 9 11	at
T23	Center 12 27	Bradley Chevron
</div>
</td></tr></tbody>
</table>

### Linker case

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-295935-0001
# text = Very Informative website with alot of good work
1       Very    very    ADV     RB      _       2       advmod  _        _
2       Informative     informative     ADJ     JJ      Degree=Pos      3       amod    _  _
3       website website NOUN    NN      Number=Sing     0       root    _  _
4       with    with    ADP     IN      _       6       case    _  _
5       a       a       DET     DT      Definite=Ind|PronType=Art       6       det     _   SpaceAfter=No
6       lot     lot     NOUN    NN      Number=Sing     3       nmod    _     _
7       of      of      ADP     IN      _       9       case    _  _
8       good    good    ADJ     JJ      Degree=Pos      9       amod    _  _
9       work    work    NOUN    NN      Number=Sing     6       nmod    _       _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Very Informative website with a lot of good work
T2	ParallelScene 0 48	Very Informative website with a lot of good work
T3	Adverbial 0 4	Very
T4	State 5 16	Informative
T5	Participant 17 48	website with a lot of good work
T6	Center 17 24	website
T7	Elaborator 25 48	with a lot of good work
T8	Relator 25 29	with
T9	Adverbial 30 35	a lot
T10	Process 36 38;44 48	of work
T11	Adverbial 39 43	good
T12	Relator 36 38	of
T13	Center 44 48	work
</div>
</td></tr></tbody>
</table>

### Elaborator case

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-095040-0003
# text = She worked with us for over a year, helping us find our perfect home.
1       She     she     PRON    PRP     Case=Nom|Gender=Fem|Number=Sing|Person=3|PronType=Prs   2       nsubj   _ _
2       worked  work    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
3       with    with    ADP     IN      _       4       case    _  _
4       us      we      PRON    PRP     Case=Acc|Number=Plur|Person=1|PronType=Prs      2       obl     _      _
5       for     for     ADP     IN      _       8       case    _  _
6       over    over    ADP     IN      _       8       case    _  _
7       a       a       DET     DT      Definite=Ind|PronType=Art       8       det     _   _
8       year    year    NOUN    NN      Number=Sing     2       obl     _      SpaceAfter=No
9       ,       ,       PUNCT   ,       _       2       punct   _ _
10      helping help    VERB    VBG     VerbForm=Ger    2       advcl   _ _
11      us      we      PRON    PRP     Case=Acc|Number=Plur|Person=1|PronType=Prs      10      obj     _   _
12      find    find    VERB    VB      VerbForm=Inf    10      xcomp   _        _
13      our     we      PRON    PRP$    Number=Plur|Person=1|Poss=Yes|PronType=Prs      15      nmod:poss       _    _
14      perfect perfect ADJ     JJ      Degree=Pos      15      amod    _ _
15      home    home    NOUN    NN      Number=Sing     12      obj     _  SpaceAfter=No
16      .       .       PUNCT   .       _       2       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
She worked with us for over a year , helping us find our perfect home .
T2	ParallelScene 0 34	She worked with us for over a year
T3	ParallelScene 37 71	helping us find our perfect home .
T6	Adverbial 37 44	helping
T7	Participant 45 47	us
T8	Process 48 52	find
T9	Participant 53 71	our perfect home .
T10	Elaborator 53 56	our
T11	Elaborator 57 64	perfect
T12	Center 65 69	home
R1	Participant parent:T10 child:T12
R2	Participant parent:T11 child:T12
T13	State 57 64	perfect
T14	State 53 56	our
T15	Participant 0 3	She
R3	Participant parent:T3 child:T15
T16	Process 4 10	worked
T17	Participant 11 18	with us
T18	Time 19 34	for over a year
T19	Relator 19 22	for
T20	Quantifier 23 29	over a
T21	Center 30 34	year
T22	Elaborator 23 27	over
T23	Center 28 29	a
T24	Relator 11 15	with
T25	Center 16 18	us
</div>
</td></tr></tbody>
</table>

### State case

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-034501-0003
# text = It is right on the hustle and bustle of Wisconsin Ave but some might miss it as it is nestled in between Subway Sandwiches and Modell's.
1       It      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  6       nsubj   _ _
2       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   6       cop     _   _
3       right   right   ADV     RB      _       6       advmod  _        _
4       on      on      ADP     IN      _       6       case    _  _
5       the     the     DET     DT      Definite=Def|PronType=Art       6       det     _   _
6       hustle  hustle  NOUN    NN      Number=Sing     0       root    _  _
7       and     and     CCONJ   CC      _       8       cc      _    _
8       bustle  bustle  NOUN    NN      Number=Sing     6       conj    _      _
9       of      of      ADP     IN      _       11      case    _ _
10      Wisconsin       Wisconsin       PROPN   NNP     Number=Sing     11      compound        _     _
11      Ave     Ave     PROPN   NNP     Number=Sing     6       nmod    _       _
12      but     but     CCONJ   CC      _       15      cc      _   _
13      some    some    DET     DT      _       15      nsubj   _        _
14      might   might   AUX     MD      VerbForm=Fin    15      aux     _  _
15      miss    miss    VERB    VB      VerbForm=Inf    6       conj    _      _
16      it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  15      obj     _  _
17      as      as      SCONJ   IN      _       20      mark    _ _
18      it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  20      nsubj:pass      _   _
19      is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   20      aux:pass        _     _
20      nestled nestle  VERB    VBN     Tense=Past|VerbForm=Part        15      advcl   _     _
21      in      in      ADP     IN      _       24      case    _ _
22      between between ADP     IN      _       21      fixed   _        _
23      Subway  Subway  PROPN   NNP     Number=Sing     24      compound        _     _
24      Sandwiches      Sandwiches      PROPN   NNPS    Number=Plur     20      obl     _       _
25      and     and     CCONJ   CC      _       26      cc      _   _
26      Modell  Modell  PROPN   NNP     Number=Sing     24      conj    _   SpaceAfter=No
27      's      's      PART    POS     _       26      case    _ SpaceAfter=No
28      .       .       PUNCT   .       _       6       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
It is right on the hustle and bustle of Wisconsin Ave but some might miss it as it is nestled in between Subway Sandwiches and Modell 's .
T2	ParallelScene 0 53	It is right on the hustle and bustle of Wisconsin Ave
T3	Linker 54 57	but
T4	ParallelScene 58 76	some might miss it
T5	Linker 77 79	as
T6	ParallelScene 80 138	it is nestled in between Subway Sandwiches and Modell 's .
T8	Participant 80 82	it
T9	Function 83 85	is
T10	State 86 93	nestled
T11	Participant 94 138	in between Subway Sandwiches and Modell 's .
T12	Relator 94 104	in between
T13	Center 105 122	Subway Sandwiches
T14	Connector 123 126	and
T15	Center 127 136	Modell 's
T16	Function 94 96	in
T17	Center 97 104	between
T18	Participant 58 62	some
T19	Adverbial 63 68	might
T20	Process 69 73	miss
T21	Participant 74 76	it
T22	Participant 0 2	It
T23	Function 3 5	is
T24	Adverbial 6 11	right
T25	State 12 14	on
T26	Participant 15 53	the hustle and bustle of Wisconsin Ave
T27	Function 15 18	the
T28	Center 19 36	hustle and bustle
T29	Elaborator 37 53	of Wisconsin Ave
T30	Relator 37 39	of
T31	Center 40 53	Wisconsin Ave
T32	Center 19 25	hustle
T33	Connector 26 29	and
T34	Center 30 36	bustle
</div>
</td></tr></tbody>
</table>

### Connector cc

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-023926-0002
# text = Mercedes and Dan are very thorough and on top of everything!
1       Mercedes        Mercedes        PROPN   NNP     Number=Sing     6       nsubj   _ _
2       and     and     CCONJ   CC      _       3       cc      _    _
3       Dan     Dan     PROPN   NNP     Number=Sing     1       conj    _      _
4       are     be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        6       cop     _   _
5       very    very    ADV     RB      _       6       advmod  _        _
6       thorough        thorough        ADJ     JJ      Degree=Pos      0       root    _  _
7       and     and     CCONJ   CC      _       9       cc      _    _
8       on      on      ADP     IN      _       9       case    _  _
9       top     top     NOUN    NN      Number=Sing     6       conj    _      _
10      of      of      ADP     IN      _       11      case    _ _
11      everything      everything      PRON    NN      Number=Sing     9       nmod    _       SpaceAfter=No
12      !       !       PUNCT   .       _       6       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Mercedes and Dan are very thorough and on top of everything !
T2	ParallelScene 0 34	Mercedes and Dan are very thorough
T3	Linker 35 38	and
T4	ParallelScene 39 61	on top of everything !
T5	State 39 45	on top
T6	Participant 46 61	of everything !
T7	Relator 46 48	of
T8	Center 49 59	everything
T10	Participant 0 16	Mercedes and Dan
R1	Participant parent:T4 child:T10
T11	Function 17 20	are
T12	Adverbial 21 25	very
T13	State 26 34	thorough
T14	Center 0 8	Mercedes
T15	Connector 9 12	and
T16	Center 13 16	Dan
</div>
</td></tr></tbody>
</table>

### Linker cc

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-299148-0001
# text = Outdated but not bad
1       Outdated        outdated        ADJ     JJ      Degree=Pos      0       root    _  _
2       but     but     CCONJ   CC      _       4       cc      _    _
3       not     not     ADV     RB      _       4       advmod  _        _
4       bad     bad     ADJ     JJ      Degree=Pos      1       conj    _      _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
Outdated but not bad
T2	ParallelScene 0 8	Outdated
T3	Linker 9 12	but
T4	ParallelScene 13 20	not bad
T6	Adverbial 13 16	not
T7	State 17 20	bad
T9	State 0 8	Outdated
</div>
</td></tr></tbody>
</table>

### Elaborator det

<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">
# sent_id = reviews-071650-0013
# text = I will never recommend this gym to any woman.
1       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      4       nsubj   _ _
2       will    will    AUX     MD      VerbForm=Fin    4       aux     _   _
3       never   never   ADV     RB      _       4       advmod  _        _
4       recommend       recommend       VERB    VB      VerbForm=Inf    0       root    _  _
5       this    this    DET     DT      Number=Sing|PronType=Dem        6       det     _   _
6       gym     gym     NOUN    NN      Number=Sing     4       obj     _   _
7       to      to      ADP     IN      _       9       case    _  _
8       any     any     DET     DT      _       9       det     _   _
9       woman   woman   NOUN    NN      Number=Sing     4       obl     _        SpaceAfter=No
10      .       .       PUNCT   .       _       4       punct   _ _
</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">
I will never recommend this gym to any woman .
T2	ParallelScene 0 46	I will never recommend this gym to any woman .
T4	Participant 0 1	I
T5	Function 2 6	will
T6	Adverbial|Time 7 12	never
T7	Process 13 22	recommend
T8	Participant 23 31	this gym
T9	Participant 32 46	to any woman .
T10	Relator 32 34	to
T11	Elaborator 35 38	any
T12	Center 39 44	woman
T13	Elaborator 23 27	this
T14	Center 28 31	gym
</div>
</td></tr></tbody>
</table>




<table>
<tbody><tr><td width="600">
UD:
<div class="conllu-parse">

</div>
</td><td width="600">
UCCA:
<div class="ann-annotation">

</div>
</td></tr></tbody>
</table>



<!-- ([\d_]+(:\w+)+\|?)+ -->


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
