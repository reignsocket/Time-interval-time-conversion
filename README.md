
Problem Description  
Until the 19th century, time calibration was a purely local phenomenon. Every village rises to the highest point when the sun rises
Time to adjust their clock to 12 noon. The time when a watchmaker manufactures a merchant's home or the village's main watch is considered to be
At official time, the citizens aligned their watches with this time. Every week, some enthusiastic citizens will take the time standard table and walk around the streets for other citizens. When traveling between cities, you need to calibrate your pocket watch when you arrive at a new place. However, when the railway is put into use, more and more people frequently travel long distances, and time becomes more and more important. In the early days of the railway, the timetable was very confusing, and every so-called stop time was based on the local time of the stop. The standardization of time has become very important for the efficient operation of railways.
In 1878, Canadian Sir Sanford Fleming proposed to use a global time zone (this proposal was
Adopted and derived from the concept of the global time zone we use today, he suggested dividing the world into 24 time zones, each spanning 15 degrees of warp (because the Earth's longitude is 360 degrees, divided into 24 blocks, one piece is 15 degrees) . Sir Sanford Fleming's approach solves a global problem of time chaos.
On November 18, 1883, the American Railway Company used the time method proposed by Fleming. One in 1884
The International Meridian Conference was held in Washington, DC. His goal was to choose a suitable prime meridian. The conference finally selected Greenwich as the standard 0 degree. Although the time zone was determined, countries did not immediately change their time specifications. In the United States, although many states began using standard time zone time in 1895, Congress did not enforce the time specifications established by the conference until 1918. Today, each country uses a variant of the Fleming time zone specification. China has spanned five time zones, but used a uniform time specification that is eight hours ahead of Coordinated Universal Time (UTC). Russia also embraces this time zone specification, although the time spent in the entire country is one hour ahead of the standard time zone. Australia uses three time zones, with the main time zone being ahead of his time zone of Fleming by half an hour. Many Middle Eastern countries also use half-time zones (that is, not according to Fleming's 24 integer time zones). Because the time zone is a division of longitude, scientists working in the Antarctic or the Arctic use UTC time directly, otherwise the Antarctic continent will be broken down into 24 time zones.
The time zone conversion table is as follows:  
  
UTC Coordinated Universal Time  
GMT Greenwich Mean Time, defined as UTC  
BST British Summer Time, defined as UTC+1 hour  
IST Irish Summer Time, defined as UTC+1 hour  
WET Western Europe Time, defined as UTC  
WEST Western Europe Summer Time, defined as UTC+1 hour  
CET Central Europe Time, defined as UTC+1  
CEST Central Europe Summer Time, defined as UTC+2  
EET Eastern Europe Time, defined as UTC+2  
EEST Eastern Europe Summer Time, defined as UTC+3  
MSK Moscow Time, defined as UTC+3  
MSD Moscow Summer Time, defined as UTC+4  
AST Atlantic Standard Time, defined as UTC-4 hours  
ADT Atlantic Daylight Time, defined as UTC-3 hours  
NST Newfoundland Standard Time, defined as UTC-3.5 hours  
NDT Newfoundland Daylight Time, defined as UTC-2.5 hours  
EST Eastern Standard Time, defined as UTC-5 hours  
EDT Eastern Daylight Saving Time, defined as UTC-4 hours  
CST Central Standard Time, defined as UTC-6 hours  
CDT Central Daylight Saving Time, defined as UTC-5 hours  
MST Mountain Standard Time, defined as UTC-7 hours  
MDT Mountain Daylight Saving Time, defined as UTC-6 hours  
PST Pacific Standard Time, defined as UTC-8 hours  
PDT Pacific Daylight Saving Time, defined as UTC-7 hours  
HST Hawaiian Standard Time, defined as UTC-10 hours  
AKST Alaska Standard Time, defined as UTC-9 hours  
AKDT Alaska Standard Daylight Saving Time, defined as UTC-8 hours  
AEST Australian Eastern Standard Time, defined as UTC+10 hours  
AEDT Australian Eastern Daylight Time, defined as UTC+11 hours  
ACST Australian Central Standard Time, defined as UTC+9.5 hours  
ACDT Australian Central Daylight Time, defined as UTC+10.5 hours  
AWST Australian Western Standard Time, defined as UTC+8 hours  
Here are some times, please convert between different time zones.  
  
Input data  
The first line of the input contains an integer N indicating that there are N sets of test data. Next N lines, each line of packets
Includes a time and an abbreviation for two time zones separated by spaces. The time is given by the standard a.m./p.m.
Midnight means 12 o'clock in the evening (12:00 a.m.) and noon means 12 noon (12:00 p.m.).
  
  
Output requirements  
Suppose the time given by the input line is the standard time in the first time zone, and it is required to output this time in the second
Standard time in the time zone.  
  
Input sample  
4  
Noon HST CEST  
11:29 a.m. EST GMT  
6:01 p.m. CST UTC  
12:40 p.m. ADT MSK  
  
Output sample  
Midnight  
4:29 p.m.  
12:01 a.m.  
6:40 p.m.  
  
Problem solving  
This topic requires time conversion between two time zones. We can derive the difference between the two time zones based on the conversion formula for each time zone and Greenwich Mean Time. The solution to the problem is not difficult to think, but the common feature of the date processing class is that the input and output are more troublesome, and there are some situations that require special handling. For example, if one or more days after the conversion, the situation needs to be handled. Specific to this topic: input, in addition to the general time representation: time: sub-am / pm, special treatment of noon and midnight; after direct conversion through Greenwich time, to determine whether more than one day or Reduced the situation of the day; special processing of noon and midnight is required when outputting time. When solving this problem, the key is to determine the time difference between the two time zones. Since the time zone is given as a string, the time zone is first mapped to the time difference between the time zone and Greenwich Mean Time. With the time difference between each time zone and Greenwich Mean Time, you can calculate the time difference between any two time zones.  
  
Common problems in implementation  
Question 1: When someone deals with the correspondence between the time zone name and the time difference, it does not use the array element and its subscript method, but uses a series of if else statements to determine one by one, resulting in code redundancy and increasing the chance of error;  
Question 2: There are understanding problems with the representation of special time points. 12:01am means 1 point, 12:01pm means 12:1 noon; noon is output at noon, midnight is output in the early morning;  
Question 3: The situation of moving forward one day and pushing back one day did not take into account.  
Question 4: The big classmates convert the 12-hour system into a 24-hour system, and then change the time according to the time zone relationship.  
The 24-hour clock is converted to a 12-hour clock. Note that when there is a difference of half an hour, the adjustment of the minute value is the most error-prone.  
  
