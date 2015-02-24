---
title: SeqPlots
author: Przemyslaw Stempor
framework: impressjs
#highlighter: highlight.js  # {highlight.js, prettify, highlight}
#hitheme: tomorrow  
#mode: draft
mode: selfcontained
--- #s .slide x:0 y:-2000 z:0

<h1><b style="font-size: 140%;">SeqPlots</b> - a fast interactive web tool for visualizing next generation sequencing signals along genomic features.</h1>
<p style="font-size: 85%; text-align: right;">Przemyslaw Stempor @ Internal Seminar, 25 February 2015<p>

--- #big x:0 y:-1250 rot:0 z:100 scale:1 .hide
The <b>BIG</b> <span class="thoughts">question!</span>

--- #q x:0 y:-700 z:0 rot:0 scale:2 .cent 
What are the **relationships** between **chromatin features**, underlying **DNA sequence** and **gene regulation**?

--- #qf1v2 x:-300 y:50 z:0 rot:0 scale:1.2
<img src="chromatin2.jpg" alt="chrom" height='500px'>
<p class="source" style="font-size: 0.46em;">Source: http://www.cliffsnotes.com/assets/24452.jpg</p>

--- #qf2 x:700 y:50 z:0 rot:0 scale:1.2
![mod](model.png)

--- #o0 x:0 y:-220 z:600 rot:0 scale:1

--- #tools x:0 y:900 z:0 rot:0 scale:2

## Every BIG question needs **small tools**.

--- #t1 x:-350 y:1200 z:0 rot:0 scale:1.2
- ChIP-<b style="color: red;">seq</b>
- RNA-<b style="color: red;">seq</b>
- DNase-<b style="color: red;">seq</b>
- MNase-<b style="color: red;">seq</b>
- ATAC-<b style="color: red;">seq</b>

--- #rad x:-350 y:1650 z:0 rot:0 scale:1 .red
<img src="Red_Arrow_Down.svg" alt="rad" hight=80px, width=80px style="margin-left:50px; margin-bottom:40px">
<br>
<p>1. DNA library</p>
<p>2. Short reads</p>
<p>3. <b>Genomic position</b></p>


--- #problem x:300 y:1100 z:0 rot:0 roty:90 scale:1.2 .sm .hide
<span class=red>Technical problem</span> – typical experiment produce **tens of 
millions** of such positions over **hundreds of millions to billions** possible
locations (base pairs) in the genome!

--- #solution1 x:300 y:1450 z:0 rot:0 scale:1 
<u>Solutions:</u>
- Shrink/simplify the data so they are small enough for us to understand (e.g. peak calls, unsupervised machine learning) 

--- #solution2 x:300 y:1750 z:0 rot:0 scale:1
- Use <b>data visualization</b> to make an original comprehensible to us

--- #o1 x:0 y:1400 z:600 rot:0 scale:1




--- #vis x:0 y:2400 z:0 rot:0 scale:2
## Scientific data visualization – is it important?

--- #v1 x:0 y:2650 z:0 rot:0 scale:2 .sm
- Data visualization is <b class="zzz">prevalent approach</b> in science

--- #v1a x:-1000 y:2650 z:300 roty:90 scale:1 .md
![](heatmap.jpg)
Shaded matrix display from Loua (1873).

--- #v2 x:0 y:3000 z:0 rot:0 scale:2.0 .sm
- Since the advent of sequencing techniques there is **great advance** in methods specific to this field 
- Helps us to **better understand the data** and find the patterns that might be lost due to shrinkage/simplification
- Great for **exploratory data analyses**
- Very useful for **results presentation**


--- #o2 x:-200 y:2800 z:600 rot:0 scale:1




--- #stat x:0 y:3900 z:0 rot:0 scale:3 .sm .hide
## We can visualize reads directly, but usually more useful is **converting them to a read coverage**

--- #statp1 x:-300 y:4600 z:200 rot:0 scale:1.5
![](readscov.png)
<br />
![](covarrow.png)

--- #statp2 x:100 y:5200 z:0 rot:0 scale:1.5
![](trackscov.png)

--- #o3 x:0 y:4600 z:1200 rot:0 scale:1






--- #global x:3000 y:-2300 z:0 scale:2 
## <span class='red'>*-seq</span> data visualization:<br/>global approaches.

--- #circos x:3000 y:-1700 z:0 scale:1.2
![plot of chunk circos](assets/fig/circos-1.svg) 

--- #hibo x:3000 y:-1900 z:600 scale:1



--- #gb x:3000 y:-900 z:0 scale:2
## <span class='red'>*-seq</span> data visualization:<br />genome browsers.

--- #ucsc x:2650 y:-500 z:0 scale:1 
UCSC Genome Browser
![](ucsc.png)

--- #igv x:3350 y:-500 z:0 scale:1
IGV (Broad Institute)
![](igv.png)

--- #biod x:2675 y:0 z:0 scale:1.05
Biodalliance (Thomas Down)
![](biodalliance.png)

--- #biod x:3000 y:-100 z:0 scale:1.5

--- #gbo x:3000 y:-400 z:600 scale:1








--- #trf x:3000 y:2400 z:0 scale:2
## <span class='red'>*-seq</span> data visualization:<br />multiple parts of genome, using pre-defined genomic features
<hr/>

--- #av x:3000 y:3100 z:0 scale:2  .sm .cent
![plot of chunk aver](assets/fig/aver-1.svg) 

--- #hm x:3000 y:3920 z:0 scale:2  .sm .cent
![plot of chunk heatmap](assets/fig/heatmap-1.png) 

--- #osp x:3000 y:3250 z:1500 scale:1


--- #ngsp1 x:2550 y:5000 z:0 scale:1.2  .sm .cent
Command line tools, e.g. ngsplot
<hr/>
![](nsgp1.png)
<br /><br />
![](ngsp2.png)

--- #dt1 x:3550 y:5000 z:0 scale:1.2 .sm .cent
Tools on Galaxy platform: deepTools, Cistrome, etc.
<hr/>
<img src="dt1.png" alt="" height="336px">
<img src="dt2.png" alt="">



--- #logo x:3000 y:1300 scale:4
![plot of chunk logo](assets/fig/logo-1.svg) 







--- #why x:6000 y:-2200 scale:3 .cent

## Why do we need **yet another** visualization tool?
<hr />

--- #why1 x:6000 y:-1600 scale:2 .md
Existing solutions did not meet our requirements:
- Custom scripts and pargramic languages labraries allows to run things in batch, 
  but are **too complicated** to run for users without IT expertise
- Even with good training these tools **requires a lot of time** to code
- Galaxy/Cistrome was too **slow** and **not configurable** enough 
  (plus **data privacy** problem!)

<hr />


--- #why2 x:6000 y:-1000 scale:2 .cent .md
I want take the best from two worlds - connect the **intuitiveness** and **interactiveness** of genome browsers with **visualization power** of plotting 1000s of  genomic features at once.


--- #why3 x:6000 y:-500 scale:2 .cent .lg
<hr />
Goal: **fast**, **intuitive** software for **exploratory data analyses**!
<hr />

--- #seqplots x:6000 y:-50 scale:3 .cent
## SeqPlots is **this** software!

--- #spim x:6000 y:900 scale:2 .cent .md
<hr />
We developed a highly configurable, **GUI operated web application** for **rapidly generating** sets of publication quality **linear plots** and **heatmaps**. 
<hr />
<img src="sp.png" alt="sp" height=600px>




--- #waod x:6000 y:2100 scale:2.5 .lg .cent
**See SeqPlots in action on the movie...**
<hr />

--- #task x:6900 y:2800 scale:1 .slide z:380 roty:-90
## **Quick explanaton of the example in hand**
<hr />

**Files - signal profiles from ChIP-seq experiments:**
- H3K4me3 (mark active promoters)
- H3K36me3 (mark transcribed regions of active genes)
- HTZ1 (histon variant, *C. elegans* homolog of H2A.Z)

<hr />

**Files - genomic features:**
- *C. elegans* transcription start sites (TSS), divided into 5 expression bins 
  based on RNA-seq data

<hr />

**Tasks:**
- Compare histone marks between highly and lowly expressed genes.
- Check if CpG (CG-dinucleotide) occupancy is higher on transcription start sites (TSS) relative to local neighborhood

<hr />



--- #vid x:6000 y:2800 scale:1.8 .lg .cent
<iframe width="840" height="600" src="https://www.youtube.com/embed/9TKYZQa1Ykw?vq=hd720&rel=0&amp;showinfo=0" frameborder="0" allowfullscreen></iframe>

--- #spaccs x:6000 y:3900 scale:2 .lg
<hr />
The app is available as:

- **R package** from Bioconductor 
- **Mac OS X app**
- **Server deployment** with Shiny Server
- **Web service** (shinyapps.io, Amazon EC2, etc.) 

<hr />

--- #clust x:5900 y:5000 scale:1.5
![](last.png)

