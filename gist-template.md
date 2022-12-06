# Hexi-decimals
[The Martian](https://www.youtube.com/watch?v=NttUBB98zg4)

Doing my research I felt like I was learning a new language.


If you have ever *wondered* how **search** works, 
its all about *finding* ***patterns***. <br />
While a *search engine* will have sophisticated 
[search algorithms](http://en.wikipedia.org/wiki/Search_algorithm) at their
*core* are searches for patterns in text.

## Summary

A regular expression is a pattern we search for in text.

Imagine you want to check if an email address is well correct when someone
is filling in a form.
One way of doing this would be to try *sending* an email to the address and
waiting for a reply or "[bounce](http://en.wikipedia.org/wiki/Bounce_message)" 
(error)...
(*obviously* this is a *terrible* idea! sending email is time consuming)
A far more efficient way of checking email validity is to use a regular
expression that will tell us in a milisecond 
if the email matches a valid pattern.

![email regex](http://i.imgur.com/7rV4c56.jpg "email regex")

## Table of Contents

- [Anchors](https://learn.microsoft.com/en-us/dotnet/standard/base-types/anchors-in-regular-expressions)
Anchors, or atomic zero-width assertions, specify a position in the string where a match must occur. When you use an anchor in your search expression, the regular expression engine does not advance through the string or consume characters; it looks for a match in the specified position only. For example, ^ specifies that the match must start at the beginning of a line or string. Therefore, the regular expression ^http: matches "http:" only when it occurs at the beginning of a line. The following table lists the anchors supported by the regular expressions in .NET.
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

# Regex Components

### Anchors
using System;
using System.Text.RegularExpressions;

public class Example
{
    public static void Main()
    {
        string input = "Brooklyn Dodgers, National League, 1911, 1912, 1932-1957\n" +
                       "Chicago Cubs, National League, 1903-present\n" +
                       "Detroit Tigers, American League, 1901-present\n" +
                       "New York Giants, National League, 1885-1957\n" +
                       "Washington Senators, American League, 1901-1960\n";

        string pattern = @"\A((\w+(\s?)){2,}),\s(\w+\s\w+),(\s\d{4}(-(\d{4}|present))?,?)+";

        Match match = Regex.Match(input, pattern, RegexOptions.Multiline);
        while (match.Success)
        {
            Console.Write("The {0} played in the {1} in",
                              match.Groups[1].Value, match.Groups[4].Value);
            foreach (Capture capture in match.Groups[5].Captures)
                Console.Write(capture.Value);

            Console.WriteLine(".");
            match = match.NextMatch();
        }
        Console.WriteLine();
    }
}
// The example displays the following output:
//    The Brooklyn Dodgers played in the National League in 1911, 1912, 1932-1957.

### Quantifiers

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references
The Martian 4K HDR | First Contact
https://www.youtube.com/watch?v=NttUBB98zg4
Doing my research I felt like I was learning a new language.
### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
