# NopCommerceDataDriven
NopCommerceDataDriven
#Set level
#log4j.rootLogger=debug, console, file , R , HTML, TTCC
log4j.rootCategory=debug, console, file , R , HTML, TTCC

# Defining Appender
log4j.appender.console=org.apache.log4j.ConsoleAppender  
log4j.appender.R=org.apache.log4j.RollingFileAppender 
log4j.appender.TTCC=org.apache.log4j.RollingFileAppender
log4j.appender.HTML=org.apache.log4j.FileAppender
log4j.appender.file=org.apache.log4j.RollingFileAppender
  
# Appender layout and pattern  
log4j.appender.console.layout=org.apache.log4j.PatternLayout
log4j.appender.console.layout.ConversionPattern=%d{MM-dd-yyyy HH:mm:ss} %F %-5p [%t] %c{2} %L - %m%n

log4j.appender.R.layout=org.apache.log4j.PatternLayout
log4j.appender.R.layout.ConversionPattern=%d - %c -%p - %m%n

log4j.appender.TTCC.layout=org.apache.log4j.TTCCLayout
log4j.appender.TTCC.layout.DateFormat=ISO8601

log4j.appender.HTML.layout=org.apache.log4j.HTMLLayout
log4j.appender.TTCC.layout.Title=Application log
log4j.appender.TTCC.layout.LocationInfo=true
  

# Files location
log4j.appender.file.File=./logs/application.log
log4j.appender.R.File=./logs/application_R.log
log4j.appender.TTCC.File=./logs/application_TTCC.log
log4j.appender.HTML.File=./logs/application_HTML.html
  
# Defining maximum size of a log file
log4j.appender.file.MaxFileSize=10mb 
log4j.appender.file.MaxBackupIndex=10
log4j.appender.file.layout=org.apache.log4j.PatternLayout  
log4j.appender.file.layout.ConversionPattern=%d{ISO8601} %5p [%t] %c{1}:%L - %m%n
log4j.appender.file.Append=false
