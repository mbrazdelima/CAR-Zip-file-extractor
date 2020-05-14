# CAR zip file extractor

This is a simple code to extract zip files from CAR (Cadastro Ambiental Rural). You can download the files on this site: http://www.car.gov.br/publico/municipios/downloads

Those files have information about soil cover, native vegetation, APP (Área de Preservação Permanente), and others. That information can be used for those who want to study areas to buy, study the conservation of areas, etc.

The problem is, each zip file, have other zip files inside. You will extract a lot of zip files to access the information. If you want the information from many cities, you will have to spend a lot of time doing hard and repetitive work. You can use this code to extract the information automatically.

-------------------------------
## Instructions
To use this code, you will need to do some adjusts.

1 - Create a folder and move all zip files there.
2 - Change the directory of the first for loop. Don't forget to add "/*.zip"/* in the final.
3 - Lastly, you need to count the number of characters of the directory until "/" and adjust the first value of interval. The second         value of the interval is the first value + 13.

Follow this example below:

Directory: C:\Users\EAML00133972\Desktop\municipios

- Change the directory and add "/*zip"
for i in glob(r'C:\Users\EAML00133972\Desktop\municipios/*.zip'): ...

- Set the interval
C:\Users\EAML00133972\Desktop\municipios/ --> 41 caractheres 

41 + 13 = 54

for i in glob(r'C:\Users\EAML00133972\Desktop\municipios/*.zip'):
  municipios.append(i[41:54])
