<h1>OPDSGen</h1>
Simple PHP OPDS Generator
<h3>Introduction:</h3>
OPDSGen is a web front-end html generator, as well as an opds xml generator. It is designed specifically for use in ebookpub.org. Written in PHP with JavaScript, without any back-end database, it is designed to be small and simple for catalogs that contain no more than a few thousand items. It supports all the major languages of the world.<br />

<h3>How to Install:</h3>
1) Download the zip file containing the latest version of OPDSGen from code.google.com/p/opdsgen.<br />
2) Using ftp, copy opdsgen folder and its entire contents into the parent directory of your top opds folder on your website.<br />
3) Using your web browser open {your-site}/opdsgen/add.php. This will create the books folder which will be at the same level as the opdsgen folder, e.g. {your-site}/books. This folder is the root folder for your book catalog.<br />
4) When you use add.php for the first time, you will be prompted for an admin password.

<h3>How to Generate your HTML and XML files:</h3>
5) Open a new spreadsheet so that you have nine columns for the following fields: {lang}	{dept}	{section}	{subsection}	{title}	{author}	{year}	{description} {filename}<br />
6) Enter the details of your books to be uploaded under the relevant columns in your spreadsheet. For example:
<pre>
english	literature	19th-century	romance	Pride and Prejudice	Jane Austen	1813	The story follows the main character Elizabeth Bennet as she deals with issues of manners, upbringing, morality, education, and marriage in the society...	austen_prideandprejudice.epub<br>
tagalog	ingles panitikan	ika-19 siglo	kuwento-ng-pag-iibigan	Pagmamalaki at Pinsala	Jane Austen	1813	Pagmamalaki at pinsala ay isang nobelang sa pamamagitan ng Jane Austen... 	austen_pagmamalakiatpinsala.epub<br>
</pre>
Note that where the value contains character values greater than ascii 127 in the {lang}, {dept}, {section}, {subsection}, {title}, or {author} fields, their non-accented latin alphabet values should be provided after a forward slash '/'. Filenames should be in non-accented latin letters and/or numerals only. For example:
<pre>
français/francais	littérature/litterature	19e-siècle/19e-siecle	romance	Les Trois Mousquetaires	Alexandre Dumas	1844	Les Trois Mousquetaires est un roman d’Alexandre Dumas et d’Auguste Maquet...	dumas_lestroismousquetaires.epub<br>
中文繁體/zhong1wen2fan2ti3	文學/wen2xue2	十四世紀/shi2si4shi4ji4	經典小說/jing1dian3xiao3shuo1	水滸傳/shui2hu2chuan2	施耐庵/shi1nai4an1	14th-C	《水滸傳》是中國歷史上以白話文寫成的章回小說、被候...	shinaian_shuihuchuan_fanti.epub<br>
中文简体/zhong1wen2jian2ti3	文学/wen2xue2	十四世纪/shi2si4shi4ji4	经典小说/jing1dian3xiao3shuo1	水浒传/shui2hu2chuan2	施耐庵/shi1nai4an1	14th-C	《水浒传》是中国历史上以白话文写成的章回小说、被候人...	shinaian_shuihuchuan_jianti.epub<br>
</pre>
7) To add books into your catalog, create a folder on your local computer with the named using date-time format 'mmdd' under the folder 'YYYY'. For example if today is 1st July 2013, create a folder called 2013 on your computer, and underneath the 2013 folder, create a folder called 0701. All the books to be uploaded to your website into the 0701 folder. In the above example, one would copy the five files: austen\_prideandprejudice.epub, austen\_pagmamalakiatpinsala.epub, dumas\_lestroismousquetaires.epub, shinaian\_shuihuchuan\_fanti.epub, and shinaian\_shuihuchuan\_jianti.epub into the 0701 folder underneath the 2013 folder.<br />
8) Ftp the folder and its subfolder named 'YYYY/mmdd', e.g. '2013/0701' with all its contents to {your-site}/books folder on your webserver.<br />
9) Copy and paste data from the nine columns into the textarea in add.php<br />
10) enter the uploaded folder and subfolder 'YYYY/mmdd' path in the textfield in add.php, e.g. '2013/0701', and then click on submit<br />
11) If no errors were encountered, your HTML pages will be generated at {your-site}/main/index.html, and your OPDS root XML will be generated at {your-site}/main/opds.xml<br />
12) To add new books to your website, and OPDS catalog, simply follow above steps 6 to 11.<br />
