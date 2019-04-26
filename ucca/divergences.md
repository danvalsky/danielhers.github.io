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

## Scene/Non-Scene
### Participant nsubj
<table id="305187-0005">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-305187-0005
# text = Wine was excellent.
1       Wine    wine    NOUN    NN      Number=Sing     3       nsubj   _ _
2       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   3       cop     _   _
3       excellent       excellent       ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
4       .       .       PUNCT   .       _       3       punct   _ _
</div>
</td><td>
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

### Process nsubj
<table id="079007-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-079007-0002
# text = But service is very poor.
1       But     but     CCONJ   CC      _       5       cc      _    _
2       service service NOUN    NN      Number=Sing     5       nsubj   _ _
3       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   5       cop     _   _
4       very    very    ADV     RB      _       5       advmod  _        _
5       poor    poor    ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
6       .       .       PUNCT   .       _       5       punct   _ _
</div>
</td><td>
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

### Linker nsubj
<table id="295491-0007">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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

### Adverbial amod
<table id="305187-0007">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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

### State amod
<table id="073356-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-073356-0001
# text = Beautiful hotel!
1       Beautiful       beautiful       ADJ     JJ      Degree=Pos      2       amod    _  _
2       hotel   hotel   NOUN    NN      Number=Sing     0       root    _  SpaceAfter=No
3       !       !       PUNCT   .       _       2       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Beautiful hotel !
T2	ParallelScene 0 17	Beautiful hotel !
T4	State 0 9	Beautiful
T5	Participant 10 15	hotel
</div>
</td></tr></tbody>
</table>


<table id="303922-0005">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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


### Elaborator amod
<table id="071650-0007">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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


### Participant nmod
<table id="247226-0005">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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

<table id="095040-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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

### Elaborator nmod/acl
<table id="295288-0006">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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


<table id="241739-0005">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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
<table id="024385-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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
<table id="303922-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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
<table id="295935-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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
<table id="095040-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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
<table id="034501-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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
<table id="023926-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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
<table id="299148-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-299148-0001
# text = Outdated but not bad
1       Outdated        outdated        ADJ     JJ      Degree=Pos      0       root    _  _
2       but     but     CCONJ   CC      _       4       cc      _    _
3       not     not     ADV     RB      _       4       advmod  _        _
4       bad     bad     ADJ     JJ      Degree=Pos      1       conj    _      _
</div>
</td><td>
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
<table id="071650-0013">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td><td>
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


### Adverbial det
<table id="252791-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# newdoc id = reviews-252791
# sent_id = reviews-252791-0001
# text = no feathers in stock!!!!
1       no      no      DET     DT      _       2       det     _   _
2       feathers        feather NOUN    NNS     Number=Plur     0       root    _  _
3       in      in      ADP     IN      _       4       case    _  _
4       stock   stock   NOUN    NN      Number=Sing     2       nmod    _       SpaceAfter=No
5       !!!!    !!!!    PUNCT   .       _       2       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
no feathers in stock !!!!
T2	ParallelScene 0 25	no feathers in stock !!!!
T4	Adverbial 0 2	no
T5	Participant 3 11	feathers
T6	State 12 25	in stock !!!!
T7	Relator 12 14	in
T8	Center 15 20	stock
</div>
</td></tr></tbody>
</table>

<table id="243799-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-243799-0002
# text = went in there and got my dog groomed came home to an uneven dog then took him back to get evened up what a mistake!
1       went    go      VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        25      parataxis       _    _
2       in      in      ADP     IN      _       3       case    _  _
3       there   there   ADV     RB      PronType=Dem    1       obl     _        _
4       and     and     CCONJ   CC      _       5       cc      _    _
5       got     get     VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        1       conj    _      _
6       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      7       nmod:poss       _     _
7       dog     dog     NOUN    NN      Number=Sing     5       obj     _     _
8       groomed groom   VERB    VBN     Tense=Past|VerbForm=Part        5       xcomp   _ _
9       came    come    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        1       conj    _      _
10      home    home    ADV     RB      _       9       advmod  _        _
11      to      to      ADP     IN      _       14      case    _ _
12      an      a       DET     DT      Definite=Ind|PronType=Art       14      det     _  _
13      uneven  uneven  ADJ     JJ      Degree=Pos      14      amod    _ _
14      dog     dog     NOUN    NN      Number=Sing     9       obl     _        _
15      then    then    ADV     RB      PronType=Dem    16      advmod  _       _
16      took    take    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        1       conj    _      _
17      him     he      PRON    PRP     Case=Acc|Gender=Masc|Number=Sing|Person=3|PronType=Prs  16      obj     _  _
18      back    back    ADV     RB      _       16      advmod  _       _
19      to      to      PART    TO      _       21      mark    _ _
20      get     get     AUX     VB      VerbForm=Inf    21      aux:pass        _     _
21      evened  even    VERB    VBN     Tense=Past|VerbForm=Part        16      advcl   _     _
22      up      up      ADP     RP      _       21      compound:prt    _ _
23      what    what    PRON    WP      PronType=Int    25      det:predet      _   _
24      a       a       DET     DT      Definite=Ind|PronType=Art       25      det     _  _
25      mistake mistake NOUN    NN      Number=Sing     0       root    _  SpaceAfter=No
26      !       !       PUNCT   .       _       25      punct   _        _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
went in there and got my dog groomed came home to an uneven dog then took him back to get evened up what a mistake !
T2	ParallelScene 0 13	went in there
T3	Linker 14 17	and
T4	ParallelScene 18 36	got my dog groomed
T5	ParallelScene 37 46	came home
T6	Linker 47 49	to
T7	ParallelScene 50 63	an uneven dog
T8	Linker 64 68	then
T9	ParallelScene 69 82	took him back
T10	Linker 83 85	to
T11	ParallelScene 86 99	get evened up
T12	ParallelScene 100 116	what a mistake !
T14	Adverbial 100 104	what
T15	State 105 116	a mistake !
T16	Function 105 106	a
T17	Center 107 114	mistake
T18	Adverbial 86 89	get
T19	Process 90 99	evened up
T21	Process 69 73	took
T22	Participant 74 77	him
R1	Participant parent:T11 child:T22
T23	Adverbial 78 82	back
T24	Participant 50 52;60 63	an dog
T25	State 53 59	uneven
T26	Function 50 52	an
T27	Center 60 63	dog
T29	Process 37 41	came
T30	Participant 42 46	home
T32	Adverbial 18 21	got
T33	Participant 22 28	my dog
T34	Process 29 36	groomed
T35	Elaborator 22 24	my
T36	Center 25 28	dog
R2	Participant parent:T35 child:T36
T37	State 22 24	my
T39	Process 0 4	went
T40	Participant 5 13	in there
T41	Relator 5 7	in
T42	Center 8 13	there
</div>
</td></tr></tbody>
</table>

<table id="349020-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-349020-0002
# text = The night I drove back home, I found that the rear window has some leakage.
1       The     the     DET     DT      Definite=Def|PronType=Art       2       det     _   _
2       night   night   NOUN    NN      Number=Sing     9       obl:tmod        _      _
3       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      4       nsubj   _ _
4       drove   drive   VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        2       acl:relcl       _     _
5       back    back    ADV     RB      _       6       advmod  _        _
6       home    home    ADV     RB      _       4       advmod  _        SpaceAfter=No
7       ,       ,       PUNCT   ,       _       9       punct   _ _
8       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      9       nsubj   _ _
9       found   find    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
10      that    that    SCONJ   IN      _       14      mark    _ _
11      the     the     DET     DT      Definite=Def|PronType=Art       13      det     _  _
12      rear    rear    ADJ     JJ      Degree=Pos      13      amod    _ _
13      window  window  NOUN    NN      Number=Sing     14      nsubj   _        _
14      has     have    VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   9       ccomp   _ _
15      some    some    DET     DT      _       16      det     _  _
16      leakage leakage NOUN    NN      Number=Sing     14      obj     _  SpaceAfter=No
17      .       .       PUNCT   .       _       9       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
The night I drove back home , I found that the rear window has some leakage .
T2	Linker 0 9	The night
T3	ParallelScene 10 27	I drove back home
T4	ParallelScene 30 77	I found that the rear window has some leakage .
T7	Participant 30 31	I
T8	Process 32 37	found
T9	Participant 38 77	that the rear window has some leakage .
T10	Relator 38 42	that
T11	Participant 43 58	the rear window
T12	Function 59 62	has
T13	Adverbial 63 67	some
T14	Process 68 75	leakage
T15	Function 43 46	the
T16	Elaborator 47 51	rear
T17	Center 52 58	window
T18	Participant 10 11	I
T19	Process 12 17	drove
T20	Adverbial 18 22	back
T21	Participant 23 27	home
T22	Function 0 3	The
T23	Center 4 9	night
</div>
</td></tr></tbody>
</table>

## Primary/Secondary Relations
### Adverbial advmod
<table id="241855-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-241855-0002
# text = I sometimes go into this store just for something to do on a sunday afternoon.
1       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      3       nsubj   _ _
2       sometimes       sometimes       ADV     RB      _       3       advmod  _        _
3       go      go      VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        0       root    _  _
4       into    into    ADP     IN      _       6       case    _  _
5       this    this    DET     DT      Number=Sing|PronType=Dem        6       det     _   _
6       store   store   NOUN    NN      Number=Sing     3       obl     _      _
7       just    just    ADV     RB      _       9       advmod  _        _
8       for     for     ADP     IN      _       9       case    _  _
9       something       something       PRON    NN      Number=Sing     3       obl     _       _
10      to      to      PART    TO      _       11      mark    _ _
11      do      do      VERB    VB      VerbForm=Inf    9       acl     _        _
12      on      on      ADP     IN      _       15      case    _ _
13      a       a       DET     DT      Definite=Ind|PronType=Art       15      det     _  _
14      sunday  sunday  PROPN   NNP     Number=Sing     15      compound        _     _
15      afternoon       afternoon       NOUN    NN      Number=Sing     11      obl     _       SpaceAfter=No
16      .       .       PUNCT   .       _       3       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
I sometimes go into this store just for something to do on a sunday afternoon .
T2	ParallelScene 0 30	I sometimes go into this store
T3	ParallelScene 31 35;40 79	just something to do on a sunday afternoon .
T4	Linker 36 39	for
T6	Adverbial 31 35	just
T7	Participant 40 49	something
T8	Function 50 52	to
T9	Process 53 55	do
T10	Time 56 79	on a sunday afternoon .
T11	Relator 56 58	on
T12	Function 59 60	a
T13	Center 61 67	sunday
T14	Center 68 77	afternoon
T15	Participant 0 1	I
T16	Time 2 11	sometimes
T17	Process 12 14	go
T18	Participant 15 30	into this store
T19	Relator 15 19	into
T20	Elaborator 20 24	this
T21	Center 25 30	store
</div>
</td></tr></tbody>
</table>

### Participant advmod
<table id="047007-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-047007-0002
# text = I will never come here again.
1       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      4       nsubj   _ _
2       will    will    AUX     MD      VerbForm=Fin    4       aux     _   _
3       never   never   ADV     RB      _       4       advmod  _        _
4       come    come    VERB    VB      VerbForm=Inf    0       root    _  _
5       here    here    ADV     RB      PronType=Dem    4       advmod  _        _
6       again   again   ADV     RB      _       4       advmod  _        SpaceAfter=No
7       .       .       PUNCT   .       _       4       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
I will never come here again .
T2	ParallelScene 0 30	I will never come here again .
T3	Participant 0 1	I
T4	Function 2 6	will
T5	Time|Adverbial 7 12	never
T6	Process 13 17	come
T7	Participant 18 22	here
T8	Adverbial 23 28	again
</div>
</td></tr></tbody>
</table>

### Adverbial obl
<table id="307250-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-307250-0002
# text = Worst buffet period by far.
1       Worst   worst   ADJ     JJS     Degree=Sup      3       amod    _  _
2       buffet  buffet  NOUN    NN      Number=Sing     3       compound        _      _
3       period  period  NOUN    NN      Number=Sing     0       root    _  _
4       by      by      ADP     IN      _       5       case    _  _
5       far     far     ADV     RB      Degree=Pos      3       nmod    _       SpaceAfter=No
6       .       .       PUNCT   .       _       3       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Worst buffet period by far .
T2	ParallelScene 0 28	Worst buffet period by far .
T4	Adverbial 0 5	Worst
T5	Process 6 12	buffet
T6	Ground 13 19	period
T7	Adverbial 20 26	by far
</div>
</td></tr></tbody>
</table>

### Participant csubj
<table id="071518-0008">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-071518-0008
# text = And it was great that they did not charge a service fee to diagnose the problem - an added bonus!!
1       And     and     CCONJ   CC      _       4       cc      _    _
2       it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  4       expl    _  _
3       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   4       cop     _   _
4       great   great   ADJ     JJ      Degree=Pos      0       root    _  _
5       that    that    SCONJ   IN      _       9       mark    _  _
6       they    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      9       nsubj   _ _
7       did     do      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        9       aux     _   _
8       not     not     PART    RB      _       9       advmod  _        _
9       charge  charge  VERB    VB      VerbForm=Inf    4       csubj   _ _
10      a       a       DET     DT      Definite=Ind|PronType=Art       12      det     _  _
11      service service NOUN    NN      Number=Sing     12      compound        _     _
12      fee     fee     NOUN    NN      Number=Sing     9       obj     _    _
13      to      to      PART    TO      _       14      mark    _ _
14      diagnose        diagnose        VERB    VB      VerbForm=Inf    9       xcomp   _ _
15      the     the     DET     DT      Definite=Def|PronType=Art       16      det     _  _
16      problem problem NOUN    NN      Number=Sing     14      obj     _  _
17      -       -       PUNCT   ,       _       20      punct   _        _
18      an      a       DET     DT      Definite=Ind|PronType=Art       20      det     _  _
19      added   add     VERB    VBN     Tense=Past|VerbForm=Part        20      amod    _ _
20      bonus   bonus   NOUN    NN      Number=Sing     9       parataxis       _     SpaceAfter=No
21      !!      !!      PUNCT   .       _       20      punct   _        _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
And it was great that they did not charge a service fee to diagnose the problem - an added bonus !!
T2	Linker 0 3	And
T3	ParallelScene 4 99	it was great that they did not charge a service fee to diagnose the problem - an added bonus !!
T4	Function 4 6	it
T5	Function 7 10	was
T6	Adverbial 11 16	great
T7	Function 17 21	that
T8	Participant 22 26	they
R1	Participant parent:T13 child:T8
T9	Function 27 30	did
T10	Adverbial 31 34	not
T11	Process 35 41	charge
T12	Participant 42 55	a service fee
T13	Participant 56 79	to diagnose the problem
T14	Ground 82 96	an added bonus
T17	Relator 56 58	to
T18	Process 59 67	diagnose
T19	Participant 68 79	the problem
T20	Function 68 71	the
T21	Center 72 79	problem
T22	Function 42 43	a
T23	Elaborator 44 51	service
T24	Center 52 55	fee
T25	Process 44 51	service
</div>
</td></tr></tbody>
</table>

### Participant ccomp
<table id="245160-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-245160-0003
# text = i was looking for a car but did not really know what i wanted and they were very helpful and took the time to first figure out what my needs were and showing me various options to meet those needs.
1       i       i       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      3       nsubj   _        _
2       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   3       aux     _   _
3       looking look    VERB    VBG     VerbForm=Ger    0       root    _  _
4       for     for     ADP     IN      _       6       case    _  _
5       a       a       DET     DT      Definite=Ind|PronType=Art       6       det     _   _
6       car     car     NOUN    NN      Number=Sing     3       obl     _       _
7       but     but     CCONJ   CC      _       11      cc      _   _
8       did     do      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        11      aux     _  _
9       not     not     PART    RB      _       11      advmod  _       _
10      really  really  ADV     RB      _       11      advmod  _       _
11      know    know    VERB    VB      VerbForm=Inf    3       conj    _      _
12      what    what    PRON    WP      PronType=Int    14      obj     _  _
13      i       i       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      14      nsubj   _        _
14      wanted  want    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        11      ccomp   _        _
15      and     and     CCONJ   CC      _       19      cc      _   _
16      they    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      19      nsubj   _       _
17      were    be      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        19      cop     _  _
18      very    very    ADV     RB      _       19      advmod  _       _
19      helpful helpful ADJ     JJ      Degree=Pos      3       conj    _      _
20      and     and     CCONJ   CC      _       21      cc      _   _
21      took    take    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        19      conj    _     _
22      the     the     DET     DT      Definite=Def|PronType=Art       23      det     _  _
23      time    time    NOUN    NN      Number=Sing     21      obj     _  _
24      to      to      PART    TO      _       26      mark    _ _
25      first   first   ADV     RB      _       26      advmod  _       _
26      figure  figure  VERB    VB      VerbForm=Inf    21      advcl   _     _
27      out     out     ADP     RP      _       26      compound:prt    _ _
28      what    what    PRON    WP      PronType=Int    26      ccomp   _        _
29      my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      30      nmod:poss       _    _
30      needs   need    NOUN    NNS     Number=Plur     28      nsubj   _        _
31      were    be      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        28      cop     _  _
32      and     and     CCONJ   CC      _       33      cc      _   _
33      showing show    VERB    VBG     VerbForm=Ger    26      conj    _ _
34      me      I       PRON    PRP     Case=Acc|Number=Sing|Person=1|PronType=Prs      33      iobj    _ _
35      various various ADJ     JJ      Degree=Pos      36      amod    _ _
36      options option  NOUN    NNS     Number=Plur     33      obj     _  _
37      to      to      PART    TO      _       38      mark    _ _
38      meet    meet    VERB    VB      VerbForm=Inf    33      advcl   _     _
39      those   those   DET     DT      Number=Plur|PronType=Dem        40      det     _  _
40      needs   need    NOUN    NNS     Number=Plur     38      obj     _  SpaceAfter=No
41      .       .       PUNCT   .       _       3       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
i was looking for a car but did not really know what i wanted and they were very helpful and took the time to first figure out what my needs were and showing me various options to meet those needs .
T2	ParallelScene 0 23	i was looking for a car
T3	Linker 24 27	but
T4	ParallelScene 28 61	did not really know what i wanted
T5	Linker 62 65	and
T6	ParallelScene 66 88	they were very helpful
T7	Linker 89 92	and
T8	ParallelScene 93 198	took the time to first figure out what my needs were and showing me various options to meet those needs .
T11	Process 93 97	took
T12	Participant 98 198	the time to first figure out what my needs were and showing me various options to meet those needs .
T13	ParallelScene 98 145	the time to first figure out what my needs were
T14	Linker 146 149	and
T15	ParallelScene 150 198	showing me various options to meet those needs .
T16	Process 150 157	showing
T17	Participant 158 160	me
T18	Participant 161 198	various options to meet those needs .
T19	Elaborator 161 168	various
T20	Center 169 176	options
R1	Participant parent:T21 child:T20
T21	Elaborator 177 198	to meet those needs .
T22	Function 177 179	to
T23	Process 180 184	meet
T24	Participant 185 198	those needs .
T25	Elaborator 185 190	those
T26	Center 191 196	needs
T27	Time 98 106	the time
T28	Function 107 109	to
T29	Time 110 115	first
T30	Process 116 126	figure out
T31	Participant 127 145	what my needs were
T32	Participant 127 131	what
T33	Participant 132 134	my
T34	State 135 140	needs
T35	Function 141 145	were
T36	Function 98 101	the
T37	Center 102 106	time
T38	Participant 66 70	they
R2	Participant parent:T13 child:T38
R3	Participant parent:T15 child:T38
T39	Function 71 75	were
T40	Adverbial 76 80	very
T41	State 81 88	helpful
T42	Function 28 31	did
T43	Adverbial 32 35	not
T44	Adverbial 36 42	really
T45	Process 43 47	know
T46	Participant 48 61	what i wanted
T47	Participant 48 52	what
T48	Participant 53 54	i
T49	Process 55 61	wanted
T50	Participant 0 1	i
R4	Participant parent:T4 child:T50
T51	Function 2 5	was
T52	Process 6 13	looking
T53	Participant 14 23	for a car
T54	Relator 14 17	for
T55	Function 18 19	a
T56	Center 20 23	car
</div>
</td></tr></tbody>
</table>

### Participant xcomp
<table id="068436-0005">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-068436-0005
# text = I asked them to change it but they rudely said that it was okay.
1       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      2       nsubj   _ _
2       asked   ask     VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
3       them    they    PRON    PRP     Case=Acc|Number=Plur|Person=3|PronType=Prs      2       obj     _     _
4       to      to      PART    TO      _       5       mark    _  _
5       change  change  VERB    VB      VerbForm=Inf    2       xcomp   _ _
6       it      it      PRON    PRP     Case=Acc|Gender=Neut|Number=Sing|Person=3|PronType=Prs  5       obj     _   _
7       but     but     CCONJ   CC      _       10      cc      _   _
8       they    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      10      nsubj   _        _
9       rudely  rudely  ADV     RB      _       10      advmod  _       _
10      said    say     VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        2       conj    _      _
11      that    that    SCONJ   IN      _       14      mark    _ _
12      it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  14      nsubj   _        _
13      was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   14      cop     _  _
14      okay    okay    ADJ     JJ      Degree=Pos      10      ccomp   _        SpaceAfter=No
15      .       .       PUNCT   .       _       2       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
I asked them to change it but they rudely said that it was okay .
T2	ParallelScene 0 25	I asked them to change it
T3	Linker 26 29	but
T4	ParallelScene 30 65	they rudely said that it was okay .
T6	Participant 30 34	they
T7	Adverbial 35 41	rudely
T8	Process 42 46	said
T9	Participant 47 65	that it was okay .
T10	Relator 47 51	that
T11	Participant 52 54	it
T12	Function 55 58	was
T13	State 59 63	okay
T14	Participant 0 1	I
T15	Process 2 7	asked
T16	Participant 8 12	them
R1	Participant parent:T17 child:T16
T17	Participant 13 25	to change it
T18	Relator 13 15	to
T19	Process 16 22	change
T20	Participant 23 25	it
</div>
</td></tr></tbody>
</table>

### Unmatched xcomp
<table id="247226-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-247226-0004
# text = You have to bring in your own models and they have to pay for you to use them if you dont then you can graduate!
1       You     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  2       nsubj   _   _
2       have    have    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        0       root    _  _
3       to      to      PART    TO      _       4       mark    _  _
4       bring   bring   VERB    VB      VerbForm=Inf    2       xcomp   _ _
5       in      in      ADV     RB      _       4       advmod  _        _
6       your    you     PRON    PRP$    Person=2|Poss=Yes|PronType=Prs  8       nmod:poss       _     _
7       own     own     ADJ     JJ      Degree=Pos      8       amod    _  _
8       models  model   NOUN    NNS     Number=Plur     4       obj     _   _
9       and     and     CCONJ   CC      _       11      cc      _   _
10      they    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      11      nsubj   _ _
11      have    have    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        2       conj    _      _
12      to      to      PART    TO      _       13      mark    _ _
13      pay     pay     VERB    VB      VerbForm=Inf    11      xcomp   _        _
14      for     for     SCONJ   IN      _       17      mark    _ _
15      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  17      nsubj   _        _
16      to      to      PART    TO      _       17      mark    _ _
17      use     use     VERB    VB      VerbForm=Inf    13      advcl   _    _
18      them    they    PRON    PRP     Case=Acc|Number=Plur|Person=3|PronType=Prs      17      obj     _  _
19      if      if      SCONJ   IN      _       21      mark    _ _
20      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  21      nsubj   _        _
21      do      do      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        26      advcl   _     SpaceAfter=No
22      nt      not     PART    RB      _       21      advmod  _       _
23      then    then    ADV     RB      PronType=Dem    26      advmod  _       _
24      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  26      nsubj   _        _
25      can     can     AUX     MD      VerbForm=Fin    26      aux     _  _
26      graduate        graduate        VERB    VB      VerbForm=Inf    2       parataxis       _     SpaceAfter=No
27      !       !       PUNCT   .       _       2       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
You have to bring in your own models and they have to pay for you to use them if you do nt then you can graduate !
T2	ParallelScene 0 36	You have to bring in your own models
T3	Linker 37 40	and
T4	ParallelScene 41 77	they have to pay for you to use them
T5	Linker 78 80	if
T6	ParallelScene 81 90	you do nt
T7	Linker 91 95	then
T8	ParallelScene 96 114	you can graduate !
T10	Participant 96 99	you
T11	Adverbial 100 103	can
T12	Process 104 112	graduate
T13	Participant 81 84	you
T14	Function 85 87	do
T15	Adverbial 88 90	nt
R1	Adverbial parent:T8 child:T15
T16	Participant 41 45	they
T17	Adverbial 46 53	have to
T18	Process 54 57	pay
R2	Process parent:T6 child:T18
T19	Participant 58 77	for you to use them
T20	Relator 58 61	for
T21	Participant 62 65	you
T22	Function 66 68	to
T23	Process 69 72	use
T24	Participant 73 77	them
T25	Center 46 50	have
T26	Function 51 53	to
T27	Participant 0 3	You
T28	Adverbial 4 11	have to
T29	Process 12 17	bring
T30	Adverbial 18 20	in
T31	Participant 21 36	your own models
T32	Elaborator 21 29	your own
T33	Center 30 36	models
R3	Participant parent:T32 child:T33
T34	State 21 25	your
T35	Adverbial 26 29	own
T36	Center 4 8	have
T37	Function 9 11	to
</div>
</td></tr></tbody>
</table>


### State xcomp
<table id="254908-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-254908-0002
# text = The price they gave was good so I said hey this seems great.
1       The     the     DET     DT      Definite=Def|PronType=Art       2       det     _   _
2       price   price   NOUN    NN      Number=Sing     6       nsubj   _ _
3       they    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      4       nsubj   _ _
4       gave    give    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        2       acl:relcl       _     _
5       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   6       cop     _   _
6       good    good    ADJ     JJ      Degree=Pos      0       root    _  _
7       so      so      ADV     RB      _       9       mark    _  _
8       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      9       nsubj   _ _
9       said    say     VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        6       advcl   _      _
10      hey     hey     INTJ    UH      _       12      discourse       _    _
11      this    this    PRON    DT      Number=Sing|PronType=Dem        12      nsubj   _ _
12      seems   seem    VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   9       ccomp   _ _
13      great   great   ADJ     JJ      Degree=Pos      12      xcomp   _        SpaceAfter=No
14      .       .       PUNCT   .       _       6       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
The price they gave was good so I said hey this seems great .
T2	ParallelScene 0 28	The price they gave was good
T3	Linker 29 31	so
T4	ParallelScene 32 61	I said hey this seems great .
T6	Participant 32 33	I
T7	Process 34 38	said
T8	Participant 39 61	hey this seems great .
T9	Function 39 42	hey
T10	Participant 43 47	this
T11	Ground 48 53	seems
T12	State 54 59	great
T13	Participant 0 19	The price they gave
T14	Function 20 23	was
T15	State 24 28	good
T16	Function 0 3	The
T17	Center 4 9	price
R1	Participant parent:T18 child:T17
T18	Elaborator 10 19	they gave
T19	Participant 10 14	they
T20	Process 15 19	gave
</div>
</td></tr></tbody>
</table>

### Function aux
<table id="105518-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-105518-0004
# text = If you are on the lookout for a pure breed pup don't forget to check out the shelters!
1       If      if      SCONJ   IN      _       6       mark    _  _
2       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  6       nsubj   _ _
3       are     be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        6       cop     _   _
4       on      on      ADP     IN      _       6       case    _  _
5       the     the     DET     DT      Definite=Def|PronType=Art       6       det     _   _
6       lookout lookout NOUN    NN      Number=Sing     14      advcl   _     _
7       for     for     ADP     IN      _       11      case    _ _
8       a       a       DET     DT      Definite=Ind|PronType=Art       11      det     _  _
9       pure    pure    ADJ     JJ      Degree=Pos      10      amod    _ _
10      breed   breed   NOUN    NN      Number=Sing     11      compound        _     _
11      pup     pup     NOUN    NN      Number=Sing     6       nmod    _      _
12      do      do      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        14      aux     _  SpaceAfter=No
13      n't     not     PART    RB      _       14      advmod  _       _
14      forget  forget  VERB    VB      Mood=Imp|VerbForm=Fin   0       root    _  _
15      to      to      PART    TO      _       16      mark    _ _
16      check   check   VERB    VB      VerbForm=Inf    14      xcomp   _        _
17      out     out     ADP     RP      _       16      compound:prt    _ _
18      the     the     DET     DT      Definite=Def|PronType=Art       19      det     _  _
19      shelters        shelter NOUN    NNS     Number=Plur     16      obj     _  SpaceAfter=No
20      !       !       PUNCT   .       _       14      punct   _        _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
If you are on the lookout for a pure breed pup do n't forget to check out the shelters !
T2	Linker 0 2	If
T3	ParallelScene 3 46	you are on the lookout for a pure breed pup
T4	ParallelScene 47 88	do n't forget to check out the shelters !
T6	Function 47 49	do
T7	Adverbial 50 53	n't
T8	Adverbial 54 60	forget
T9	Function 61 63	to
T10	Process 64 73	check out
T11	Participant 74 88	the shelters !
T12	Function 74 77	the
T13	Center 78 86	shelters
T14	Participant 3 6	you
R1	Participant parent:T4 child:T14
T15	Function 7 10	are
T16	Process 11 25	on the lookout
T17	Participant 26 46	for a pure breed pup
T18	Relator 26 29	for
T19	Function 30 31	a
T20	Elaborator 32 42	pure breed
T21	Center 43 46	pup
T22	Elaborator 32 36	pure
T23	Center 37 42	breed
</div>
</td></tr></tbody>
</table>

### Adverbial aux
<table id="247226-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-247226-0004
# text = You have to bring in your own models and they have to pay for you to use them if you dont then you can graduate!
1       You     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  2       nsubj   _   _
2       have    have    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        0       root    _  _
3       to      to      PART    TO      _       4       mark    _  _
4       bring   bring   VERB    VB      VerbForm=Inf    2       xcomp   _ _
5       in      in      ADV     RB      _       4       advmod  _        _
6       your    you     PRON    PRP$    Person=2|Poss=Yes|PronType=Prs  8       nmod:poss       _     _
7       own     own     ADJ     JJ      Degree=Pos      8       amod    _  _
8       models  model   NOUN    NNS     Number=Plur     4       obj     _   _
9       and     and     CCONJ   CC      _       11      cc      _   _
10      they    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      11      nsubj   _ _
11      have    have    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        2       conj    _      _
12      to      to      PART    TO      _       13      mark    _ _
13      pay     pay     VERB    VB      VerbForm=Inf    11      xcomp   _        _
14      for     for     SCONJ   IN      _       17      mark    _ _
15      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  17      nsubj   _        _
16      to      to      PART    TO      _       17      mark    _ _
17      use     use     VERB    VB      VerbForm=Inf    13      advcl   _    _
18      them    they    PRON    PRP     Case=Acc|Number=Plur|Person=3|PronType=Prs      17      obj     _  _
19      if      if      SCONJ   IN      _       21      mark    _ _
20      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  21      nsubj   _        _
21      do      do      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        26      advcl   _     SpaceAfter=No
22      nt      not     PART    RB      _       21      advmod  _       _
23      then    then    ADV     RB      PronType=Dem    26      advmod  _       _
24      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  26      nsubj   _        _
25      can     can     AUX     MD      VerbForm=Fin    26      aux     _  _
26      graduate        graduate        VERB    VB      VerbForm=Inf    2       parataxis       _     SpaceAfter=No
27      !       !       PUNCT   .       _       2       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
You have to bring in your own models and they have to pay for you to use them if you do nt then you can graduate !
T2	ParallelScene 0 36	You have to bring in your own models
T3	Linker 37 40	and
T4	ParallelScene 41 77	they have to pay for you to use them
T5	Linker 78 80	if
T6	ParallelScene 81 90	you do nt
T7	Linker 91 95	then
T8	ParallelScene 96 114	you can graduate !
T10	Participant 96 99	you
T11	Adverbial 100 103	can
T12	Process 104 112	graduate
T13	Participant 81 84	you
T14	Function 85 87	do
T15	Adverbial 88 90	nt
R1	Adverbial parent:T8 child:T15
T16	Participant 41 45	they
T17	Adverbial 46 53	have to
T18	Process 54 57	pay
R2	Process parent:T6 child:T18
T19	Participant 58 77	for you to use them
T20	Relator 58 61	for
T21	Participant 62 65	you
T22	Function 66 68	to
T23	Process 69 72	use
T24	Participant 73 77	them
T25	Center 46 50	have
T26	Function 51 53	to
T27	Participant 0 3	You
T28	Adverbial 4 11	have to
T29	Process 12 17	bring
T30	Adverbial 18 20	in
T31	Participant 21 36	your own models
T32	Elaborator 21 29	your own
T33	Center 30 36	models
R3	Participant parent:T32 child:T33
T34	State 21 25	your
T35	Adverbial 26 29	own
T36	Center 4 8	have
T37	Function 9 11	to
</div>
</td></tr></tbody>
</table>

## Multi-Word Expressions
### Elaborator compound
<table id="241739-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-241739-0002
# text = Firstly, the other reviewer clearly has never been to Nick's, or he would know that Nick only charges $13 for a haircut which is pretty much industry standard.
1       Firstly firstly ADV     RB      _       11      advmod  _       SpaceAfter=No
2       ,       ,       PUNCT   ,       _       11      punct   _        _
3       the     the     DET     DT      Definite=Def|PronType=Art       5       det     _   _
4       other   other   ADJ     JJ      Degree=Pos      5       amod    _  _
5       reviewer        reviewer        NOUN    NN      Number=Sing     11      nsubj   _        _
6       clearly clearly ADV     RB      _       11      advmod  _       _
7       has     have    AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   11      aux     _  _
8       never   never   ADV     RB      _       11      advmod  _       _
9       been    be      AUX     VBN     Tense=Past|VerbForm=Part        11      cop     _  _
10      to      to      ADP     IN      _       11      case    _ _
11      Nick    Nick    PROPN   NNP     Number=Sing     0       root    _  SpaceAfter=No
12      's      's      PART    POS     _       11      case    _ SpaceAfter=No
13      ,       ,       PUNCT   ,       _       17      punct   _        _
14      or      or      CCONJ   CC      _       17      cc      _   _
15      he      he      PRON    PRP     Case=Nom|Gender=Masc|Number=Sing|Person=3|PronType=Prs  17      nsubj   _        _
16      would   would   AUX     MD      VerbForm=Fin    17      aux     _  _
17      know    know    VERB    VB      VerbForm=Inf    11      conj    _      _
18      that    that    SCONJ   IN      _       21      mark    _ _
19      Nick    Nick    PROPN   NNP     Number=Sing     21      nsubj   _        _
20      only    only    ADV     RB      _       21      advmod  _       _
21      charges charge  VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   17      ccomp   _        _
22      $       $       SYM     $       _       21      obj     _  SpaceAfter=No
23      13      13      NUM     CD      NumType=Card    22      nummod  _       _
24      for     for     ADP     IN      _       26      case    _ _
25      a       a       DET     DT      Definite=Ind|PronType=Art       26      det     _  _
26      haircut haircut NOUN    NN      Number=Sing     21      obl     _      _
27      which   which   PRON    WDT     PronType=Int    32      nsubj   _        _
28      is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   32      cop     _  _
29      pretty  pretty  ADV     RB      _       30      advmod  _       _
30      much    much    ADV     RB      _       32      advmod  _       _
31      industry        industry        NOUN    NN      Number=Sing     32      compound        _     _
32      standard        standard        NOUN    NN      Number=Sing     21      parataxis       _    SpaceAfter=No
33      .       .       PUNCT   .       _       11      punct   _        _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
Firstly , the other reviewer clearly has never been to Nick 's , or he would know that Nick only charges $ 13 for a haircut which is pretty much industry standard .
T2	Linker 0 7	Firstly
T3	ParallelScene 10 62	the other reviewer clearly has never been to Nick 's
T4	Linker 65 67	or
T5	ParallelScene 68 123	he would know that Nick only charges $ 13 for a haircut
T6	Linker 124 129	which
T7	ParallelScene 130 164	is pretty much industry standard .
T11	Function 130 132	is
T12	Adverbial 133 144	pretty much
T13	Participant 145 153	industry
T14	State 154 162	standard
T15	Participant 68 70	he
T16	Adverbial 71 76	would
T17	Process 77 81	know
T18	Participant 82 123	that Nick only charges $ 13 for a haircut
T19	Relator 82 86	that
T20	Participant 87 91	Nick
T21	Adverbial 92 96	only
T22	Process 97 104	charges
T23	Participant 105 123	$ 13 for a haircut
T24	Participant 105 109	$ 13
R1	Participant parent:T7 child:T24
T25	Function 110 113	for
T26	Process 114 123	a haircut
T27	Function 114 115	a
T28	Center 116 123	haircut
T29	Quantifier 105 109	$ 13
T30	Participant 10 28	the other reviewer
T31	Ground 29 36	clearly
T32	Function 37 40	has
T33	Adverbial|Time 41 46	never
T34	Process 47 51	been
T35	Participant 52 62	to Nick 's
T36	Relator 52 54	to
T37	Center 55 59	Nick
T38	Relator 60 62	's
T39	Function 10 13	the
T40	Elaborator 14 19	other
T41	Center 20 28	reviewer
</div>
</td></tr></tbody>
</table>

<table id="070730-0006">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-070730-0006
# text = The service is solicitous, the atmosphere is nice and mod except the out-of-place flat-screen TV playing football.
1       The     the     DET     DT      Definite=Def|PronType=Art       2       det     _   _
2       service service NOUN    NN      Number=Sing     4       nsubj   _ _
3       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   4       cop     _   _
4       solicitous      solicitous      ADJ     JJ      Degree=Pos      0       root    _  SpaceAfter=No
5       ,       ,       PUNCT   ,       _       4       punct   _ _
6       the     the     DET     DT      Definite=Def|PronType=Art       7       det     _   _
7       atmosphere      atmosphere      NOUN    NN      Number=Sing     9       nsubj   _        _
8       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   9       cop     _   _
9       nice    nice    ADJ     JJ      Degree=Pos      4       list    _  _
10      and     and     CCONJ   CC      _       11      cc      _   _
11      mod     mod     ADJ     JJ      Degree=Pos      9       conj    _      _
12      except  except  ADP     IN      _       22      case    _ _
13      the     the     DET     DT      Definite=Def|PronType=Art       22      det     _  _
14      out     out     ADP     IN      _       22      compound        _     SpaceAfter=No
15      -       -       PUNCT   HYPH    _       14      punct   _        SpaceAfter=No
16      of      of      ADP     IN      _       18      case    _ SpaceAfter=No
17      -       -       PUNCT   HYPH    _       18      punct   _        SpaceAfter=No
18      place   place   NOUN    NN      Number=Sing     14      nmod    _      _
19      flat    flat    ADJ     JJ      Degree=Pos      21      amod    _ SpaceAfter=No
20      -       -       PUNCT   HYPH    _       21      punct   _        SpaceAfter=No
21      screen  screen  NOUN    NN      Number=Sing     22      compound        _     _
22      TV      tv      NOUN    NN      Number=Sing     9       obl     _    _
23      playing play    VERB    VBG     VerbForm=Ger    22      acl     _  _
24      football        football        NOUN    NN      Number=Sing     23      obj     _  SpaceAfter=No
25      .       .       PUNCT   .       _       4       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
The service is solicitous , the atmosphere is nice and mod except the out - of - place flat - screen TV playing football .
T2	ParallelScene 0 25	The service is solicitous
T3	ParallelScene 28 58	the atmosphere is nice and mod
T4	Linker 59 65	except
T5	ParallelScene 66 122	the out - of - place flat - screen TV playing football .
T8	Participant 66 103	the out - of - place flat - screen TV
T9	Process 104 111	playing
T10	Participant 112 120	football
T11	Function 66 69	the
T12	Elaborator 70 86	out - of - place
T13	Elaborator 87 100	flat - screen
T14	Center 101 103	TV
R1	Participant parent:T12 child:T14
T15	Elaborator 87 91	flat
T16	Center 94 100	screen
T18	State 70 86	out - of - place
T19	Relator 70 73	out
T20	Function 76 78	of
T21	Center 81 86	place
T24	Process 28 42	the atmosphere
T25	Function 43 45	is
T26	Adverbial 46 58	nice and mod
T27	Center 46 50	nice
T28	Connector 51 54	and
T29	Center 55 58	mod
T30	Function 28 31	the
T31	Center 32 42	atmosphere
T32	Process 0 11	The service
T33	Function 12 14	is
T34	Adverbial 15 25	solicitous
T35	Function 0 3	The
T36	Center 4 11	service
</div>
</td></tr></tbody>
</table>

### Unmatched compound
<table id="081796-0005">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-081796-0005
# text = The mark up is minimal considering that the clothing is hard to find and often shipped for Europe.
1       The     the     DET     DT      Definite=Def|PronType=Art       3       det     _   _
2       mark    mark    NOUN    NN      Number=Sing     3       compound        _      _
3       up      up      NOUN    NN      Number=Sing     5       nsubj   _ _
4       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   5       cop     _   _
5       minimal minimal ADJ     JJ      Degree=Pos      0       root    _  _
6       considering     consider        VERB    VBG     VerbForm=Ger    5       advcl   _ _
7       that    that    SCONJ   IN      _       11      mark    _ _
8       the     the     DET     DT      Definite=Def|PronType=Art       9       det     _   _
9       clothing        clothing        NOUN    NN      Number=Sing     11      nsubj:pass      _     _
10      is      be      VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   11      aux:pass        _     _
11      hard    hard    ADJ     JJ      Degree=Pos      6       ccomp   _ _
12      to      to      PART    TO      _       13      mark    _ _
13      find    find    VERB    VB      VerbForm=Inf    11      ccomp   _        _
14      and     and     CCONJ   CC      _       16      cc      _   _
15      often   often   ADV     RB      _       16      advmod  _       _
16      shipped ship    VERB    VBN     Tense=Past|VerbForm=Part        11      conj    _     _
17      for     for     ADP     IN      _       18      case    _ _
18      Europe  Europe  PROPN   NNP     Number=Sing     16      obl     _      SpaceAfter=No
19      .       .       PUNCT   .       _       5       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
The mark up is minimal considering that the clothing is hard to find and often shipped for Europe .
T2	ParallelScene 0 22	The mark up is minimal
T3	Linker 23 39	considering that
T4	ParallelScene 40 68	the clothing is hard to find
T5	Linker 69 72	and
T6	ParallelScene 73 99	often shipped for Europe .
T8	Time 73 78	often
T9	Process 79 86	shipped
T10	Participant 87 99	for Europe .
T11	Relator 87 90	for
T12	Center 91 97	Europe
T13	Participant 40 52	the clothing
T14	Function 53 55	is
T15	Adverbial 56 60	hard
T16	Function 61 63	to
T17	Process 64 68	find
T18	Function 40 43	the
T19	Center 44 52	clothing
R1	Participant parent:T6 child:T19
T20	Process 0 11	The mark up
T21	Function 12 14	is
T22	Adverbial 15 22	minimal
T23	Function 0 3	The
T24	Center 4 11	mark up
</div>
</td></tr></tbody>
</table>

<table id="363685-0020">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-363685-0020
# text = If you go later, it's all cleaned up.
1       If      if      SCONJ   IN      _       3       mark    _  _
2       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  3       nsubj   _ _
3       go      go      VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        9       advcl   _      _
4       later   later   ADV     RBR     Degree=Cmp      3       advmod  _        SpaceAfter=No
5       ,       ,       PUNCT   ,       _       9       punct   _ _
6       it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  9       nsubj:pass      _    SpaceAfter=No
7       's      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   9       aux:pass        _      _
8       all     all     ADV     RB      _       9       advmod  _        _
9       cleaned clean   VERB    VBN     Tense=Past|VerbForm=Part|Voice=Pass     0       root    _  _
10      up      up      ADP     RP      _       9       compound:prt    _  SpaceAfter=No
11      .       .       PUNCT   .       _       9       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
If you go later , it 's all cleaned up .
T2	Linker 0 2	If
T3	ParallelScene 3 15	you go later
T4	ParallelScene 18 40	it 's all cleaned up .
T6	Participant 18 20	it
T7	Function 21 23	's
T8	Adverbial 24 27	all
T9	Process 28 38	cleaned up
T10	Participant 3 6	you
T11	Process 7 9	go
T12	Time 10 15	later
</div>
</td></tr></tbody>
</table>

### Participant compound
<table id="247097-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-247097-0003
# text = Before treatment, my food cravings were "out of control" which caused me to be stressed out.
1       Before  before  ADP     IN      _       2       case    _  _
2       treatment       treatment       NOUN    NN      Number=Sing     11      obl     _   SpaceAfter=No
3       ,       ,       PUNCT   ,       _       11      punct   _        _
4       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      6       nmod:poss       _     _
5       food    food    NOUN    NN      Number=Sing     6       compound        _      _
6       cravings        craving NOUN    NNS     Number=Plur     11      nsubj   _        _
7       were    be      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        11      cop     _  _
8       "       "       PUNCT   ``      _       11      punct   _        SpaceAfter=No
9       out     out     ADP     IN      _       11      case    _ _
10      of      of      ADP     IN      _       11      case    _ _
11      control control NOUN    NN      Number=Sing     0       root    _  SpaceAfter=No
12      "       "       PUNCT   ''      _       11      punct   _        _
13      which   which   PRON    WDT     PronType=Int    14      nsubj   _        _
14      caused  cause   VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        11      parataxis       _    _
15      me      I       PRON    PRP     Case=Acc|Number=Sing|Person=1|PronType=Prs      14      obj     _   _
16      to      to      PART    TO      _       18      mark    _ _
17      be      be      AUX     VB      VerbForm=Inf    18      aux:pass        _     _
18      stressed        stress  VERB    VBN     Tense=Past|VerbForm=Part        14      xcomp   _        _
19      out     out     ADP     RP      _       18      compound:prt    _ SpaceAfter=No
20      .       .       PUNCT   .       _       11      punct   _        _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
Before treatment , my food cravings were " out of control " which caused me to be stressed out .
T2	Linker 0 6	Before
T3	ParallelScene 7 16	treatment
T4	ParallelScene 19 57	my food cravings were " out of control
T5	Linker 60 65	which
T6	ParallelScene 66 96	caused me to be stressed out .
T10	Adverbial 66 72	caused
T11	Participant 73 75	me
T12	Function 76 78	to
T13	State 79 96	be stressed out .
T14	Function 79 81	be
T15	Center 82 94	stressed out
T16	Participant 19 35	my food cravings
T17	Function 36 40	were
T18	State 43 57	out of control
T20	Function 43 46	out
T21	Relator 47 49	of
T22	Center 50 57	control
T23	Participant 19 21	my
T24	Participant 22 26	food
T25	Process 27 35	cravings
R1	Participant parent:T6 child:T25
T26	Process 7 16	treatment
</div>
</td></tr></tbody>
</table>

### Adverbial compound
<table id="095040-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-095040-0002
# text = As first-time home buyers, my husband and I found Stephanie Fairchild at Prudential Steamboat Realty, extremely helpful.
1       As      as      ADP     IN      _       6       case    _  _
2       first   first   ADJ     JJ      Degree=Pos|NumType=Ord  4       amod    _  SpaceAfter=No
3       -       -       PUNCT   HYPH    _       4       punct   _ SpaceAfter=No
4       time    time    NOUN    NN      Number=Sing     6       compound        _      _
5       home    home    NOUN    NN      Number=Sing     6       compound        _      _
6       buyers  buyer   NOUN    NNS     Number=Plur     12      obl     _       SpaceAfter=No
7       ,       ,       PUNCT   ,       _       12      punct   _        _
8       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      9       nmod:poss       _     _
9       husband husband NOUN    NN      Number=Sing     12      nsubj   _        _
10      and     and     CCONJ   CC      _       11      cc      _   _
11      I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      9       conj    _     _
12      found   find    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
13      Stephanie       Stephanie       PROPN   NNP     Number=Sing     12      obj     _   _
14      Fairchild       Fairchild       PROPN   NNP     Number=Sing     13      flat    _ _
15      at      at      ADP     IN      _       18      case    _ _
16      Prudential      Prudential      PROPN   NNP     Number=Sing     18      compound        _     _
17      Steamboat       Steamboat       PROPN   NNP     Number=Sing     18      compound        _     _
18      Realty  Realty  PROPN   NNP     Number=Sing     13      nmod    _      SpaceAfter=No
19      ,       ,       PUNCT   ,       _       21      punct   _        _
20      extremely       extremely       ADV     RB      _       21      advmod  _       _
21      helpful helpful ADJ     JJ      Degree=Pos      12      xcomp   _        SpaceAfter=No
22      .       .       PUNCT   .       _       12      punct   _        _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
As first - time home buyers , my husband and I found Stephanie Fairchild at Prudential Steamboat Realty , extremely helpful .
T2	Linker 0 2	As
T3	ParallelScene 3 27	first - time home buyers
T4	ParallelScene 30 125	my husband and I found Stephanie Fairchild at Prudential Steamboat Realty , extremely helpful .
T7	Participant 30 46	my husband and I
T8	Adverbial 47 52	found
T9	Participant 53 103	Stephanie Fairchild at Prudential Steamboat Realty
T10	Adverbial 106 115	extremely
T11	State 116 123	helpful
T13	Center 53 72	Stephanie Fairchild
T14	Elaborator 73 103	at Prudential Steamboat Realty
T15	Relator 73 75	at
T16	Center 76 103	Prudential Steamboat Realty
T17	Center 30 40	my husband
T18	Connector 41 44	and
T19	Center 45 46	I
T20	Participant 30 32	my
T21	Participant|State 33 40	husband
T23	Adverbial 3 15	first - time
T24	Participant 16 20	home
T25	Process 21 27	buyers
T26	Quantifier 3 8	first
T27	Center 11 15	time
</div>
</td></tr></tbody>
</table>


### Unmatched obj
<table id="114941-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-114941-0001
# text = Give them a try!
1       Give    give    VERB    VB      Mood=Imp|VerbForm=Fin   0       root    _  _
2       them    they    PRON    PRP     Case=Acc|Number=Plur|Person=3|PronType=Prs      1       iobj    _  _
3       a       a       DET     DT      Definite=Ind|PronType=Art       4       det     _   _
4       try     try     NOUN    NN      Number=Sing     1       obj     _   SpaceAfter=No
5       !       !       PUNCT   .       _       1       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Give them a try !
T2	ParallelScene 0 17	Give them a try !
T5	Process 0 4;10 17	Give a try !
T6	Participant 5 9	them
T7	Function 0 4	Give
T8	Function 10 11	a
T9	Center 12 15	try
</div>
</td></tr></tbody>
</table>

<table id="024385-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-024385-0001
# text = Another great business bites the dust!
1       Another another DET     DT      _       3       det     _   _
2       great   great   ADJ     JJ      Degree=Pos      3       amod    _  _
3       business        business        NOUN    NN      Number=Sing     4       nsubj   _ _
4       bites   bite    VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   0       root    _  _
5       the     the     DET     DT      Definite=Def|PronType=Art       6       det     _   _
6       dust    dust    NOUN    NN      Number=Sing     4       obj     _   SpaceAfter=No
7       !       !       PUNCT   .       _       4       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Another great business bites the dust !
T2	ParallelScene 0 39	Another great business bites the dust !
T4	Participant 0 22	Another great business
T5	Process 23 37	bites the dust
T6	Elaborator 0 7	Another
T7	Elaborator 8 13	great
T8	Center 14 22	business
R1	Participant parent:T7 child:T8
T9	State 8 13	great
</div>
</td></tr></tbody>
</table>

### Unmatched advcl
<table id="345455-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-345455-0003
# text = I'ma soccer mom so I wasn't sure what I was looking for when it comes to dancewear.
1       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      5       nsubj   _ SpaceAfter=No
2       'm      be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        5       cop     _   SpaceAfter=No
3       a       a       DET     DT      Definite=Ind|PronType=Art       5       det     _   _
4       soccer  soccer  NOUN    NN      Number=Sing     5       compound        _      _
5       mom     mom     NOUN    NN      Number=Sing     0       root    _  _
6       so      so      ADV     RB      _       10      advmod  _       _
7       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      10      nsubj   _        _
8       was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   10      cop     _  SpaceAfter=No
9       n't     not     PART    RB      _       10      advmod  _       _
10      sure    sure    ADJ     JJ      Degree=Pos      5       conj    _  _
11      what    what    PRON    WP      PronType=Int    14      obl     _      _
12      I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      14      nsubj   _        _
13      was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   14      aux     _  _
14      looking look    VERB    VBG     VerbForm=Ger    10      ccomp   _        _
15      for     for     ADP     IN      _       11      case    _ _
16      when    when    ADV     WRB     PronType=Int    18      mark    _ _
17      it      it      PRON    PRP     Case=Nom|Gender=Neut|Number=Sing|Person=3|PronType=Prs  18      nsubj   _        _
18      comes   come    VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   14      advcl   _   _
19      to      to      ADP     IN      _       20      case    _ _
20      dancewear       dancewear       NOUN    NN      Number=Sing     18      obl     _       SpaceAfter=No
21      .       .       PUNCT   .       _       5       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
I 'm a soccer mom so I was n't sure what I was looking for when it comes to dancewear .
T2	ParallelScene 0 17	I 'm a soccer mom
T3	Linker 18 20	so
T4	ParallelScene 21 87	I was n't sure what I was looking for when it comes to dancewear .
T6	Participant 21 22	I
T7	Function 23 26	was
T8	Adverbial 27 30	n't
T9	State 31 35	sure
T10	Participant 36 87	what I was looking for when it comes to dancewear .
T11	Participant 36 40;55 58	what for
T12	Participant 41 42	I
T13	Function 43 46	was
T14	Process 47 54	looking
T15	Participant 59 87	when it comes to dancewear .
T16	Relator 59 75	when it comes to
T17	Center 76 85	dancewear
T18	Center 36 40	what
T19	Relator 55 58	for
T20	Participant 0 1	I
T21	Function 2 4	'm
T22	State 5 6;14 17	a mom
T23	Participant 7 13	soccer
T24	Function 5 6	a
T25	Center 14 17	mom
</div>
</td></tr></tbody>
</table>

## Linkage
### Head selection
<table id="052884-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-052884-0001
# text = unique gifts and cards
1       unique  unique  ADJ     JJ      Degree=Pos      2       amod    _  _
2       gifts   gift    NOUN    NNS     Number=Plur     0       root    _  _
3       and     and     CCONJ   CC      _       4       cc      _    _
4       cards   card    NOUN    NNS     Number=Plur     2       conj    _      _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
unique gifts and cards
T2	ParallelScene 0 22	unique gifts and cards
T3	State 0 6	unique
T4	Participant 7 22	gifts and cards
T5	Center 7 12	gifts
T6	Connector 13 16	and
T7	Center 17 22	cards
</div>
</td></tr></tbody>
</table>

### Parallel Scene advcl
<table id="084373-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-084373-0003
# text = We called few companies before we decide to hire them.
1       We      we      PRON    PRP     Case=Nom|Number=Plur|Person=1|PronType=Prs      2       nsubj   _ _
2       called  call    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        0       root    _  _
3       few     few     ADJ     JJ      Degree=Pos      4       amod    _  _
4       companies       company NOUN    NNS     Number=Plur     2       obj     _   _
5       before  before  SCONJ   IN      _       7       mark    _  _
6       we      we      PRON    PRP     Case=Nom|Number=Plur|Person=1|PronType=Prs      7       nsubj   _   _
7       decide  decide  VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        2       advcl   _  _
8       to      to      PART    TO      _       9       mark    _  _
9       hire    hire    VERB    VB      VerbForm=Inf    7       xcomp   _ _
10      them    they    PRON    PRP     Case=Acc|Number=Plur|Person=3|PronType=Prs      9       obj     _   SpaceAfter=No
11      .       .       PUNCT   .       _       2       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
We called few companies before we decide to hire them .
T2	ParallelScene 0 23	We called few companies
T3	Linker 24 30	before
T4	ParallelScene 31 55	we decide to hire them .
T6	Participant 31 33	we
R1	Participant parent:T8 child:T6
T7	Process 34 40	decide
T8	Participant 41 55	to hire them .
T9	Function 41 43	to
T10	Process 44 48	hire
T11	Participant 49 53	them
T12	Participant 0 2	We
T13	Process 3 9	called
T14	Participant 10 23	few companies
T15	Quantifier 10 13	few
T16	Center 14 23	companies
</div>
</td></tr></tbody>
</table>

### Parallel Scene parataxis
<table id="069995-0007">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-069995-0007
# text = Check out The Willow Lounge, youll be happy!
1       Check   check   VERB    VB      Mood=Imp|VerbForm=Fin   0       root    _  _
2       out     out     ADP     RP      _       1       compound:prt    _  _
3       The     the     DET     DT      Definite=Def|PronType=Art       5       det     _   _
4       Willow  Willow  PROPN   NNP     Number=Sing     5       compound        _      _
5       Lounge  Lounge  PROPN   NNP     Number=Sing     1       obj     _   SpaceAfter=No
6       ,       ,       PUNCT   ,       _       1       punct   _ _
7       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  10      nsubj   _        SpaceAfter=No
8       ll      will    AUX     MD      VerbForm=Fin    10      aux     _  _
9       be      be      AUX     VB      VerbForm=Inf    10      cop     _  _
10      happy   happy   ADJ     JJ      Degree=Pos      1       parataxis       _     SpaceAfter=No
11      !       !       PUNCT   .       _       1       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Check out The Willow Lounge , you ll be happy !
T2	ParallelScene 0 27	Check out The Willow Lounge
T3	ParallelScene 30 47	you ll be happy !
T5	Participant 30 33	you
T6	Function 34 36	ll
T7	Function 37 39	be
T8	State 40 45	happy
T11	Process 0 9	Check out
T12	Participant 10 27	The Willow Lounge
T13	Function 10 13	The
T14	Center 14 27	Willow Lounge
</div>
</td></tr></tbody>
</table>

### Linker wh-pronoun
<table id="083454-0001">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-083454-0001
# text = I didn't end up buying my car here, but I did think the guy who worked with me was pretty cool - he was willing to budge a little on the price which means a lot to me.
1       I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      4       nsubj   _   _
2       did     do      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        4       aux     _   SpaceAfter=No
3       n't     not     PART    RB      _       4       advmod  _        _
4       end     end     VERB    VB      VerbForm=Inf    0       root    _  _
5       up      up      ADP     RP      _       4       compound:prt    _  _
6       buying  buy     VERB    VBG     VerbForm=Ger    4       xcomp   _ _
7       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      8       nmod:poss       _     _
8       car     car     NOUN    NN      Number=Sing     6       obj     _   _
9       here    here    ADV     RB      PronType=Dem    6       advmod  _        SpaceAfter=No
10      ,       ,       PUNCT   ,       _       14      punct   _        _
11      but     but     CCONJ   CC      _       14      cc      _   _
12      I       I       PRON    PRP     Case=Nom|Number=Sing|Person=1|PronType=Prs      14      nsubj   _        _
13      did     do      AUX     VBD     Mood=Ind|Tense=Past|VerbForm=Fin        14      aux     _  _
14      think   think   VERB    VB      VerbForm=Inf    4       conj    _      _
15      the     the     DET     DT      Definite=Def|PronType=Art       16      det     _  _
16      guy     guy     NOUN    NN      Number=Sing     23      nsubj   _       _
17      who     who     PRON    WP      PronType=Rel    18      nsubj   _  _
18      worked  work    VERB    VBD     Mood=Ind|Tense=Past|VerbForm=Fin        16      acl:relcl       _    _
19      with    with    ADP     IN      _       20      case    _ _
20      me      I       PRON    PRP     Case=Acc|Number=Sing|Person=1|PronType=Prs      18      obl     _     _
21      was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   23      cop     _  _
22      pretty  pretty  ADV     RB      _       23      advmod  _       _
23      cool    cool    ADJ     JJ      Degree=Pos      14      ccomp   _        _
24      -       -       PUNCT   ,       _       4       punct   _ _
25      he      he      PRON    PRP     Case=Nom|Gender=Masc|Number=Sing|Person=3|PronType=Prs  27      nsubj   _ _
26      was     be      AUX     VBD     Mood=Ind|Number=Sing|Person=3|Tense=Past|VerbForm=Fin   27      cop     _  _
27      willing willing ADJ     JJ      Degree=Pos      14      parataxis       _    _
28      to      to      PART    TO      _       29      mark    _ _
29      budge   budge   VERB    VB      VerbForm=Inf    27      xcomp   _        _
30      a       a       DET     DT      Definite=Ind|PronType=Art       31      det     _  _
31      little  little  NOUN    NN      Number=Sing     29      obl:npmod       _    _
32      on      on      ADP     IN      _       34      case    _ _
33      the     the     DET     DT      Definite=Def|PronType=Art       34      det     _  _
34      price   price   NOUN    NN      Number=Sing     29      obl     _       _
35      which   which   PRON    WDT     PronType=Int    36      nsubj   _        _
36      means   mean    VERB    VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   27      parataxis       _    _
37      a       a       DET     DT      Definite=Ind|PronType=Art       38      det     _  _
38      lot     lot     NOUN    NN      Number=Sing     36      obj     _  _
39      to      to      ADP     IN      _       40      case    _ _
40      me      I       PRON    PRP     Case=Acc|Number=Sing|Person=1|PronType=Prs      36      obl     _       SpaceAfter=No
41      .       .       PUNCT   .       _       4       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
I did n't end up buying my car here , but I did think the guy who worked with me was pretty cool - he was willing to budge a little on the price which means a lot to me .
T2	ParallelScene 0 35	I did n't end up buying my car here
T3	Linker 38 41	but
T4	ParallelScene 42 96	I did think the guy who worked with me was pretty cool
T5	ParallelScene 99 144	he was willing to budge a little on the price
T6	Linker 145 150	which
T7	ParallelScene 151 170	means a lot to me .
T11	State 151 156	means
T12	Adverbial 157 162	a lot
T13	Participant 163 170	to me .
T14	Relator 163 165	to
T15	Center 166 168	me
T16	Function 157 158	a
T17	Center 159 162	lot
T18	Participant 99 101	he
T19	Function 102 105	was
T20	Adverbial 106 113	willing
T21	Function 114 116	to
T22	Process 117 122	budge
R1	Participant parent:T7 child:T22
T23	Adverbial 123 131	a little
T24	Participant 132 144	on the price
T25	Relator 132 134	on
T26	Function 135 138	the
T27	Center 139 144	price
T28	Function 123 124	a
T29	Center 125 131	little
T30	Participant 42 43	I
T31	Function 44 47	did
T32	Process 48 53	think
T33	Participant 54 96	the guy who worked with me was pretty cool
T34	Participant 54 80	the guy who worked with me
T35	Function 81 84	was
T36	Adverbial 85 91	pretty
T37	State 92 96	cool
T38	Function 54 57	the
T39	Center 58 61	guy
R2	Participant parent:T40 child:T39
T40	Elaborator 62 80	who worked with me
T41	Relator 62 65	who
T42	Process 66 72	worked
T43	Participant 73 80	with me
T44	Relator 73 77	with
T45	Center 78 80	me
T46	Participant 0 1	I
T47	Function 2 5	did
T48	Adverbial 6 9	n't
T49	Adverbial 10 16	end up
T50	Process 17 23	buying
T51	Participant 24 30	my car
T52	Participant 31 35	here
T53	Elaborator 24 26	my
T54	Center 27 30	car
R3	Participant parent:T53 child:T54
T55	State 24 26	my
</div>
</td></tr></tbody>
</table>

### Linker oblique
<table id="292997-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-292997-0002
# text = From the moment you enter the restaurant, you know you are some place special.
1       From    from    ADP     IN      _       3       case    _  _
2       the     the     DET     DT      Definite=Def|PronType=Art       3       det     _   _
3       moment  moment  NOUN    NN      Number=Sing     10      obl     _     _
4       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  5       nsubj   _ _
5       enter   enter   VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        3       acl:relcl       _     _
6       the     the     DET     DT      Definite=Def|PronType=Art       7       det     _   _
7       restaurant      restaurant      NOUN    NN      Number=Sing     5       obj     _   SpaceAfter=No
8       ,       ,       PUNCT   ,       _       10      punct   _        _
9       you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  10      nsubj   _        _
10      know    know    VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        0       root    _  _
11      you     you     PRON    PRP     Case=Nom|Person=2|PronType=Prs  14      nsubj   _        _
12      are     be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        14      cop     _  _
13      some    some    DET     DT      _       14      det     _  _
14      place   place   NOUN    NN      Number=Sing     10      ccomp   _        _
15      special special ADJ     JJ      Degree=Pos      14      amod    _ SpaceAfter=No
16      .       .       PUNCT   .       _       10      punct   _        _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
From the moment you enter the restaurant , you know you are some place special .
T2	Linker 0 15	From the moment
T3	ParallelScene 16 40	you enter the restaurant
T4	ParallelScene 43 80	you know you are some place special .
T7	Participant 43 46	you
T8	State 47 51	know
T9	Participant 52 80	you are some place special .
T11	Participant 52 55	you
T12	Function 56 59	are
T13	Participant 60 80	some place special .
T14	Elaborator 60 64	some
T15	Center 65 70	place
R1	Participant parent:T16 child:T15
T16	Elaborator 71 80	special .
T17	State 71 78	special
T18	Participant 16 19	you
T19	Process 20 25	enter
T20	Participant 26 40	the restaurant
T21	Function 26 29	the
T22	Center 30 40	restaurant
T23	Relator 0 4	From
T24	Function 5 8	the
T25	Center 9 15	moment
</div>
</td></tr></tbody>
</table>

## Other
### Apposition
<table id="351058-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-351058-0002
# text = This place and its sister store Peking Garden are the worst places to order from.
1       This    this    DET     DT      Number=Sing|PronType=Dem        2       det     _   _
2       place   place   NOUN    NN      Number=Sing     12      nsubj   _        _
3       and     and     CCONJ   CC      _       6       cc      _    _
4       its     its     PRON    PRP$    Gender=Neut|Number=Sing|Person=3|Poss=Yes|PronType=Prs  6       nmod:poss       _     _
5       sister  sister  NOUN    NN      Number=Sing     6       compound        _      _
6       store   store   NOUN    NN      Number=Sing     2       conj    _     _
7       Peking  Peking  PROPN   NNP     Number=Sing     8       compound        _      _
8       Garden  Garden  PROPN   NNP     Number=Sing     6       appos   _ _
9       are     be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        12      cop     _  _
10      the     the     DET     DT      Definite=Def|PronType=Art       12      det     _  _
11      worst   worst   ADJ     JJS     Degree=Sup      12      amod    _ _
12      places  place   NOUN    NNS     Number=Plur     0       root    _  _
13      to      to      PART    TO      _       14      mark    _ _
14      order   order   VERB    VB      VerbForm=Inf    12      acl     _       _
15      from    from    ADP     IN      _       14      obl     _  SpaceAfter=No
16      .       .       PUNCT   .       _       12      punct   _        _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
This place and its sister store Peking Garden are the worst places to order from .
T2	ParallelScene 0 82	This place and its sister store Peking Garden are the worst places to order from .
T4	Participant 0 45	This place and its sister store Peking Garden
T5	State 46 49	are
T6	Participant 50 82	the worst places to order from .
T7	Elaborator 50 59	the worst
T8	Center 60 66	places
R1	Participant parent:T7 child:T8
R2	Center parent:T12 child:T8
T9	Elaborator 67 82	to order from .
T10	Relator 67 69	to
T11	Process 70 75	order
T12	Participant 76 82	from .
T13	Relator 76 80	from
T14	State 50 59	the worst
T15	Function 50 53	the
T16	Center 54 59	worst
T17	Center 0 10	This place
T18	Connector 11 14	and
T19	Center 15 45	its sister store Peking Garden
T20	Elaborator 15 31	its sister store
T21	Center 32 45	Peking Garden
T22	Relator 15 18	its
T23	State 19 25	sister
T24	Participant 26 31	store
T25	Elaborator 0 4	This
T26	Center 5 10	place
</div>
</td></tr></tbody>
</table>

### State copula (expressing identity)
<table id="291046-0002">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-291046-0002
# text = This is the original Ham's restaurant, expanded into a regional chain in the late 80's -- but this one is no more.
1       This    this    PRON    DT      Number=Sing|PronType=Dem        7       nsubj   _ _
2       is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   7       cop     _   _
3       the     the     DET     DT      Definite=Def|PronType=Art       5       det     _   _
4       original        original        ADJ     JJ      Degree=Pos      5       amod    _  _
5       Ham     Ham     PROPN   NNP     Number=Sing     7       nmod:poss       _     SpaceAfter=No
6       's      's      PART    POS     _       5       case    _  _
7       restaurant      restaurant      NOUN    NN      Number=Sing     0       root    _  SpaceAfter=No
8       ,       ,       PUNCT   ,       _       7       punct   _ _
9       expanded        expand  VERB    VBN     Tense=Past|VerbForm=Part        7       acl     _   _
10      into    into    ADP     IN      _       13      case    _ _
11      a       a       DET     DT      Definite=Ind|PronType=Art       13      det     _  _
12      regional        regional        ADJ     JJ      Degree=Pos      13      amod    _ _
13      chain   chain   NOUN    NN      Number=Sing     9       obl     _      _
14      in      in      ADP     IN      _       17      case    _ _
15      the     the     DET     DT      Definite=Def|PronType=Art       17      det     _  _
16      late    late    ADJ     JJ      Degree=Pos      17      amod    _ _
17      80's    80'     NOUN    NNS     Number=Plur     9       obl     _        _
18      --      --      PUNCT   ,       _       7       punct   _ _
19      but     but     CCONJ   CC      _       24      cc      _   _
20      this    this    DET     DT      Number=Sing|PronType=Dem        21      det     _  _
21      one     one     NOUN    NN      Number=Sing     24      nsubj   _        _
22      is      be      AUX     VBZ     Mood=Ind|Number=Sing|Person=3|Tense=Pres|VerbForm=Fin   24      cop     _  _
23      no      no      ADV     RB      _       24      advmod  _       _
24      more    more    ADV     RBR     _       7       conj    _      SpaceAfter=No
25      .       .       PUNCT   .       _       7       punct   _ _
</div>
</td></tr><tr><td>
UCCA:
<div class="ann-annotation">
This is the original Ham 's restaurant , expanded into a regional chain in the late 80's -- but this one is no more .
T2	ParallelScene 0 88	This is the original Ham 's restaurant , expanded into a regional chain in the late 80's
T3	Linker 92 95	but
T4	ParallelScene 96 117	this one is no more .
T7	Participant 96 104	this one
T8	Function 105 107	is
T9	Adverbial 108 110	no
T10	State 111 115	more
T11	Elaborator 96 100	this
T12	Center 101 104	one
T13	Participant 0 4	This
T14	State 5 7	is
T15	Participant 8 88	the original Ham 's restaurant , expanded into a regional chain in the late 80's
T16	Elaborator 8 20	the original
T17	Elaborator 21 27	Ham 's
R1	Participant parent:T19 child:T17
T18	Center 28 38	restaurant
R2	Participant parent:T16 child:T18
T19	Elaborator 41 88	expanded into a regional chain in the late 80's
T21	Process 41 49	expanded
T22	Participant 50 71	into a regional chain
T23	Time 72 88	in the late 80's
T24	Relator 72 74	in
T25	Function 75 78	the
T26	Elaborator 79 83	late
T27	Center 84 88	80's
T28	Relator 50 54	into
T29	Function 55 56	a
T30	Elaborator 57 65	regional
T31	Center 66 71	chain
T32	State|Adverbial 8 20	the original
T33	Function 8 11	the
T34	Center 12 20	original
</div>
</td></tr></tbody>
</table>

### Function copula (expressing attribution/location)
<table id="063347-0003">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-063347-0003
# text = Excellent chefs are in the kitchen preparing memorable breakfasts.
1       Excellent       excellent       ADJ     JJ      Degree=Pos      2       amod    _  _
2       chefs   chef    NOUN    NNS     Number=Plur     6       nsubj   _ _
3       are     be      AUX     VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        6       cop     _   _
4       in      in      ADP     IN      _       6       case    _  _
5       the     the     DET     DT      Definite=Def|PronType=Art       6       det     _   _
6       kitchen kitchen NOUN    NN      Number=Sing     0       root    _  _
7       preparing       prepare VERB    VBG     VerbForm=Ger    2       acl     _   _
8       memorable       memorable       ADJ     JJ      Degree=Pos      9       amod    _  _
9       breakfasts      breakfast       NOUN    NNS     Number=Plur     7       obj     _   SpaceAfter=No
10      .       .       PUNCT   .       _       6       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Excellent chefs are in the kitchen preparing memorable breakfasts .
T2	ParallelScene 0 34	Excellent chefs are in the kitchen
T3	ParallelScene 35 67	preparing memorable breakfasts .
T5	Process 35 44	preparing
T6	Participant 45 67	memorable breakfasts .
T7	Adverbial 45 54	memorable
T8	Process 55 65	breakfasts
T9	Adverbial 0 9	Excellent
T10	Process|Participant 10 15	chefs
R1	Participant parent:T3 child:T10
T11	Function 16 19	are
T12	Participant 20 34	in the kitchen
T13	Relator 20 22	in
T14	Function 23 26	the
T15	Center 27 34	kitchen
</div>
</td></tr></tbody>
</table>


### Ground discourse
<table id="351561-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-351561-0004
# text = They say no, Warwick in New Jersey, Call New Jersey.
1       They    they    PRON    PRP     Case=Nom|Number=Plur|Person=3|PronType=Prs      2       nsubj   _ _
2       say     say     VERB    VBP     Mood=Ind|Tense=Pres|VerbForm=Fin        0       root    _  _
3       no      no      INTJ    UH      _       5       discourse       _     SpaceAfter=No
4       ,       ,       PUNCT   ,       _       5       punct   _ _
5       Warwick Warwick PROPN   NNP     Number=Sing     2       ccomp   _ _
6       in      in      ADP     IN      _       8       case    _  _
7       New     New     PROPN   NNP     Number=Sing     8       compound        _      _
8       Jersey  Jersey  PROPN   NNP     Number=Sing     5       nmod    _       SpaceAfter=No
9       ,       ,       PUNCT   ,       _       5       punct   _ _
10      Call    call    VERB    VB      Mood=Imp|VerbForm=Fin   5       parataxis       _     _
11      New     New     PROPN   NNP     Number=Sing     12      compound        _     _
12      Jersey  Jersey  PROPN   NNP     Number=Sing     10      obj     _  SpaceAfter=No
13      .       .       PUNCT   .       _       2       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
They say no , Warwick in New Jersey , Call New Jersey .
T2	ParallelScene 0 55	They say no , Warwick in New Jersey , Call New Jersey .
T4	Participant 0 4	They
T5	Process 5 8	say
T6	Participant 9 55	no , Warwick in New Jersey , Call New Jersey .
T7	ParallelScene 9 11	no
T8	ParallelScene 14 35	Warwick in New Jersey
T9	ParallelScene 38 55	Call New Jersey .
T13	Process 38 42	Call
T14	Participant 43 53	New Jersey
T15	Participant 14 21	Warwick
T16	State 22 24	in
T17	Participant 25 35	New Jersey
</div>
</td></tr></tbody>
</table>


<table id="007403-0006">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-007403-0006
# text = Please visit my website to learn more about my practice at www.veraakulov.com.
1       Please  please  INTJ    UH      _       2       discourse       _     _
2       visit   visit   VERB    VB      Mood=Imp|VerbForm=Fin   0       root    _  _
3       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      4       nmod:poss       _     _
4       website website NOUN    NN      Number=Sing     2       obj     _   _
5       to      to      PART    TO      _       6       mark    _  _
6       learn   learn   VERB    VB      VerbForm=Inf    2       advcl   _      _
7       more    more    ADJ     JJR     Degree=Cmp      6       obj     _   _
8       about   about   ADP     IN      _       10      case    _ _
9       my      my      PRON    PRP$    Number=Sing|Person=1|Poss=Yes|PronType=Prs      10      nmod:poss       _    _
10      practice        practice        NOUN    NN      Number=Sing     7       obl     _     _
11      at      at      ADP     IN      _       12      case    _ _
12      www.veraakulov.com      www.veraakulov.com      X       ADD     _       2       obl     _        SpaceAfter=No
13      .       .       PUNCT   .       _       2       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Please visit my website to learn more about my practice at www.veraakulov.com .
T2	ParallelScene 0 23;56 79	Please visit my website at www.veraakulov.com .
T3	Linker 24 26	to
T4	ParallelScene 27 55	learn more about my practice
T7	Process 27 32	learn
T8	Adverbial 33 37	more
T9	Participant 38 55	about my practice
T10	Relator 38 43	about
T11	Participant 44 46	my
T12	Process 47 55	practice
T14	Ground 0 6	Please
T15	Process 7 12	visit
T16	Participant 13 23;56 79	my website at www.veraakulov.com .
T17	Elaborator 13 15	my
T18	Center 16 23	website
R1	Participant parent:T17 child:T18
T19	Elaborator 56 79	at www.veraakulov.com .
T20	Relator 56 58	at
T21	Center 59 77	www.veraakulov.com
T22	State 13 15	my
</div>
</td></tr></tbody>
</table>


### Ground + Participant vocative
<table id="024132-0004">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
# sent_id = reviews-024132-0004
# text = Thanks Mark.
1       Thanks  thanks  NOUN    NN      Number=Sing     0       root    _  _
2       Mark    Mark    PROPN   NNP     Number=Sing     1       vocative        _      SpaceAfter=No
3       .       .       PUNCT   .       _       1       punct   _ _
</div>
</td><td>
UCCA:
<div class="ann-annotation">
Thanks Mark .
T2	ParallelScene 0 13	Thanks Mark .
T3	Process 0 6	Thanks
T4	Participant 7 11	Mark
</div>
</td></tr></tbody>
</table>


### Function nsubj (expletive)
<table id="295288-0006">
<tbody><tr><td>
UD:
<div class="conllu-parse">
# visual-style nodes red
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
</td></tr><tr><td>
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



<!-- ([\d_]+(:\w+)+\|?)+ -->


## Toy example
<table id="toy">
<tbody><tr><td>
</td><td>
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
