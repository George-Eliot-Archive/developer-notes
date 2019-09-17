# Post-processing Data for the Relationship Web
The excel sheet containing the data is located in the resources section. To use the data, it must first be converted into a CSV format. To do this, simply save the excel sheet as a "csv" (File > Save As > name.csv)    
Converting an excel sheet to a CSV has _some_ minor consequences that need manual handling:
  * All text decorations (italicized, boldened, underlined, etc) are lost
  * Some special characters may be corrupted
    * Single quote character "'"
    * French c-cedilla -> Ç 
To fix this, manually run find and replace all. All text that requires find and replace are outlined below in the "Find and Replace" section.

## Find and Replace
| Find  | Replace |
|---|---|
|The Mill on the Floss|`<i>`The Mill on the Floss`</i>`|
|Mill on the Floss|`<i>`Mill on the Floss`</i>`|
|Adam Bede|`<i>`Adam Bede`</i>`|
|Romola|`<i>`Romola`</i>`|
|Silas Marner|`<i>`Silas Marner`</i>`|
|Westminster Review|`<i>`Westminster Reivew`</i>`|
|Scenes of Clerical Life|`<i>`Scenes of Clerical Life`</i>`|
|Middlemarch|`<i>`Middlemarch`</i>`|
|Blackwood's Magazine|`<i>`Blackwood's Magazine`</i>`|
|Daniel Deronda|`<i>`Daniel Deronda`</i>`|
|Felix Holt, the Radical|`<i>`Felix Holt, the Radical`</i>`|
|Every Man in his Humor|`<i>`Every Man in his Humor`</i>`|
|Autobiography of a Shirtmaker|`<i>`Autobiography of a Shirtmaker`</i>`|
|Fran�ois|François|
|�|,|
|Das Leben Jesu|`<i>`Das Leben Jesu`</i>`|
|Railway Sketches|`<i>`Railway Sketches`</i>`|
|All the Year Round|`<i>`All the Year Round`</i>`|

## Manual fix
| Find  | Replace |
|---|---|
|Fran�is|François|