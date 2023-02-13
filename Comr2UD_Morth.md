### A Russian tagset for UD

Updated: 20 Jan 2023   
Based on [UD guidelines](https://universaldependencies.org/guidelines.html)

## Parts of speech (Части речи)

<table>
    <thead>
        <tr>
            <th>Compreno</th>
            <th>UD</th>
            <th>Конвертация</th>
            <th>Примеры</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td rowspan=2>Noun</td>
            <td>NOUN</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>PROPN</td>
            <td>
                <body>
                    <ul>
                    <li>'Proper' в тегах </li>
                    <li> lemma = 'бен', 'аль', 'де' + pos=Prefixoid</li> 
                    <li> lemma = ‘#Acronym’ + pos=Invariable </li>
                    </ul>
                </body>
            </td>
            <td>бен Ладен, де Голь 
                <br> А300, М1
            </td>
        </tr>
        <tr>
            <td>Adjective</td>
            <td>ADJ</td>
            <td>
                <body>
                    <ul>
                    <li> pos=’Numeral’ + ‘MaximallyRestrictiveModifiers’=’Ordinal’ </li> 
                    <li> label=’OrderInTimeAndSpace’ + semrel="#number:#number:DIGITAL_NUMBER"’’ </li>
                    <li> semrel='"#day_number:DAY_NUMBER"'</li>
                    </ul>
                </body>
            </td>
            <td> IV, третьего <br> в 1998 году <br> 8 марта </td>
        </tr>
        <tr>
            <td rowspan=2>Verb</td>
            <td>VERB</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>AUX</td>
            <td>‘SyntacticParadigm’ = ‘SyntAuxVerb’</td>
            <td></td>
        </tr>
        <tr>
            <td>Adverb</td>
            <td>ADV</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Number</td>
            <td>NUM</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Particle</td>
            <td>PART</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Preposition</td>
            <td>ADP</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Predicative</td>
            <td>ADV</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Interjection</td>
            <td>INTJ</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>Preposition</td>
            <td>ADP</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td rowspan=2>Pronoun</td>
            <td>PRON</td>
            <td></td>
            <td></td>
        </tr>
        <tr>
            <td>DET</td>
            <td>
                <body>
                    <ul>
                    <li> dep=’det and’ lemma={'такой', 'какой', 'всякий', 'некоторый',
                        'никакой', 'некий', 'сей', 'чей', 
                        'какой-либо', 'какой-нибудь','кое-какой',
                        'весь', 'этот', 'тот', 'каждый',
                        'мой', 'твой', 'ваш', 'наш', 'свой', 'любой', 
                        'каждый', 'какой-то', 'некоторый', 'такой-то', 'чей-то', 
                        'чей-либо', 'кой', 'никой'}
                    </li> 
                    <li> token=lemma / token=’ее’, lemma=’её’ </li>
                    </ul>
                </body>
            </td>
            <td></td>
        <tr>
        <tr>
            <td>-</td>
            <td>SYM</td>
            <td>token={'%', '$', '№', '°', '€', '+', '=', '№', '#', '@', '~', '^', '&', '\\','/', '&'}</td>
            <td></td>
        </tr>
        <tr>
            <td rowspan=2>Conjunction</td>
            <td>CCONJ</td>
            <td>‘Coordinator’ в тегах</td>
            <td></td>
        </tr>
        <tr>
            <td>SCONJ</td>
            <td>иначе</td>
            <td></td>
        </tr>
    </tbody>
</table>

## Grammatical features (FEAT)

Теги
adj_feats = ('Case', 'Gender', 'Number', 'DegreeOfComparison') <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ Animacy если Case = Acc, Gender = Masc / Case = Acc, lemma в ('оба', 'обе', 'два', 'три', 'четыре' / Case = Acc, Gender, lemma = 'один'); <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- ‘Case’ если Variant = Short; <br>
adv_feats = 'DegreeOfComparison'; <br>
noun_feats = ('Animatedness', 'Case', 'Gender', 'Number'); <br>
num_feats = ('Animatedness', 'Case', 'Gender'); <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- ‘Gender’ если lemma не в ('i', 'ii', 'оба', 'один', 'полтора', 'два'); <br>
verb_feats = ('Aspect', 'Mood', 'Number', 'Person', 'Tense', 'GrammaticalType', 'Voice', 'Gender'); <br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ ‘Case’ если VerbForm = Part, Variant != Short; <br>
pron_feats = ('Animatedness', 'Case', 'Gender', 'Number', 'Person'); <br>
det_set = {'Animatedness', 'Case', 'Degree', 'Gender', 'Number'}.



<table>
    <thead>
        <tr>
            <th>Compreno</th>
            <th>UD</th>
            <th>Конвертация</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td colspan=3> <b>Case</td>
        </tr>
        <tr>
            <td>Accusative</td>
            <td>Acc</td>
            <td></td>
        </tr>
        <tr>
            <td>Dative</td>
            <td>Dat</td>
            <td></td>
        </tr>
        <tr>
            <td>Genitive</td>
            <td rowspan=2>Gen</td>
            <td></td>
        </tr>
        <tr>
            <td>Genitive|Partitive</td>
            <td></td>
        </tr>
        <tr>
            <td>Instrumental</td>
            <td>Ins</td>
            <td></td>
        </tr>
        <tr>
            <td>Locative</td>
            <td rowspan=2>Loc</td>
            <td></td>
        </tr>
        <tr>
            <td>Prepositional</td>
            <td></td>
        </tr>
        <tr>
            <td>Nominative</td>
            <td>Nom</td>
            <td></td>
        </tr>
        <tr>
            <td>Partitive</td>
            <td>Par</td>
            <td></td>
        </tr>
        <tr>
            <td>Vocative</td>
            <td>Voc</td>
            <td></td>
        </tr>
        <tr>
            <td>ZeroCase</td>
            <td> - </td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><b>Person</td>
        </tr>
        <tr>
            <td>PersonFirst</td>
            <td>1</td>
            <td></td>
        </tr>
        <tr>
            <td>PersonSecond</td>
            <td>2</td>
            <td></td>
        </tr>
        <tr>
            <td>PersonThird</td>
            <td>3</td>
            <td></td>
        </tr>
        <tr>
            <td>PersonZero</td>
            <td> - </td>
            <td></td>
        </tr>
        <tr>
            <td><b>DegreeOfComparison</td>
            <td colspan=2><b>Degree</td>
        </tr>
        <tr>
            <td>DegreeSuperlative </td>
            <td> Sup </td>
            <td></td>
        </tr>
        <tr>
            <td>DegreePositive </td>
            <td> Pos </td>
            <td></td>
        </tr>
        <tr>
            <td>DegreeComparative </td>
            <td> Cmp </td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><b>Mood</td>
        </tr>
        <tr>
            <td>Imperative</td>
            <td> Imp </td>
            <td></td>
        </tr>
        <tr>
            <td>Subjunctive</td>
            <td> Cnd </td>
            <td></td>
        </tr>
        <tr>
            <td></td>
            <td> Ind </td>
            <td> не Imp, Cnd, NoMood</td>
        </tr>
        <tr>
            <td>NoMood</td>
            <td> - </td>
            <td></td>
        </tr>
        <tr>
            <td><b>GrammaticalType</td>
            <td colspan=2><b>VerbForm</td>
        </tr>
        <tr>
            <td>GTInfinitive</td>
            <td> Inf </td>
            <td></td>
        </tr>
        <tr>
            <td>GTVerb</td>
            <td> Fin </td>
            <td></td>
        </tr>
        <tr>
            <td>GTParticipleAttributive</td>
            <td rowspan=2> Part </td>
            <td></td>
        </tr>
        <tr>
            <td>GTParticiple</td>
            <td></td>
        </tr>
        <tr>
            <td>GTAdverb</td>
            <td> Conv </td>
            <td></td>
        </tr>
        <tr>
            <td><b>Animatedness</td>
            <td colspan=2><b>Animacy</td>
        </tr>
        <tr>
            <td>Animate</td>
            <td> Anim </td>
            <td></td>
        </tr>
        <tr>
            <td>Inanimate</td>
            <td> Inan </td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><b>Gender</td>
        </tr>
        <tr>
            <td>Feminine</td>
            <td> Fem </td>
            <td>‘SyntacticGender’=’SyntFeminine’</td>
        </tr>
        <tr>
            <td>Neuter</td>
            <td> Neut </td>
            <td>‘SyntacticGender’= ’SyntNeuter’</td>
        </tr>
        <tr>
            <td>Masculine</td>
            <td> Masc </td>
            <td></td>
        </tr>
        <tr>
            <td>Common</td>
            <td> - </td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><b>Number</td>
        </tr>
        <tr>
            <td>Plural</td>
            <td>Plur</td>
            <td></td>
        </tr>
        <tr>
            <td>Singular</td>
            <td>Sing</td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><b>Aspect</td>
        </tr>
        <tr>
            <td>Perfective</td>
            <td>Perf</td>
            <td></td>
        </tr>
        <tr>
            <td>Imperfective</td>
            <td>Imp</td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><i>Если ‘Pairness’=’BiAspectual’ аспекта нет</td>
        </tr>
        <tr>
            <td colspan=3><b>Tense</td>
        </tr>
        <tr>
            <td>Present</td>
            <td>Pres</td>
            <td></td>
        </tr>
        <tr>
            <td>Future</td>
            <td>Fut</td>
            <td>‘Tense’=’Pres’ and ‘Aspect’=’Perf’</td>
        </tr>
        <tr>
            <td>Past</td>
            <td>Past</td>
            <td></td>
        </tr>
        <tr>
            <td colspan=3><b>Voice</td>
        </tr>
        <tr>
            <td>Active</td>
            <td>Act</td>
            <td>‘Voise’=’VoiceSya’ and ‘SyntActive’ in feats</td>
        </tr>
        <tr>
            <td>Passive</td>
            <td>Pass</td>
            <td>‘Voise’=’VoiceSya’ and ‘SyntPassive’ in feats</td>
        </tr>
        <tr>
            <td>VoiceSya</td>
            <td>Mid</td>
            <td></td>
        </tr>
    </tbody>
</table>
