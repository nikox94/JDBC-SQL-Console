# JDBC-SQL-Console
A simple cmd tool to run SQL queries and export the data.

This is a pruned version of the source code of this tool:
http://jdbcsqlconsole.sourceforge.net/

<h1>JDBC SQL Console</h1>
<h2>Description</h2>
JDBC SQL Console is a JAVA console application that can be used by scripts to:
<ul>
<li>Execute queries in diferent databases. such as mysql, oracle, postgresql</li>
<li>Dump data from queries to txt and excel files</li>
<li>Generate create table commands based on SELECT statements</li>
</ul> 

<p>This application runs on any Windows, Linux, Mac, Solaris and other operating system that supports JAVA.</p>
<p>In order to execute application your computer needs Java Runtime Enviroment <a href="http://www.java.com/">Install it</a>


<a name="download">
</a></p><h2><a name="download">Download</a></h2><a name="download">
</a><p><a name="download">
To download software visit </a><a href="http://sourceforge.net/projects/jdbcsqlconsole/files/">sourceforge JDBC SQL Console</a>
<a href="http://sourceforge.net/projects/jdbcsqlconsole/files/binary/JDBCSqlConsole-2011-06-09.zip/download">Last release</a>
</p>


<a name="documentation">
<h2>Documentation</h2>
<p>Main commands:</p>
<ul>
<li>-query             Execute query (this is the default command)</li>
<li>-export-to-cvs     Generate text file</li>
<li>-export-to-excel   Generate Microsoft Excel File</li>
<li>-generate-create-table   Generate create table</li>
</ul>

<p>JDBC Drivers:</p>
<ul>
<li>-driver     JDBC driver i.e: com.mysql.jdbc.Driver</li>
<li>-oracle     to use Oracle driver</li>
<li>-mysql      to use mysql driver</li>
<li>-sqlserver  to use Microsoft SQLServer driver</li>
<li>-postgresql to use Postgresql driver</li>
</ul>

<p>URL:</p>
<ul>
<li>-url       JDBC Url</li>
<li>-host       server host if not url </li>
<li>-port       server port (optional) if not url</li>
<li>-database   database if not url</li>
<li>-sid        SID if not url</li>
</ul>

<p>Authentication:</p>
<ul>
<li>-user       user to connnect to database</li>
<li>-password   password to connnect to database</li>
</ul>

<p>Options:</p>
<ul>
<li>-separator  column separator for output (text file o stdout</li>
<li>-hide-headers  hide headers on text output</li>
<li>-show-metadata show additional row with metadata</li>
</ul>



</a><a name="examples">
<h2>Examples</h2>

<p class="command">
java -jar JDBCSqlConsole.jar -mysql  -host 127.0.0.1 -database myDB -user peter -password changeit "SELECT * FROM element_model"
</p>



<p class="command">
java -jar JDBCSqlConsole.jar -mysql -generate-create-table -host 127.0.0.1 -database myDB -user peter -password changeit "SELECT * FROM users";
</p>
<p class="result">
CREATE TABLE users (
    login    VARCHAR(50),
    password    VARCHAR(255),
    name    VARCHAR(150),
    email    VARCHAR(100),
    login_mobile    VARCHAR(50),
    password_mobile    VARCHAR(255),
    phone    VARCHAR(50),
    identification    VARCHAR(50),
    mobile_phone    VARCHAR(50)
)
</p>
