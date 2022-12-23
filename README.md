# -Excel-generator
How to generate fake data using Excel formulas

### Prepare in advance a table on the side of the document with all the characters you want to include, for example in my case it was all uppercase letters and all numbers, the sum total comes out to 36 options

=RANDARRAY(6,1,1,36,1) ### Generates 6 cells of random numbers in the range 1-36

=INDEX(our_table!B1:B36,RANDARRAY(6,1,1,36,1),1) ### Translates the number we created to the corresponding character in our table according to the index 

=TEXTJOIN("",1,INDEX(our_table!$B$1:$B$36,RANDARRAY(6,1,1,36,1),1)) ### Combines the 6 characters we created in different cells in one column into one cell containing the 6 characters
