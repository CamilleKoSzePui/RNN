# Experiments RNN

|exp|depth|max_length|Seq_len|Model|lrate|BATCHSIZE|EPOCH|Optimizer|Criterion|loss|val_loss|MAE|MAPE|MDAP|MSE|RMSE|r2|
|---|-----|----------|-------|---|-----|---------|-----|---------|---------|----|--------|---|----|----|---|----|--|
|1. |  3  |     1783 |  100|Simple|0.001|	32|	50|	Adam|	MSE|  0.0126|	  0.0113|37.56|	6.72|5.79||||
|   |  3  | 	1783 |  100|  LSTM|0.001|	32|	50|	Adam|	MSE|1.20E-03|	1.70E-03| 48.5|	2.34|1.91||||		
|   |  3  |     1783 |	100|   GRU|0.001|	32|	50|	Adam|	MSE|1.20E-03|	1.50E-03|45.09|	2.19|1.61||||
|2. |  3  |     1783 |	 50|Simple|0.001|	32|	50|	Adam|	MSE|8.70E-03|	   0.004|86.19|	4.35|3.64|||0.8132390108|
|   |  3  |     1783 |	 50|  LSTM|0.001|	32|	50|	Adam|	MSE|1.10E-03|	2.10E-03|57.23|	2.70|2.39|||0.9194633207|
|   |  3  |     1783 | 	 50|   GRU|0.001|	32|	50|	Adam|	MSE|9.43E-04|	1.80E-03|53.11|	2.52|2.20|||0.9310838756|
|2a |  3  |     1783 |	   |Simple|	|	  |	  |	    |	   |2.60E-03|.  3.20E-03|70.39|	3.37|2.79|clipiping value = 0.5|||
|   |  3  |     1783 |     |  LSTM|	|	  |	  |	    |	   |1.10E-03|	2.10E-03|57.30|	2.70|2.40||||		
|   |  3  |     1783 |     |   GRU|	| 	  |	  |	    |	   |9.44E-04|	1.80E-03|53.12| 2.52|2.21||||		
|3. |  3  |     1783 |   20|Simple|0.001|	32|	50|	Adam|	MSE|	0.002|	0.0022|55.62156913|2.698406571|2.151738406|||0.9153807844|
|.  |  3  |     1783 |   20|  LSTM|0.001|	32|	50|	Adam|	MSE|	0.0013|	0.0018|50.16|2.41|1.93|||0.9328273009|
|.  |  3  |     1783 |   20|   GRU|0.001|	32|	50|	Adam|	MSE|	9.20E-04|0.0015|46.42|	2.24|	1.71|||	0.9420456131|
|4. |  3  |     1783 |    5|Simple|0.001|	32|	50|	Adam|	MSE|	0.0021|	0.0028|	61.51|	 2.98|	2.34|||0.8951874147|
|.  |  3  |     1783 | 	  5|  LSTM|0.001|	32|	50|	Adam|	MSE|	0.0021|	0.0037|	74.86|	3.61|	 2.87|||0.8606880266|
|.  |  3  |     1783 |	  5|   GRU|0.001|	32|	50|	Adam|	MSE|	0.0012| 0.0018|	49.59|	2.41 |	1.95|||0.9308900793|
|5. |  3  |     1783 | 	100|Simple|0.001|	985|	50|	Adam|	MSE|	3.59E-02|0.0292|2.16E+02|9.91798547|	9.444998141|	70224.69593|	264.9994263|	batch size issue||| 
|.  |  3  |	1783 |  100|  LSTM|0.001|	985|	50|	Adam|	MSE|	3.70E-03|7.60E-03|112.5445641|	5.327169276|	4.780164582|	18654.4124|	136.5811568|||
|.  |  3  |	1783 |  100|   GRU|0.001|	985|	50|	Adam|	MSE|	1.90E-03|3.00E-03|65.5083509|	3.213933722|	2.611886911|	7478.678576|	86.47935347|||	
|6. |  3  |     1783 |  200|Simple|0.001|	32|	50|	Adam|	MSE|	0.0329|	0.0207|	190.3414664|	9.283580649|	9.022375207|	||||		
|.  |  3  |     1783 |	200|  LSTM|0.001|	32|	50|	Adam|	MSE|	0.0011|	0.0018|	52.55|	2.5|2.09|||||			
|.  |  3  |     1783 |	200|   GRU|0.001|	32|	50|	Adam|	MSE|	9.38E-04|0.0018|52.11|	2.47|2.11|	||||		
|7. |  9  |     1783 |   50|Simple|0.001|	32|	50|	Adam|	MSE|	0.0283|	0.0311|	225.3|	10.44|9.86| 	||||		
|.  |  9  |     1783 |	 50|  LSTM|0.001|	32|	50|	Adam|	MSE|	0.0022|	0.0036|	76.39|	3.56|3.34|	||||		
|.  |  9  |     1783 |   50|   GRU|0.001|	32|	50|	Adam|	MSE|	0.0012|	0.002|	56.03|	2.65|2.35|	|||		
|7a |  9  |     1783 |	   |Simple|	|	|	|		||		|	|166.2342648|	7.785481713|	7.704468359	|clipping value = 0.5	|||	
|.  |  9  |     1783 |	   |  LSTM|	|	|	|		||	0.002|	0.0037|	76.84238639|	3.570454926|	3.290196716			|||0.9971744698|
|.  |  9  |     1783 |	   |   GRU|	|	|	|		||	0.0012|	0.0019|	53.8626307|	2.550806588|	2.273683388			
|8. |     |     1783 |	   |Regression|	|	| 	|		||		|	|		10.89|	 0.58 |0.43 |	224.6492167	|14.98830266	|||99.7|
|8a |     |     1783 |	   |Regression|	|	|	|		||		|	|			109.9369001|	5.401495771	|	4.15091175|	||	0.6694181474|
