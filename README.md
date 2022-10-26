### Installation Imagemagick

https://imagemagick.org/script/download.php


### make PDF like scanned copy (after adding e-signature)

```convert -density 300 input.pdf -attenuate 0.45  -sharpen 0x1.0  -rotate 0.4  output.pdf  ```

###### additional parameters 

 -colorspace gray  
 -blur 0x1  
 -quality 85  
 -compress JPEG  

### Merge images or PDFs 


```convert +append *.png merged.png ```
```convert -append *.pdf merged.pdf ```

-append : one after the other
+append : side by side

### Export PDF as an Image

```convert file-?.pdf file.jpg```

### Reduce scanned PDF size

```convert -density 200x200 -quality 60 -compress jpeg input.pdf output.pdf```   

or

```convert -density 150x150 -compress Zip input.pdf output.pdf```   

or

```convert input.pdf -resample 85% output.pdf```


###### References

https://askubuntu.com/questions/113544/how-can-i-reduce-the-file-size-of-a-scanned-pdf-file   
https://gist.github.com/bre7/468e4a73bc7a6b5ae5542c2529fc58a3   
https://gist.github.com/scf37/39e2724e7e091ed2a9bc75532244a832   
