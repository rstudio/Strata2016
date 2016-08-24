
Strata2016
==========

Materials for Nathan and Garrett's tutorial R for Big Data

R for big data
==============

Slides to repurpose: <https://www.dropbox.com/sh/thz33i0zfgfnm9w/AAB4l1NcaKFqkOD2gj36eDNya?dl=0>
------------------------------------------------------------------------------------------------

Key concepts
------------

### Scope: Big data

-   R is an excellent big data solution
-   Connecting to relational databases
-   Working with data at scale in spark
-   Using dplyr for data hygiene/tidy (big data best practices)
-   spark, rdbms, R
-   Toolchain: Data &gt; model building &gt; sharing
-   Introduce notebooks: Do everything in notebooks

Intro to R and dplyr (slides: Garrett)
--------------------------------------

> No matter how complex and polished the individual operations are, it is often the quality of the glue that most directly determines the power of the system. — Hal Abelson.

1.  R
    1.  R is both tools and a glue, and it is a very good glue.
        1.  Preview of R's tools
        2.  Role of R as an interface between languages
        3.  Preview of the RStudio tool chain (*details in proportion to the lack of context here*)

2.  tidyverse
    1.  Introduction to the R package system
    2.  Like many mature languages, R contains legacy tools that you should avoid. Some of these tools were not designed for big data.
    3.  The tidyverse encapsulates the most modern tools that work best with big data. The tidyverse is R + organization + best practices.
        1.  The tidyverse is all open source and free

3.  dplyr
    1.  dplyr an R package
    2.  not only is dplyr the main tool in the tidyverse, dplyr is the glue between R and big data
    3.  have students open an R Markdown document, demonstrate notebook interface and exporting results as nb.html.
    4.  Teach
        1.  `select()`
        2.  `filter()`
        3.  `mutate()`
        4.  `summarise()`
        5.  `left_join()`
        6.  `right_join()`
        7.  `inner_join()`
        8.  `full_join()`
        9.  `%>%`

    5.  Segue exercise to big data?
    6.  Also dissect modeling code and ggplot code?

Big data (slides: Garrett)
--------------------------

1.  R and Big data
    1.  R copies data into RAM, which has advantages, but it also creates a fundamental limit on the size of data that you can evaluate in R
        1.  But keep in mind, you can put a lot of RAM on a machine (1 TB)

    2.  What do you do when you have more data than can fit into RAM? Keep it outside of RAM. Today we will look at two options. There are other ways as well.
        1.  RDBMS
        2.  Spark (compare)

SQLite exercise (nycflights13) (slides: Nathan?)
------------------------------------------------

1.  What is relational database?
    1.  tabular data with indexes
    2.  can be multinodal
    3.  Invented 50 years ago

2.  Introduce the flights data set
    1.  The SQL exercise from 2015

Spark intro
-----------

1.  What is Spark?
    1.  Analytic engine (not a database!) (like R)
    2.  Distributed / multi-nodal in memory (like R)
    3.  You can run SQL and machine learning (like R)
    4.  Run interactive analyses (like R)
    5.  Handles semi-structured data (like R)
    6.  Handles streaming data (we're still working on this)
    7.  Runs two modes (1) cluster (typically hadoop) (2) lol (talk about architecture)

2.  Explain technologies
    1.  Hadoop, HDFS, Hive, Spark, (show architecture)
    2.  then talk about R, Sparklyr, and RStudio Server

3.  Sparklyr
    1.  dplyr
    2.  Spark SQL
    3.  Spark ML
    4.  What about sparkr? Jeff's slides (from UseR!)

Spark demo (full flights data set)
----------------------------------

1.  [Spark Demo](https://beta.rstudioconnect.com/content/1409/sparkClusterDemo.html)
2.  Provision cluster
3.  Connect to data
4.  Run Spark SQL
5.  Run Spark ML

Spark exercises (nycflights13 data set)
---------------------------------------

1.  Student exercise (local)

Communicating
-------------

1.  Media
    1.  Flexdashboard (interactive)
    2.  Shiny app
    3.  Notebook
    4.  Slideshows
    5.  R Markdown document / email

2.  Platform
    1.  RSC

Conclusion: Toolchain Demo
--------------------------

*from Roger*

[Toolchain images](https://beta.rstudioconnect.com/connect/#/apps/1416)
