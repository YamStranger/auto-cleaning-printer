# auto-cleaning-printer

Project with bat file to clean printer



@echo off
:A
 :W
 timeout /t 5 /nobreak
 echo %time%|find "19:00" >nul ||goto :W
 
 echo "Printing"
 start "c:\Program Files (x86)\Print from command line" "SumatraPDF.exe" -print-to "EPSON T50 Series" CleanPrinter.pdf
timeout /t 30 /nobreak
goto :A
