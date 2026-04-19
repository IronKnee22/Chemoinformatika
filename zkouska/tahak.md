1. Věk mozku z MRI (Brain Age)

    Proč to děláme: Chceme zjistit, jestli mozek stárne rychleji než zbytek těla (prevence Alzheimerovy choroby, atd.).

    Princip: Umělá inteligence (Deep Learning) se na tisících zdravých mozků naučí, jak vypadá mozek ve 20, 40 nebo 60 letech.

    Klíčová pointa (Brain Age Gap): Rozdíl mezi chronologickým (v občance) a biologickým (odhadnutým AI) věkem. Pokud AI řekne, že je ti 60, ale v občance máš 40 (gap +20), je někde problém.

💊 2. Chemoinformatika (Hledání léku)

    Proč to děláme: Hledáme nový lék mezi miliardami existujících molekul a nechceme je všechny míchat v laboratoři.

    Princip (Virtuální screening): Počítačový "Tinder". Molekuly zapisujeme jako text (SMILES) a AI rychle filtruje obří databáze (např. ZINC), aby našla ty, které by mohly pasovat do našeho cílového proteinu.

📐 3. QSAR (Předpověď účinku podle tvaru)

    Proč to děláme: Chceme předpovědět, jak silný bude lék, jen na základě jeho vzorce (Quantitative Structure-Activity Relationship).

    Princip: Molekulu si popíšeme pomocí čísel (Deskriptory – váha, počet kruhů, náboj). AI hledá matematický vztah mezi těmito deskriptory a biologickým účinkem.

    Největší hrozba (Overfitting): Přeučení! Když máš málo otestovaných léků, ale spoustu deskriptorů, AI se to "nabifluje" nazpaměť, ale v praxi selže.

    Řešení: Výběr příznaků nebo PCA (Principal Component Analysis) – snížení počtu proměnných.

🕳️ 4. Detekce tunelů (CAVER)

    Proč to děláme: QSAR nám sice našel lék, ale my musíme ověřit, jestli se vůbec skrz změť atomů fyzicky protáhne dovnitř proteinu do aktivního místa.

    Princip (RRT algoritmus): RRT (Rapidly-exploring Random Tree) roste z aktivního místa a náhodně "vystřeluje" větve do volného prostoru. Kde narazí na atom, tam větev uschne. Rychle tak zmapuje cestu ven.

    Nástroj: Sférická sonda (virtuální kulička), kterou zkoušíme protlačit. Nejužší místo tunelu se jmenuje Bottleneck (úzké hrdlo).

    Statika vs. Dynamika: Neděláme to na jedné fotce, ale na "filmu" (sérii snímků), protože protein "dýchá". Hledáme frequent tunnels (časté tunely), které zůstávají stabilně otevřené.

🧬 5. Mikročipy a exprese genů (DNA Microarrays)

    Proč to děláme: Chceme vidět, kterých 35 000 genů je v rakovinné buňce aktivních a kterých ne.

    Princip (Hybridizace): Na čipu jsou miliony "věžiček" (sond). Z pacienta vytáhneme svítící mRNA. Kde se mRNA přilepí k sondě, tam to pod laserem svítí. Silné světlo = gen maká naplno.

    Zpracování dat (Ill-posed problem): Zase přeučení. Použijeme K-means / PCA na výběr hrstky podezřelých genů.

    Interpretace (GOrilla / KEGG): V GOrille získáme ten "červený strom" (Gene Ontology). Červená políčka = Enrichment (obohacení). Znamená to, že ty geny nejsou náhodné, ale rakovina jimi cíleně přenastavila nějaký biologický proces (např. vypnula buněčnou smrt).

    Statistika: Pozor na Multiple comparisons. Abychom neměli falešné poplachy, používáme přísné tresty jako je Bonferroniho korekce.

🔮 6. AlphaFold (Předpověď 3D tvaru)

    Proč to děláme: Abychom mohli hledat tunely nebo léky, potřebujeme znát 3D tvar proteinu. V laboratoři to trvá roky, AlphaFold to spočítá za minuty ze samotné sekvence aminokyselin.

    Vývoj (Klíčová slova):

        AF1: Konvoluční sítě (distogramy).

        AF2: Transformers a MSA (Multiple Sequence Alignment) – kouká do evoluce jiných zvířat, které aminokyseliny se měnily společně.

        AF3: Difuzní model – tvoří 3D model z atomárního šumu metodou "odšumování" (podobně jako Midjourney kreslí obrázky nebo doplňuje chybějící kousek dortu). Umí už i léky a DNA.