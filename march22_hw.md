#### Informal response from class on March 22

For each of the following three steps you only need to download the administrative subdivisions, and their associated files not complete the entire exercise.

Download the administrative subdivision for your selected country.

- Philippines
- Plot produced:

Regions:

<img src="https://user-images.githubusercontent.com/54942759/112571396-51c37a00-8dbe-11eb-8eb9-40d5d789762c.png" width = 600/>

Download the population raster from Worldpop for your selected county 

Download the 12 rasters from your selected country and stack them. 

Produce a raster stack and calculate summary statistics using the script posted to our slack channel

- Output summary statistics table for ADM 3: [link](march22hw_sumstats_adm3.csv)
    - There are 41,949 rows in this table so I won't include all of them but here are the first ten: 
    
|FIELD1|sum.water       |sum.lulc.dst011  |sum.lulc.dst040 |sum.lulc.dst130 |sum.lulc.dst140 |sum.lulc.dst150 |sum.lulc.dst160 |sum.lulc.dst190 |sum.lulc.dst200|sum.topo        |sum.slope       |sum.ntl         |sum.pop19       |mean.water       |mean.lulc.dst011  |mean.lulc.dst040|mean.lulc.dst130|mean.lulc.dst140|mean.lulc.dst150|mean.lulc.dst160|mean.lulc.dst190|mean.lulc.dst200|mean.topo       |mean.slope       |mean.ntl          |mean.pop19      |
|------|----------------|-----------------|----------------|----------------|----------------|----------------|----------------|----------------|---------------|----------------|----------------|----------------|----------------|-----------------|------------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|----------------|-----------------|------------------|----------------|
|1     |426.099822998047|-818.522888183594|1406.63146972656|16142.931640625 |10158.4228515625|2505.89916992188|6279.99853515625|855.418090820312|266730.375     |16547.880859375 |774.460998535156|70.460807800293 |1840.00964355469|1.1785968542099  |-2.26404356956482 |3.8907585144043 |44.6515312194824|28.0983123779297|6.93134498596191|17.3705463409424|2.36609601974487|737.779235839844|45.7716255187988|2.14216780662537 |0.194895386695862 |257.882019042969|
|2     |439.761749267578|-385.65234375    |1490.69421386719|12549.2490234375|7719.26953125   |2243.6669921875 |4714.6416015625 |420.506225585938|212566.796875  |12377.03125     |717.349792480469|87.0103988647461|1801.4658203125 |1.52277326583862 |-1.33540737628937 |5.16186141967773|43.4545783996582|26.7296943664551|7.76919794082642|16.3254985809326|1.45609676837921|736.059997558594|42.8582344055176|2.48398375511169 |0.301292926073074 |108.872886657715|
|3     |153.400726318359|-128.975799560547|949.700378417969|15787.33203125  |9552.498046875  |1280.09094238281|4739.20751953125|687.797607421875|265158.40625   |12573.125       |323.758758544922|22.2653617858887|1008.01483154297|0.423068970441818|-0.355706632137299|2.6192102432251 |43.5404090881348|26.3451519012451|3.53040528297424|13.0704174041748|1.89689981937408|731.289184570312|34.675838470459 |0.892905056476593|0.0614063814282417|336.004943847656|
|4     |171.567718505859|-155.640838623047|870.020629882812|8994.7158203125 |5395.0517578125 |1059.83227539062|2816.611328125  |309.226379394531|154114.6875    |8063.3017578125 |196.207962036133|41.193675994873 |1265.87329101562|0.815269112586975|-0.739586472511292|4.13423299789429|42.7418060302734|25.6366348266602|5.03619527816772|13.3841972351074|1.46940648555756|732.334411621094|38.3158378601074|0.932356536388397|0.195747375488281 |214.163360595703|
|5     |181.42529296875 |-97.4529037475586|1227.87219238281|13863.2802734375|8477.3134765625 |1409.90173339844|4460.06787109375|574.358947753906|231013.796875  |11061.947265625 |263.601287841797|68.6645355224609|997.574584960938|0.575619220733643|-0.309194833040237|3.89574575424194|43.9848823547363|26.8964958190918|4.47328233718872|14.1507320404053|1.82230401039124|732.951721191406|35.096923828125 |0.836344063282013|0.217856198549271 |88.0114212036133|
|6     |66.8384170532227|-70.8737487792969|490.310638427734|5018.35791015625|2965.59301757812|672.322143554688|1551.25915527344|183.582870483398|88076.46875    |5475.3857421875 |164.229476928711|52.7696762084961|2373.2763671875 |0.555789351463318|-0.58934485912323 |4.07713794708252|41.7297439575195|24.6601448059082|5.59063959121704|12.8993682861328|1.52656829357147|732.392639160156|45.5301208496094|1.36563670635223 |0.438801914453506 |156.969192504883|
|7     |1819.38513183594|-1407.66772460938|1602.32104492188|21666.59765625  |13227.146484375 |3293.47119140625|8883.29296875   |2063.46118164062|381241.625     |26551.427734375 |963.355651855469|55.5007209777832|0               |3.52037239074707 |-2.72373032569885 |3.10036993026733|41.923225402832 |25.59352684021  |6.37261724472046|17.1884994506836|3.99264097213745|737.673645019531|51.375          |1.86402022838593 |0.107389688491821 |NA              |
|8     |472.200439453125|-391.278259277344|940.734252929688|7951.14453125   |4790.86572265625|1526.76599121094|2978.466796875  |410.106506347656|139752.90625   |6917.93798828125|113.119201660156|39.8349685668945|0               |2.48643493652344 |-2.06032824516296 |4.95356273651123|41.8678207397461|25.2269458770752|8.03939151763916|15.6835165023804|2.15947079658508|735.8876953125  |36.4273300170898|0.595644354820251|0.209756374359131 |NA              |
|9     |347.178894042969|-180.461853027344|945.157531738281|7012.76708984375|4202.302734375  |1248.14819335938|2481.9775390625 |198.546997070312|122915.390625  |8677.169921875  |516.134521484375|126.566474914551|1553.01513671875|2.07552266120911 |-1.07884633541107 |5.65038919448853|41.9240837097168|25.1224212646484|7.46174335479736|14.8378858566284|1.1869637966156 |734.819091796875|51.8743019104004|3.08558177947998 |0.75664621591568  |33.5256881713867|
|10    |118.839797973633|-129.488967895508|1018.28582763672|10799.3291015625|6317.591796875  |1451.88891601562|3388.13232421875|491.403137207031|193160.875     |16416.7578125   |1206.55334472656|122.953071594238|772.183715820312|0.450833052396774|-0.491231948137283|3.86298942565918|40.9685516357422|23.9665431976318|5.50791501998901|12.8532867431641|1.86419677734375|732.778991699219|62.2789421081543|4.57720470428467 |0.466437220573425 |8.67860126495361|

- Output summary statistics table for regions (ADM 0):

|FIELD1|sum.water     |sum.lulc.dst011|sum.lulc.dst040|sum.lulc.dst130|sum.lulc.dst140|sum.lulc.dst150|sum.lulc.dst160|sum.lulc.dst190|sum.lulc.dst200|sum.topo  |sum.slope    |sum.ntl      |sum.pop19  |mean.water      |mean.lulc.dst011   |mean.lulc.dst040  |mean.lulc.dst130|mean.lulc.dst140|mean.lulc.dst150|mean.lulc.dst160|mean.lulc.dst190  |mean.lulc.dst200|mean.topo       |mean.slope      |mean.ntl          |mean.pop19      |
|------|--------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|---------------|----------|-------------|-------------|-----------|----------------|-------------------|------------------|----------------|----------------|----------------|----------------|------------------|----------------|----------------|----------------|------------------|----------------|
|1     |6615386.5     |701627.125     |1229887.5      |906792640      |269461792      |90801480       |9806649        |16307588       |2433041664     |631871360 |9324261      |89886.1953125|982460.4375|4.40054655075073|0.466721445322037  |0.818119525909424 |603.197265625   |179.245635986328|60.4010238647461|6.52336978912354|10.847785949707   |1618.4560546875 |420.320007324219|6.20248603820801|0.0597921796143055|50.8912544250488|
|2     |18580814      |-109769.953125 |1935951.375    |122864136      |161211696      |26915302       |18455908       |40483360       |1744955008     |1792779904|37183536     |215434.375   |1448149.125|8.34243297576904|-0.0492846295237541|0.869205474853516 |55.1636695861816|72.3809967041016|12.0844602584839|8.28635311126709|18.1762619018555  |783.451721191406|804.924194335938|16.6947021484375|0.0967259481549263|95.7804946899414|
|3     |121821.2109375|92734.4375     |294777.6875    |14236649       |6748037.5      |342720.375     |330645.78125   |-45582.12890625|69726672       |2235754.25|103142.703125|1602035.75   |13137207   |1.68946540355682|1.28607833385468   |4.08809518814087  |197.439559936523|93.5844879150391|4.75298357009888|4.58552837371826|-0.632151246070862|966.997436523438|31.0063362121582|1.43042433261871|22.2176742553711  |203.025573730469|
|4     |7392309.5     |-4625005.5     |7214389        |1027736000     |102538952      |22281228       |15327642       |16820750       |2108244352     |435035360 |11948107     |348915       |3951019    |4.86765813827515|-3.04545497894287  |4.75050210952759  |676.739501953125|67.5194396972656|14.6716537475586|10.0928840637207|11.076060295105   |1388.22827148438|286.460327148438|7.86754179000854|0.229752153158188 |94.1405944824219|
|5     |6213798.5     |-1611020.125   |6012189.5      |80584928       |114560248      |13123494       |12719918       |15354030       |1181984768     |340600000 |12543904     |391316.1875  |4940903.5  |4.13869190216064|-1.07301771640778  |4.00441074371338  |53.6734809875488|76.3026962280273|8.74088478088379|8.47208404541016|10.2265310287476  |787.259338378906|226.856170654297|8.35484981536865|0.260635614395142 |62.1703567504883|
|6     |13079071      |-1837313.875   |11536777       |360705856      |444046400      |118203104      |30001620       |52489624       |2644631040     |1172118784|32682624     |296555.8125  |3269470.5  |4.05386257171631|-0.569476068019867 |3.57582807540894  |111.800903320312|137.632339477539|36.637092590332 |9.29901218414307|16.2691764831543  |819.704284667969|363.298614501953|10.1299905776978|0.0919175744056702|55.2939186096191|
|7     |9222431       |-1999544.75    |13082455       |321666176      |199608688      |39777244       |25686398       |19823024       |2360659712     |698181184 |21725898     |1367699.5    |10985388   |3.57207417488098|-0.774472832679749 |5.06715631484985  |124.589210510254|77.313346862793 |15.4067039489746|9.94897270202637|7.67794418334961  |914.341491699219|270.422729492188|8.41497421264648|0.529743611812592 |50.7982749938965|
|8     |7367285       |-1003196.4375  |3715750        |508194848      |285036512      |82981920       |9917811        |14823479       |1981814656     |358640608 |13513138     |1639607.125  |14895638   |3.85766649246216|-0.525294899940491 |1.94564533233643  |266.101593017578|149.251159667969|43.4510917663574|5.19317579269409|7.761887550354    |1037.72009277344|187.791809082031|7.07576513290405|0.858533024787903 |89.7921295166016|
|9     |11514595      |611476.5       |1370960.25     |1128605952     |860365248      |59853868       |12085311       |68484344       |3308985344     |830991936 |35876344     |156135.140625|2656632.5  |3.60557007789612|0.191471889615059  |0.429289370775223 |353.400848388672|269.406524658203|18.7420673370361|3.78427839279175|21.4445304870605  |1036.14392089844|260.208862304688|11.2339744567871|0.0488906614482403|102.108047485352|
|10    |7760664.5     |-2001773       |3010117.5      |975776768      |400946048      |65875932       |11212661       |13860104       |2628241664     |417332928 |15272914     |172473.578125|3089599.5  |4.50678730010986|-1.162473320961    |1.74804091453552  |566.654846191406|232.838119506836|38.2555923461914|6.5114369392395 |8.04886436462402  |1526.27734375   |242.354339599609|8.86931419372559|0.100159168243408 |71.1620941162109|
|11    |6190187       |-525645.6875   |2032737.125    |951176192      |331977600      |94320544       |7692623.5      |16549218       |2551853312     |277516544 |13862499     |246499.875   |5328125.5  |2.97612023353577|-0.25272011756897  |0.977299988269806 |457.306793212891|159.608291625977|45.3474617004395|3.69846200942993|7.95653820037842  |1226.880859375  |133.424499511719|6.66481685638428|0.118512287735939 |82.093879699707 |
|12    |4796991       |-3670097.5     |6675493.5      |892179392      |151398608      |47636504       |13364405       |12124169       |1862399872     |297973568 |12840320     |279278.0625  |3893233.5  |3.26216435432434|-2.49582719802856  |4.53962850570679  |606.721130371094|102.957695007324|32.3949127197266|9.08838176727295|8.24496650695801  |1266.51354980469|202.635101318359|8.73198127746582|0.189921334385872 |91.8226623535156|
|13    |4180812       |-1966252       |4188338.25     |820324288      |118433392      |13373609       |5392821.5      |8089576.5      |1595230976     |203726880 |7534640.5    |630021.875   |5791427    |3.84992361068726|-1.81063389778137  |3.85685420036316  |755.400085449219|109.060035705566|12.3151607513428|4.96600914001465|7.44933080673218  |1468.97717285156|187.603012084961|6.93831491470337|0.580159068107605 |95.9212951660156|
|14    |11493181      |1311883        |-46568.4296875 |1760342912     |583569920      |169520080      |9739942        |24529226       |3541960960     |410719680 |20315906     |230356.03125 |3561460.75 |4.62534999847412|0.5279580950737    |-0.018741138279438|708.437683105469|234.853622436523|68.22216796875  |3.91977143287659|9.87161540985107  |1425.43737792969|165.291259765625|8.17599391937256|0.0927051678299904|76.8746719360352|
|15    |14775459      |-1401302.875   |2728959.5      |1592540032     |133825464      |24951992       |20334110       |21244200       |3423408640     |1261944192|21684248     |388125.6875  |4637948    |7.1502857208252 |-0.678132295608521 |1.32062494754791  |770.677612304688|64.7621383666992|12.0750131607056|9.84028244018555|10.2807025909424  |1656.68957519531|610.692443847656|10.4936542510986|0.187825605273247 |71.6091079711914|
|16    |11939729      |-1354792.375   |2037993.375    |1932935808     |202512656      |91883288       |21937278       |28598576       |4042680832     |971981504 |26152224     |593484.1875  |5005266.5  |5.38731288909912|-0.611294448375702 |0.91956090927124  |872.157958984375|91.3755264282227|41.4585647583008|9.89829635620117|12.9039335250854  |1824.09387207031|438.566772460938|11.8001184463501|0.267785400152206 |89.7749404907227|
|17    |12789686      |-4319187       |6041261.5      |1595442944     |178642960      |93629552       |32279874       |24700076       |3771268096     |900992768 |19873770     |359441.53125 |4145585.75 |6.03806447982788|-2.03910636901855  |2.85210490226746  |753.215270996094|84.3380889892578|44.2029037475586|15.2394638061523|11.6610097885132  |1780.43151855469|425.362457275391|9.38249015808105|0.169693857431412 |92.5089721679688|
|18    |10085915      |2031190        |-909519.3125   |2006170496     |296656544      |104402584      |14108412       |43205100       |3795277056     |526853184 |19702734     |199586.484375|2175655.5  |4.54830598831177|0.915977716445923  |-0.410153388977051|904.695007324219|133.779113769531|47.0809936523438|6.36227607727051|19.4836082458496  |1711.50378417969|237.587707519531|8.88506984710693|0.0900047644972801|102.840484619141|
