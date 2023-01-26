### 1) (Base) Domain Name extraction from the full link
- Should be used in Search Function Implementation in any app for user convenience. i.e.
> ` www.ABC.com/xyz ` ---> ABC 
> 
> ` Https://DEF.com/xyz ` ---> DEF

- If user searches documents within your app by string (copied directly form browser/somewhere) ` www.ABC.com/xyz ` & equivalent match is not found then, below formulae (typical example with Google sheets) will extract only Domain Name i.e. ABC from it and search continues....


Google sheet formuale (full link is placed in cell A1): 
```
=REGEXREPLACE(REGEXEXTRACT(A1, "(?i)^(?:https?:\/\/)?(?:www\.)?([^\/]+)/?"),"\..*","") 
```
