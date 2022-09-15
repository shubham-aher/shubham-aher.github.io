---
layout: post
title: Write CSV file in Groovy/Grails
---

There are many libraries to work with CSV files. We will make use of the OpenCSV library to write a sample CSV with two rows. 

Code snippet:

CSVWrtier Example in Groovy

```groovy

@GrabConfig(systemClassLoader = true)
@Grab(group='au.com.bytecode', module='opencsv', version='2.4')
 
import au.com.bytecode.opencsv.CSVWriter
 
class CSVWriterExample {
 
    static void main(String[] args) {
 
            def outputFilePath = "/home/user-name/employee.csv"
 
            File csvFile = new File(outputFilePath)
            csvFile.createNewFile()
 
            csvFile.withWriter { writer ->
 
                CSVWriter csvWriter = new CSVWriter(writer)
 
                csvWriter.writeNext(["1","Alice","123"] as String[])
                csvWriter.writeNext(["2","Bob","456"] as String[])
        }
    }
}

```
