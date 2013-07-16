csv
===

the import and export of csv

csvExport
===

$export = new CsvExport();
    $export->setHeader(array('ids','username','age'));
    
    $export->append(
        array(
            array('id'=>1,'username'=>'Michael','age'=>25),
            array('id'=>2,'username'=>'Han','age'=>24)
        )
    );
    $export->append(
        array(
            array('id'=>3,'username'=>'Mike','age'=>25),
        ),true
    );
    $export->export('user.csv')
    
    
csvImport
===

 $import = new CsvImport();
    $import->setFile('read.csv',500,"\t");
    print_r($import->getRows());
    print_r($import->getHeader());
