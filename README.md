# Assignment1

ssh username@trgn.usc.edu

esearch -db pubmed -query "fetal alcohol exposure heart development" |   efetch -format abstract > fas.heart.txt

vi fas.heart.txt

%s/\n//g

wq

wordcloud_cli --text fas.heart.txt --imagefile fas.heart.wordcloud.png

exit

rsync -avz username@trgn.usc.edu:~/fas.heart.wordcloud.png ~/desktop
