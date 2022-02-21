---
title: "Exercise 2"
output: 
  html_document: 
    keep_md: yes
---



##

```r
GetTreeFromOpenTree <- function() {
	library(rotl)
	library(ape)

 songbird.id <- rotl::tnrs_match_names("Passeri")$ott_id

	# Now get Open Tree's current best estimate of the phylogeny for the group
	# They call this the tree of life; we can get the subtree for just this group.
	songbird.tree <- rotl::tol_subtree(ott_id=songbird.id)

	# Let's plot the tree:
	ape::plot.phylo(songbird.tree, type="fan", cex=0.2)
	
	# and return the tree
	return(songbird.tree)
}

songbird.tree <- GetTreeFromOpenTree()
```

```
## Warning: package 'rotl' was built under R version 4.1.2
```

```
## Warning: package 'ape' was built under R version 4.1.2
```



```
## Warning in collapse_single_cpp(ances = tree$edge[, 1], desc = tree$edge[, :
## printing of extremely long output is truncated
```





```
## Warning in collapse_single_cpp(ances = tree$edge[, 1], desc = tree$edge[, :
## printing of extremely long output is truncated
```




                                                            

```
## Warning in collapse_singles(tr, show_progress): Dropping singleton nodes with
## labels: Passer melanurus ott407762
```

![](Exercise_2_files/figure-html/unnamed-chunk-1-1.png)<!-- -->



