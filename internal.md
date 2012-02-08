LinkCloud - a visualizer for your Singly links
----------------------------------------------


#Pseudocode

	var WordElement(word, count){
		this.word = word;
		this.count = count;
	};
	function getTokens(data){
		var tokens = data.match(/\w/g);
		var wdDict = {};
		for (var i in tokens) {
			var t = tokens[i];
			if (!wdDict[t])
				wdDict[t] = 0;
			wdDict[t]+=1;
		}
		return wdDict;
	}
	function sortDict(d) {
 		var sorted = {};
 		for (k in d) {
 			if (!sorted[d[k]])
    			sorted[d[k]] = [];
    		sorted[d[k]].push(k);
 		}
 	return sorted;
 	}
 	
	//Get Links
	links = getLinks()
	//Process Links
	for lnk in link 
		lnk_title = lnk.title
		wordCounts = wordHistogram(lnk_title)
		lnk_text = lnk.text
		wordCounts = wordHistogram(link_text)
	for i : (1,100):
		write "<li>"+wordCounts[i].key+" "+wordCounts[i].count
	

 	//Display Link Results