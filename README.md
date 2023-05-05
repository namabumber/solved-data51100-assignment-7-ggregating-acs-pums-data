Download Link: https://assignmentchef.com/product/solved-data51100-assignment-7-ggregating-acs-pums-data
<br>
5/5 - (1 vote)

Aggregating ACS PUMS Data

For this assignment, you will work again with the same ACS PUMS dataset as for assignment 6 to produce several tables which aggregate the data.

Note: For this assignment, you are free to program in any programming language of your choice; Python, R, Matlab, C++, Java,..etc. Please indicate the programming language you will use.

Requirements

You are to create a program in Python that performs the following using the pandas packages:

<ol>

 <li>Loads the ss13hil.csv file that contains the PUMS dataset (assume it’s in the current directory) and create a DataFrameobject from it if you use Python.</li>

 <li>Create 3 tables:TABLE 1: Statistics of HINCP – Household income (past 12 months), grouped by HHT – Household/family type

  <ul>

   <li>Table should use the HHT types (text descriptions) as the index</li>

   <li>Columns should be: mean, std, count, min, max</li>

   <li>Rows should be sorted by the mean column value in descending orderTABLE 2: HHL – Household language vs. ACCESS – Access to the Internet (Frequency Table)</li>

  </ul>

  <ul>

   <li>Table should use the HHL types (text descriptions) as the index</li>

   <li>Columns should be the text descriptions of ACCESS values</li>

   <li>Each table entry is the sum of WGTP column for the given HHL/ACCESS combination, divided by the sum of WGTPvalues in the data. Entries need to be formatted as percentages.</li>

   <li>Any rows containing NA values in HHL, ACCESS, or WGTP columns should be excluded.TABLE 3: Quantile Analysis of HINCP – Household income (past 12 months)</li>

  </ul>

  <ul>

   <li>Rows should correspond to different quantiles of HINCP: low (0-1/3), medium (1/3-2/3), high (2/3-1)</li>

   <li>Columns displayed should be: min, max, mean, household_count</li>

   <li>The household_count column contains entries with the sum of WGTP values for the corresponding range of HINCPvalues (low, medium, or high)</li>

  </ul></li>

 <li>Display the tables to the screen as shown in the sample output on the last page.</li>

 <li>Note: For this assignment, you are free to program in any programming language of your choice; Python, R, Matlab, C++, Java,..etc. Please indicate the programming language you will use.</li>

</ol>

Additional Requirements

<ol>

 <li>The name of your source code file should be tables.py for Python (or tables.m (for Matlab), tables.java (For Java, or tables.r (For R),..etc). All your code should be within a single file.</li>

 <li>You need to use the pandas DataFrame object for storing and manipulating data (if you use Python).</li>

 <li>Your code should follow good coding practices, including good use of whitespace and use of both inline and block comments.</li>

 <li>You need to use meaningful identifier names that conform to standard naming conventions.</li>

 <li>At the top of each file, you need to put in a block comment with the following information: your name, date, course name,semester, and assignment name.</li>

 <li>The output should exactly match the sample output shown on the last page.</li>

</ol>

What to Turn InYou will need to turn in the single tables.py (or tables.m (for Matlab), or tables.java (For Java), or tables.r (For R),..etc) file as well as a screen shot of the created tables using BlackBoard.

HINTS

<ul>

 <li>To get the right output, use the following functions to set pandas display parameters in Python: pd.set_option(‘display.max_columns’, 500) pd.set_option(‘display.width’, 1000)</li>

 <li>To display entries as percentages, use the applymap method, giving it a string conversion function as input. The string conversion function should take a float value v as an input and output a string representing v as a percentage. To do this, you can use the format() method</li>

</ul>

Sample Program Output

<pre>DATA-51100, [semester] [year]NAME: [put your name here]PROGRAMMING ASSIGNMENT #7</pre>

*** Table 1 – Descriptive Statistics of HINCP, grouped by HHT ***

HHT – Household/family typeMarried couple householdNonfamily household:Male householder:Not living aloneNonfamily household:Female householder:Not living aloneOther family household:Male householder, no wife presentOther family household:Female householder, no husband present 49638.428821 Nonfamily household:Male householder:Living alone 48545.356298 Nonfamily household:Female householder:Living alone 37282.245015

*** Table 2 – HHL vs. ACCESS – Frequency Table *** sum

<pre>                                             WGTPACCESS                             Yes w/ Subsrc.</pre>

HHL – Household languageEnglish only 58.71% Spanish 7.83%

<pre>Yes, wo/ Subsrc.      No</pre>

<pre>           2.93%  16.87%           0.52%   2.60%           0.18%   1.19%           0.06%   0.28%           0.03%   0.14%</pre>

Other Indo-European languagesAsian and Pacific Island languagesOther languageAll 75.19%

*** Table 3 – Quantile Analysis of HINCP – Household income (past 12 months) *** min max mean household_count

HINCPlow -11200 37200 19599.486904 medium 37210 81500 57613.846298 high 81530 1425000 159047.588900

<pre>162949915754811578445</pre>

<pre>5.11%2.73%0.80%</pre>

<pre>106790.565562 79659.567376 69055.725901 64023.122122</pre>

3.73%

21.08%

mean

std

<pre>  100888.917804   74734.380152   63871.751863   59398.970193   48004.399101   60659.516163   44385.091076</pre>

All

<pre> 78.51% 10.95%  6.48%  3.08%  0.97%100.00%</pre>

count min

25495 -5100 1410 0 1193 0 1998 0 5718 -5100 5835 -5100 8024 -11200

max

<pre>1425000 625000 645000 610000</pre>