cat tmp.ca.txt | grep -o CA[0-9][0-9][0-9][0-9] | sort | uniq | wc -
