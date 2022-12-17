# INF 1340 : INTRODUCTION TO DATA PROGRAMMING => TIDY DATA 
The goal of this project is to take the dataset of collected information and clean it up using the tidy data principles


## LOGBOOK OF REFLECTIONS 
19/10
Opening the dataset and understanding the content

Overview:
- Table of contents
- 6 tables of data
- Annex 

### Table 1 -  International migrant stock at mid-year by sex and by major area, region, country or area, 1990-2015

**Columns**
- Sort Order
- Major area, region, country or area of destination
- Notes
- Country code
- Type of data (a)
- International migrant stock at mid-year (both sexes)
    SUBCOLUMNS:
    - 1990	
    - 1995
    - 2000
    - 2005
    - 2010
    - 2015
- International migrant stock at mid-year (male):
    SUBCOLUMNS:
    - 1990
    - 1995
    - 2000
    - 2005
    - 2010
    - 2015
- International migrant stock at mid-year (female)
    SUBCOLUMNS:
    - 1990
    - 1995
    - 2000
    - 2005
    - 2010
    - 2015

**PROBLEM #1** => Not all columns have unique variables (units of measurements)
**PROBLEM #2** => Data needs to be pivoted longer rather than wider

**ROWS**

1	WORLD
2	Developed regions
3	Developing regions
4	Least developed countries
5	Less developed regions excluding least developed countries
6	Sub-Saharan Africa
7	Africa
8	Eastern Africa
9	Burundi
10	Comoros
11	Djibouti
12	Eritrea
13	Ethiopia
14	Kenya
15	Madagascar
16	Malawi
17	Mauritius
18	Mayotte
19	Mozambique
20	Réunion
21	Rwanda
22	Seychelles
23	Somalia
24	South Sudan
25	Uganda
26	United Republic of Tanzania
27	Zambia
28	Zimbabwe
29	Middle Africa
30	Angola
31	Cameroon
32	Central African Republic
33	Chad
34	Congo
35	Democratic Republic of the Congo
36	Equatorial Guinea
37	Gabon
38	Sao Tome and Principe
39	Northern Africa
40	Algeria
41	Egypt
42	Libya
43	Morocco
44	Sudan
45	Tunisia
46	Western Sahara
47	Southern Africa
48	Botswana
49	Lesotho
50	Namibia
51	South Africa
52	Swaziland
53	Western Africa
54	Benin
55	Burkina Faso
56	Cabo Verde
57	Côte d'Ivoire
58	Gambia
59	Ghana
60	Guinea
61	Guinea-Bissau
62	Liberia
63	Mali
64	Mauritania
65	Niger
66	Nigeria
67	Saint Helena
68	Senegal
69	Sierra Leone
70	Togo
71	Asia
72	Central Asia
73	Kazakhstan
74	Kyrgyzstan
75	Tajikistan
76	Turkmenistan
77	Uzbekistan
78	Eastern Asia
79	China
80	China, Hong Kong Special Administrative Region
81	China, Macao Special Administrative Region
82	Democratic People's Republic of Korea
83	Japan
84	Mongolia
85	Republic of Korea
86	South-Eastern Asia
87	Brunei Darussalam
88	Cambodia
89	Indonesia
90	Lao People's Democratic Republic
91	Malaysia
92	Myanmar
93	Philippines
94	Singapore
95	Thailand
96	Timor-Leste
97	Viet Nam
98	Southern Asia
99	Afghanistan
100	Bangladesh
101	Bhutan
102	India
103	Iran (Islamic Republic of)
104	Maldives
105	Nepal
106	Pakistan
107	Sri Lanka
108	Western Asia
109	Armenia
110	Azerbaijan
111	Bahrain
112	Cyprus
113	Georgia
114	Iraq
115	Israel
116	Jordan
117	Kuwait
118	Lebanon
119	Oman
120	Qatar
121	Saudi Arabia
122	State of Palestine
123	Syrian Arab Republic
124	Turkey
125	United Arab Emirates
126	Yemen
127	Europe
128	Eastern Europe
129	Belarus
130	Bulgaria
131	Czech Republic
132	Hungary
133	Poland
134	Republic of Moldova
135	Romania
136	Russian Federation
137	Slovakia
138	Ukraine
139	Northern Europe
140	Channel Islands
141	Denmark
142	Estonia
143	Faeroe Islands
144	Finland
145	Iceland
146	Ireland
147	Isle of Man
148	Latvia
149	Lithuania
150	Norway
151	Sweden
152	United Kingdom of Great Britain and Northern Ireland
153	Southern Europe
154	Albania
155	Andorra
156	Bosnia and Herzegovina
157	Croatia
158	Gibraltar
159	Greece
160	Holy See
161	Italy
162	Malta
163	Montenegro
164	Portugal
165	San Marino
166	Serbia
167	Slovenia
168	Spain
169	The former Yugoslav Republic of Macedonia
170	Western Europe
171	Austria
172	Belgium
173	France
174	Germany
175	Liechtenstein
176	Luxembourg
177	Monaco
178	Netherlands
179	Switzerland
180	Latin America and the Caribbean
181	Caribbean
182	Anguilla
183	Antigua and Barbuda
184	Aruba
185	Bahamas
186	Barbados
187	Bonaire, Sint Eustatius and Saba
188	British Virgin Islands
189	Cayman Islands
190	Cuba
191	Curaçao
192	Dominica
193	Dominican Republic
194	Grenada
195	Guadeloupe
196	Haiti
197	Jamaica
198	Martinique
199	Montserrat
200	Puerto Rico
201	Saint Kitts and Nevis
202	Saint Lucia
203	Saint Vincent and the Grenadines
204	Sint Maarten (Dutch part)
205	Trinidad and Tobago
206	Turks and Caicos Islands
207	United States Virgin Islands
208	Central America
209	Belize
210	Costa Rica
211	El Salvador
212	Guatemala
213	Honduras
214	Mexico
215	Nicaragua
216	Panama
217	South America
218	Argentina
219	Bolivia (Plurinational State of)
220	Brazil
221	Chile
222	Colombia
223	Ecuador
224	Falkland Islands (Malvinas)
225	French Guiana
226	Guyana
227	Paraguay
228	Peru
229	Suriname
230	Uruguay
231	Venezuela (Bolivarian Republic of)
232	Northern America
233	Bermuda
234	Canada
235	Greenland
236	Saint Pierre and Miquelon
237	United States of America
238	Oceania
239	Australia and New Zealand
240	Australia
241	New Zealand
242	Melanesia
243	Fiji
244	New Caledonia
245	Papua New Guinea
246	Solomon Islands
247	Vanuatu
248	Micronesia
249	Guam
250	Kiribati
251	Marshall Islands
252	Micronesia (Federated States of)
253	Nauru
254	Northern Mariana Islands
255	Palau
256	Polynesia
257	American Samoa
258	Cook Islands
259	French Polynesia
260	Niue
261	Samoa
262	Tokelau
263	Tonga
264	Tuvalu
265	Wallis and Futuna Islands

**PROBLEM #1** => Is the sort order column useful information? 
**PROBLEM #2** => Regions and countries should be separated.
**PROBLEM #3** => Should these parameters be rows or parameters: Developed regions, Developing regions, Least developed countries, Less developed regions excluding least developed countries

**PROBLEMS IN CELLS** 
- Missing values

20/10
**Tinkering with dataset without defining any functions.**

- Successfully remove the titles in Table 1, as these are not part of the data set and simply add NaN information in unique cells that simply represent blank space for stylism rather than provide actual data. 

21/10
**Tinkering with dataset without defining any functions.**
- Renamed the columns without removing NaN blank spaces. 


25/10
## Reflections: 
Back to the drawing board:
Do we want to divide the data into two tables 1) for the main data country 2) for summary of least developed, developed, developing? 

### What is the dataset in table1? 
Table 1 includes individual years with male and female, as well as summary per country. 
Therefore, our main columns can be:
- IMS Male
- IMS Female
- IMS Total
- Country
- Region
- Continent 
- Status

04/10 
##  Reflections
Completed first table with basic tidying, that is Columns and Rows have been melted and verticalized. However, I am still puzzled on whether the Notes column, which is elaborated information in the appendix is vital or not to the dataset. I also did not deal with the countries and regions mixed together in the same table. While the regional component does not hinder the rows, I feel the region and country should be separate columns to make it ultimtely easier to parse and sum. 

06/10
Completing the same basic tidying and extracting process as table 1, but for all tables before going more in depth. I divided the summing tables of development level as these did not fit into the table with country names and regions. It will act as a separate table. After completing a percentage analysis of missing data, I know I'll have to do something about "Notes" and "Type of Data" as both those columns are missing a tremendous amount of information. 

14/10 
Assessing that my titles (i.e. # of Migrants) are not clear and chosen acronyms for coding simplicity (T, F, M) will need to be changed for more effective use of the dataset. Repetitive code is not ideal, therefore my final submission will need to reflect code for all the tables and not one table. 

- Create functions for each step to process all the tables. 

- Table 3 & 4, must be merged to Table 1 as a column. While the percentage is a different value and perspective, it does not require a separate table and rather duplicates information more than informs. Missing information that will be needed here: Male percentages, which will be easily filled, as we assuredly know if we remove the female percentages from the total percentages, the remaining number can only be attributed to the Male percentages. 


I opted to split table 6 into two tables as one column variable was simply not computable with the others (1990-1995 vs 1990, 1995). I considered dividing the date series into single years, but I could not decide on which value belonging to 1990-1995 and 1995-2000 could be attributed to 1995 specifically. Thus, to avoid inaccurate data, I preferred to separate the data. 


15/11

I am assessing if Table 6 Columns "Year" and "Percentage of Refugee" + "Refugee Stock" can be appended. If they have the same length of indexes, as they append the same dates, I believe I can simply integrate them to another table. 


Realized I replicated WORLD, less developing world by not removing it sooner. 

Huge clean up and restructuring, as it was too easy to get lost within tinkered code that no longer served. 

Merged Tables together

16/11

Still to be done:

TYPE DATA (A)
- Separate all letters in Type data (a) into columns
- Rename all the columns
- Turn Data into YES, NaN into NO.

REINDEX ALL TABLES

ADD TABLE 4 TO TABLE 1

ADD TABLE 6 TO TABLE 5


- I created a lot of work for myself by splitting World into summary tables when they could have stayed in the data frame 