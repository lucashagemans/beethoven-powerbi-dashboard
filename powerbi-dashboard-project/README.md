# Beethoven String Quartets

This dashboard ananlyses the 16 string quartets of Beethoven (1770-1827). The main purpose is to give intuitive visual insights about one of the most important bodies of work in classical chamber music. The creation of the string quartets spans most of Beethoven's lifetime from 1798 untill 1826. How did his style develop? What was his favourite key? What are the longest movements? What is the highest note in each movment? There is hardly any quartet ensemble that didn't play Beethoven, resulting in many different recordings of the "Complete Beethoven Quartets" on a set of usually 7 CD's. This enables the comparison of several recordings and interpretations between different ensembles.

A commercially interesting question arises: (How) can spotify listeners be advanced towards a deeper level of understanding and enjoyment/appreciation of Beethoven's most intimate and personal music? Perhaps a visual dashboard can kickstart a rewarding auditory journey to develop listening skills or hightened sensibility.

# Installation instructions:

No installments required.

# Requirements:

See datasets below.

# Information sources en Datasets:

Data collection

An important datasource comes from the Annotated Beethoven Corpus (ABC) that was made public in 2018 by the Digital and Cognitive Musicology Lab (DMCL) at the École Polytechnique Fédérale de Lausanne (EPFL) in Switserland. Their annotation standards and naming conventions are implemented in this analysis. Most importantly the filenaming is used as ID. For example, the filename "n01op18-1_01.tsv" is comprised of:
* n01 : numerical order of the string quartet
* op18-1 : opus number
* 01 : movement number

Data files

* beethoven_string_quartets.csv (compiled by Lucas Hagemans)
* chronology.csv
* annotated_beethoven_corpus_overview.csv
* midi_note_numbers.csv
* n01op18-1_01.tsv (converted to csv's with python)
* n01op18-1_02.tsv
* n01op18-1_03.tsv
* n01op18-1_04.tsv
* appended_movements.csv (collection of files n01op18-1 etc.)

Dataset sources

* https://github.com/DCMLab/ABC/tree/main#overview
* https://github.com/DCMLab/standards
* https://www.inspiredacoustics.com/en/MIDI_note_numbers_and_center_frequencies
* https://en.wikipedia.org/wiki/List_of_compositions_by_Ludwig_van_Beethoven#String_quartets
* [https://imslp.org/wiki/String_Quartet_No.1,_Op.18_No.1_(Beethoven,_Ludwig_van)](https://imslp.org/wiki/String_Quartet_No.1,_Op.18_No.1_(Beethoven,_Ludwig_van)) ...etc. (SQ numbers 1 to 16)
* https://www.supraphon.com/album/571538-beethoven-the-complete-string-quartets
* https://www.discogs.com/release/9129913-Ludwig-van-Beethoven-Tokyo-String-Quartet-Complete-String-Quartets
* https://www.discogs.com/release/11297588-Budapest-String-Quartet-The-Complete-Beethoven-Quartets

Scientific articles and resources

* https://www.frontiersin.org/articles/10.3389/fdigh.2018.00016/full
* https://www.researchgate.net/publication/326162775_The_Annotated_Beethoven_Corpus_ABC_A_Dataset_of_Harmonic_Analyses_of_All_Beethoven_String_Quartets
* https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0217242
* https://core.ac.uk/download/pdf/211998554.pdf
* https://arxiv.org/pdf/2201.08796.pdf
* https://www.epfl.ch/labs/dcml/projects/corpus-project/
* https://www.epfl.ch/labs/dcml/the-musescore-parser-ms3/

Media

* https://www.forbes.com/sites/evaamsen/2019/06/06/a-data-science-analysis-finds-beethovens-style-in-his-string-quartets/
* https://phys.org/news/2019-06-decoding-beethoven-music-style-science.html
* https://actu.epfl.ch/news/decoding-beethoven-s-music-style-using-data-scienc/
* https://www.therestisnoise.com/2006/01/beethovens_gros.html

# Preprocessing

The raw tsv files were converted to csv files with the provided python script. A script to automatize this process for all 70 files seems out of scope for now.

# Navigation Guide and Dashboard Functions:

Instructions on how to navigate the dashboard, including selecting filters, slicers, and interactive elements. With an overview of the main features and interactive elements in the dashboard, including charts, tables, filters, etc.

## Tab 1: Historical chronology of the quartets

By pressing ctrl + click on the bookmarked pictures of young, middle-aged, or old Beethoven you can toggle between the early, middle, and late periods of Beethoven's musical output. The corresponding string quartets will be highlighted in the table. This gives insight into Beethoven's productivity and maturity of each string quartet.

## Tab 2: Analysis of musical notes in individual movements

With the slicer you can select the quartet movement to review. The tempo, time signature, and key are indicated. The amount of musical notes (midi notes*) together with the lowest and highest notes are indicated. The ambitus is the musical term for the range from low to high register. In the bar graph we can see the distribution of notes for each note height. By selecting an instrument one can see the data for that particular instrument. 

*Musical Instrument Digital Interface https://en.wikipedia.org/wiki/MIDI

## Tab 3: Comparison of quartet movements

The amount of quartet movments per quartet increases in the late quartets. This is clearly visible in the treemap. By clicking on an opus number, the data for that opus (i.e. string quartet) is specified. The keys that Beethoven used are visualized for string quartets in a treemap as well as the individual movements in a pie chart. The harmonic rhythm is calculated based on labels annotated in the Annotated Beethoven Corpus. The label count of each movement is divided by the number of measures. This gives an indication of the harmonic rhythm, i.e. how much the harmony changes per measure. The size of the dots in the scatter plot indicates harmonic rhythm. All 4 visuals are interacting with each other.

## Tab 4: Comparison of performances

The line chart compares durations of all quartet movements performed by 3 different ensembles. The total sum of seconds for each ensemble is indicated on a card. It is clearly visible that the Budapest String Quartet doesn't play all the repeats like the other two ensembles.