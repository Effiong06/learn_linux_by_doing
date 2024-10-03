# learn_linux_by_doing
1.) We removed the file "test-1" from the data directory
rm data/test-1

2.)We moved the file "top-5-lowest-temparatures.csv" to the analyzed directory
mv top-5-lowest-temparatures.csv analyzed

3.)We searched through the file "satelite_temperature_data.csv" for any duplicate values (rows) and remove them before starting
the analysis.  
sort satelite_temperature_data.csv | uniq > satelite_temperature_data_no_duplicates.csv

4.)We extracted the top 5 highest temperature values from  satelite_temperature_data_no_duplicates.csv and put them in the top-5-highest-temparatures.csv
sort -t, -k3 -nr satelite_temperature_data_no_duplicates.csv | head -n 5 > ../analyzed/top-5-highest-temparatures.csv

5.)We extracted the top 5 lowest temperature values from  satelite_temperature_data_no_duplicates.csv and put them in the top-5-lowest-temparatures.csv
sort -t, -k3 -n satelite_temperature_data_no_duplicates.csv | head -n 5 > ../analyzed/top-5-lowest-temparatures.csv
