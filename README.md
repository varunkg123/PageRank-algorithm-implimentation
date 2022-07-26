# PageRank-algorithm-implimentation

PageRank (PR) is an algorithm used by Google Search to rank websites in their search engine results.
PageRank works by counting the number and quality of links to a page to determine a rough estimate of how important the website is. 
The PageRank algorithm outputs a probability distribution used to represent the likelihood that a person randomly clicking on links will arrive at any particular page. PageRank can be calculated for collections of documents of any size. 

## Simplified algorithm 
Assume a small universe of four web pages: A, B, C, and D. Links from a page to itself, or multiple outbound links from one single page to another single page, are ignored. PageRank is initialized to the same value for all pages. In the original form of PageRank, the sum of PageRank over all pages was the total number of pages on the web at that time, so each page in this example would have an initial value of 1. However, later versions of PageRank, and the remainder of this section, assume a probability distribution between 0 and 1. Hence the initial value for each page in this example is 0.25.

Suppose instead that page B had a link to pages C and A, page C had a link to page A, and page D had links to all three pages. Thus, upon the first iteration, page B would transfer half of its existing value, or 0.125, to page A and the other half, or 0.125, to page C. Page C would transfer all of its existing value, 0.25, to the only page it links to, A. Since D had three outbound links, it would transfer one-third of its existing value, or approximately 0.083, to A. At the completion of this iteration, page A will have a PageRank of approximately 0.458. 

![image](https://user-images.githubusercontent.com/103302482/181094125-5ace158d-6a4c-49f9-b892-aac2feb445ad.png)

In other words, the PageRank conferred by an outbound link is equal to the document's own PageRank score divided by the number of outbound links L( ).

![image](https://user-images.githubusercontent.com/103302482/181094420-afd21884-91df-4c41-98ed-6e73d4e6f74e.png)

In the general case, the PageRank value for any page u can be expressed as:

![image](https://user-images.githubusercontent.com/103302482/181094580-5b41d55d-748a-4bfa-bdd6-84cbed0dd064.png)

i.e. the PageRank value for a page u is dependent on the PageRank values for each page v contained in the set Bu (the set containing all pages linking to page u), divided by the number L(v) of links from page v. The algorithm involves a damping factor for the calculation of the PageRank. It is like the income tax which the govt extracts from one despite paying him itself.
