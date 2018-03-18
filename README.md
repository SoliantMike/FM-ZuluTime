FM-ZuluTime
===========
"Zulu" is the phonetic alphabet name used by NATO military for the letter Z, which stands for Zone, as in Time Zone. So, Zulu Time is a standard for writing UTC time that follows a certain format, starting with the largest measure of time first and goes from there. This is an agreed upon format documented in ISO 8601. 

There are several options, a timestamp in zulu format would look like <date>T<time>Z. That is a date "YYYY-MM-DD" with the four-digit Year, two-digit month and two-digit day, "T" for "time", followed by a time formatted as "HH:MM:SS" with hours, minutes and seconds, all followed with a "Z" to denote that it is Zulu format. This format is used quite a bit, especially in calendar applications such as Calendar on OS X or Microsoft Outlook. 

While FileMaker has no built-in function to automatically format a time stamp as Zulu time, we can create a calculation to format a string as text that will be in the correct format. However, remember that due to time zones, if we have stored a relative time, we will need to get the offset from the UTC to get the correct Zulu time. 

Duration in Zulu format indicates the duration of time that has passed between two points in time. This is used a lot as well as a standard of information exchange, especially in calendaring programs.  

Unlike formatting a single time, a duration of time should not include any daylight saving or time zone business. Fortunately, this is the way that calculating time works in FileMaker, since the math is based on the underlying application framework's Epoch time, which the number of seconds that have passed since January 1st, 2001.  

For this example, we need a second date and time to compare. It then gets tricky to calculate to support all options, but the general format looks like this: 

P3D1H15M30S 

Which is to say, a <b>P</b>eriod of 3 <b>D</b>ays, 1 <b>H</b>our, 15 <b>M</b>inutes and 30 <b>S</b>econds in the above example.  

This can be expanded on to meet your requirements if you to show a unit greater than a day, which would be months, weeks or years. The calculation in the sample supports up to days. Feel free to download and examine to see it working.


Read more here:
http://www.soliantconsulting.com/blog/