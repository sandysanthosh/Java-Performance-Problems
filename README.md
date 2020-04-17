# Java-Performance-Problems

#Top Common Problems Occures in Java and Tools to be used

minimise memeory:

lazy allocation of collection
-dnt create something until u need to put something into it

dnt create colleciton in single object
-just store the object itself

size collections correctly
only 2 size put it correctly

HashMap mhy = new HashMap(2);

avoid expansion of large collections due to 2x algorithm
32 MB used to store 17MB of data

colloections do not shrink once expanded
may be reallcoation if collections uses drops



latency:
how long does gc event takes.

stats:

exception-error with app
app time per request -
data base response time
active thread state
time spent in gc
memory allocation

gather the stats:

LOGS
profiler
core jdk tool
jmx metrices
apm-application performance monitorgin tools
framework/app server moniroting tools

data does each tool provide?

logs
app server monitoring
new relic
yourkit
jvisualkit
jconsole
jmap/jhat
-->jstack

new relic:

applcation permonance monitoring(apm)tool 
that monitor web app,servers,database

donitostics paid

-->jmap/jhat



use in production:

logs
jconsole
app server monitoring
jvisualVM-
jstack
new relic



new relic:

saas

angular react and ember
legicy:

migrating web logic to cloud
lift and shift
appliacation sernver technology
not pizza delivery company software company
memeory utilization

servers
mobile
browser
plugins


new relic:

application monitor 

performance of mobile
for end perspective
performance servers
performance broser
performance platform

new relic works:

deploy new relic agenet in your apps
new relic collect app health data
app performance anywhere


external web calls
web and non-web

highest salary from employee:

select * from employee
where salary = (select max(salary) from employee);

max salary:

select max(salary) from employee;

second highest salary from employee:

select max(salary) from employee where 
salary not in (select max(salary) from employee);

select range based on employee id:
select * from employee where employee_id between 2003 and 2008;

select e.employe_name ,e.salary,d.depart from employee e
inner join department d on (e.depart_id=d.depart_id) where
salary in (select max(salary) from employee);


most common problesm:

slow database queries
ineffiecent applcition code
too many db queries
concurrency issues
memeory leaks
configuration issues(pooling threshold, request throttling)
slow db
GC pauses
memory churn

dbqureies,
memory leaks,
gc puses

->resources leaks:
forgetting to close() resources
jdbc connections
file handles

->gc login:

->Heap Dump Analysis:
 eclipse memory analuzer- eclipse MAT
 for dumps ,not histograms
  -histogream can convert into spreadsheet data easily

->memory leaks:
 -> profiler:
  -> memory: 
    -> generation count

profiler:
execution profliling
memory profiling
thread visualization
heap visulization

sampler:

sample:
 CPU

JDBC:
 JDBC is dsigned as a layout plugin component
 excellent for plugging in logging layer


->JDBC
->can plugin your own layer
->catch commication in either direaction
->monitoring
->logging
->caching

->JDBC:
JDBC logging layer
P6Spy is a framework that enables database data to be seamlessly intercepted and logged with no code changes to the application.

->concurrency:
try to determin what code is:
blocked
waiting
sleeping

the results will ne easily identified with thread dumps
but don't dump too often

concurrency:
stack traces alredy lists deadlocks
stack traces show synchorinzed locked monitors


top common problems:

slow database queires-JDBC monitoring(eg p6spy), tune sql

inefficent application code- execution profile(jvisualvm), tune code

too many db quries-jdbc monitoring(p6spy), refactor calls

commcurrency issues-stack trace analysis

memorry leaks-heap dump analyser(eclipse MAT),identify the objects retaigning memory and fix the code to stop that

configuration issue(pooling thresolds,request throtting)-keep record to changes

slow DB-JDBC monitoring(p6spy), find clusters or slow queries

GC pauses-gc logging and gc logs analyzer(gc viewer)

memeory-look for object allcoation in memory profiler(jvisualvm)


buiulding and tuning high performance java platforms:

web portals
middle wware
database
batch/data movement


proifling java code with jprofile:

->run as
->run configuration
->jprofiler->download
->install and start

memory view
cpu view

->session
->new session
->launch
->main classes->browser class file
->click ok

->general settings->

->cpu views
->program will run for few seconds
->record memory

->hot spot -> how much amount of memeory uses

cpu profiling:
->Two Types:
->instrumentation  -> all  types
->sampling   -> cpu profiling

filter settings:
filter rule for method call recording








