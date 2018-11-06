# pChart
A PHP Class to build Charts

pChart is a PHP class oriented framework designed to create aliased charts. Most of todays chart libraries have a cost, our project is intended to be free. Data can be retrieved from SQL queries, CSV files, or manually provided. This project is still under development and new features or fix are made every week. 


[![Build Status](https://travis-ci.org/wp-statistics/pchart.svg?branch=master)](https://travis-ci.org/wp-statistics/pchart)
[![Minimum PHP Version](http://img.shields.io/badge/php-%3E%3D%205.4-8892BF.svg)](https://php.net/)
[![Latest Stable Version](https://poser.pugx.org/wp-statistics/pchart/v/stable)](https://packagist.org/packages/wp-statistics/pchart)
[![Total Downloads](https://poser.pugx.org/wp-statistics/pchart/downloads)](https://packagist.org/packages/wp-statistics/pchart)
[![Latest Unstable Version](https://poser.pugx.org/wp-statistics/pchart/v/unstable)](https://packagist.org/packages/wp-statistics/pchart)
[![License](https://poser.pugx.org/wp-statistics/pchart/license)](https://packagist.org/packages/wp-statistics/pchart)


Installation
------------

The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

Either run

```
composer require wp-statistics/pchart
```

to the require section of your `composer.json` file.


Usage
-----

Let's add into config in your main-local config file before return[]
````php
<?php
require_once __DIR__ . '/../vendor/autoload.php'; // Autoload files using Composer autoload

use pChart\pData;
use pChart\pChart;
use pChart\pCache;

// Dataset definition
$DataSet = new pData;
$DataSet->AddPoint(array(1, 4, 3, 2, 3, 3, 2, 1, 0, 7, 4, 3, 2, 3, 3, 5, 1, 0, 7));
$DataSet->AddSerie();
$DataSet->SetSerieName("Sample data", "Serie1");

// Initialise the graph
$Test = new pChart(700, 230);
$Test->setFontProperties("Fonts/tahoma.ttf", 10);
$Test->setGraphArea(40, 30, 680, 200);
$Test->drawGraphArea(252, 252, 252, TRUE);
$Test->drawScale($DataSet->GetData(), $DataSet->GetDataDescription(), SCALE_NORMAL, 150, 150, 150, TRUE, 0, 2);
$Test->drawGrid(4, TRUE, 230, 230, 230, 70);

// Draw the line graph
$Test->drawLineGraph($DataSet->GetData(), $DataSet->GetDataDescription());
$Test->drawPlotGraph($DataSet->GetData(), $DataSet->GetDataDescription(), 3, 2, 255, 255, 255);

// Finish the graph
$Test->setFontProperties("Fonts/tahoma.ttf", 8);
$Test->drawLegend(45, 35, $DataSet->GetDataDescription(), 255, 255, 255);
$Test->setFontProperties("Fonts/tahoma.ttf", 10);
$Test->drawTitle(60, 22, "My pretty graph", 50, 50, 50, 585);
$Test->Render("Naked.png");
````


Screenshots
------------
The pChart charting library is providing many ways to reprensent a single or multiple series of data. We'll try to add screenshots everytime an interesting functionnality is added to the pChart library. 
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example10.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example12.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example13.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example14.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example15.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example16.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example17.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example18.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example19.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example2.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example20.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example21.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example22.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example23.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example24.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example25.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example26.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example3.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example4.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example5.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example6.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example7.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example8.png "Logo Title Text 1")
![alt text](https://raw.githubusercontent.com/wp-statistics/pchart/master/src/Examples_Images/example9.png "Logo Title Text 1")
