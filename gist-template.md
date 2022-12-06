# Hexi-decimals
[The Martian](https://www.youtube.com/watch?v=NttUBB98zg4)

Doing my research I felt like I was learning a new language.

[Morse Code](https://youtu.be/iy8BaMs_JuI)

[German Enigma Machines](https://malevus.com/world-war-ii-codes-and-ciphers/)

Its intresting that we learn this at code. Maybe the reason I don't understand it, is that it is code. Tell me to the Phonitc alphabet or 10-codes for both military and police, I can do that. This like everything else needs to be more than a few sites or a few videos.


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
- [Quantifiers](https://learn.microsoft.com/en-us/dotnet/standard/base-types/quantifiers-in-regular-expressions)
Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. The following table lists the quantifiers supported by .NET
- [OR Operator](https://www.geeksforgeeks.org/perl-operators-in-regular-expression/#:~:text=The%20Regular%20Expression%20is%20a%20string%20which%20is,%3D~%20%28Regex%20Operator%29%20and%20%21~%20%28Negated%20Regex%20Operator%29.)
The Regular Expression is a string which is the combination of different characters that provides matching of the text strings. A regular expression can also be referred to as regex or regexp.
The basic method for applying a regular expression is to use of binding operators =~ (Regex Operator) and !~ (Negated Regex Operator).
- [Character Classes](https://learn.microsoft.com/en-us/dotnet/standard/base-types/character-classes-in-regular-expressions)
A character class defines a set of characters, any one of which can occur in an input string for a match to succeed. The regular expression language in .NET supports the following character classes:

Positive character groups. A character in the input string must match one of a specified set of characters. For more information, see Positive Character Group.

Negative character groups. A character in the input string must not match one of a specified set of characters. For more information, see Negative Character Group.

Any character. The . (dot or period) character in a regular expression is a wildcard character that matches any character except \n. For more information, see Any Character.

A general Unicode category or named block. A character in the input string must be a member of a particular Unicode category or must fall within a contiguous range of Unicode characters for a match to succeed. For more information, see Unicode Category or Unicode Block.

A negative general Unicode category or named block. A character in the input string must not be a member of a particular Unicode category or must not fall within a contiguous range of Unicode characters for a match to succeed. For more information, see Negative Unicode Category or Unicode Block.

A word character. A character in the input string can belong to any of the Unicode categories that are appropriate for characters in words. For more information, see Word Character.

A non-word character. A character in the input string can belong to any Unicode category that is not a word character. For more information, see Non-Word Character.

A white-space character. A character in the input string can be any Unicode separator character, as well as any one of a number of control characters. For more information, see White-Space Character.

A non-white-space character. A character in the input string can be any character that is not a white-space character. For more information, see Non-White-Space Character.

A decimal digit. A character in the input string can be any of a number of characters classified as Unicode decimal digits. For more information, see Decimal Digit Character.

A non-decimal digit. A character in the input string can be anything other than a Unicode decimal digit. For more information, see Decimal Digit Character.
- [Flags](https://www.codeguage.com/courses/regexp/flags#:~:text=A%20flag%20is%20an%20optional%20parameter%20to%20a,is%20denoted%20using%20a%20single%20lowercase%20alphabetic%20character.)
A flag is an optional parameter to a regex that modifies its behavior of searching.
A flag changes the default searching behavior of a regular expression. It makes a regex search in a different way.
A flag is denoted using a single lowercase alphabetic character.
- [Grouping and Capturing](https://learn.microsoft.com/en-us/dotnet/standard/base-types/grouping-constructs-in-regular-expressions)
Grouping constructs delineate the subexpressions of a regular expression and capture the substrings of an input string. You can use grouping constructs to do the following:

Match a subexpression that is repeated in the input string.

Apply a quantifier to a subexpression that has multiple regular expression language elements. For more information about quantifiers, see Quantifiers.

Include a subexpression in the string that is returned by the Regex.Replace and Match.Result methods.

Retrieve individual subexpressions from the Match.Groups property and process them separately from the matched text as a whole.

The following table lists the grouping constructs supported by the .NET regular expression engine and indicates whether they are capturing or non-capturing.
- [Bracket Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)
Regular expressions are patterns used to match character combinations in strings. In JavaScript, regular expressions are also objects. These patterns are used with the exec() and test() methods of RegExp, and with the match(), matchAll(), replace(), replaceAll(), search(), and split() methods of String. This chapter describes JavaScript regular expressions.
- [Greedy and Lazy Match](https://javascript.info/regexp-greedy-and-lazy)
Quantifiers are very simple from the first sight, but in fact they can be tricky.

We should understand how the search works very well if we plan to look for something more complex than /\d+/.

Let’s take the following task as an example.

We have a text and need to replace all quotes "..." with guillemet marks: «...». They are preferred for typography in many countries.

For instance: "Hello, world" should become «Hello, world». There exist other quotes, such as „Witaj, świecie!” (Polish) or 「你好，世界」 (Chinese), but for our task let’s choose «...».

The first thing to do is to locate quoted strings, and then we can replace them.

A regular expression like /".+"/g (a quote, then something, then the other quote) may seem like a good fit, but it isn’t!
- [Boundaries](http://www.rexegg.com/regex-boundaries.html)
A word boundary, in most regex dialects, is a position between w and W (non-word char), or at the beginning or end of a string if it begins or ends (respectively) with a word character ([0-9A-Za-z_]). So, in the string "-12", it would match before the 1 or after the 2. The dash is not a word character.
- [Back-references](https://learn.microsoft.com/en-us/dotnet/standard/base-types/backreference-constructs-in-regular-expressions)
Backreferences provide a convenient way to identify a repeated character or substring within a string. For example, if the input string contains multiple occurrences of an arbitrary substring, you can match the first occurrence with a capturing group, and then use a backreference to match subsequent occurrences of the substring.
- [Look-ahead and Look-behind](https://www.regextutorial.org/positive-and-negative-lookbehind-assertions.php#:~:text=Lookbehind%20means%20to%20check%20what%20is%20before%20your,item%20plays%20a%20role%20in%20declaring%20a%20match.)
Lookbehind means to check what is before your regex match while lookahead means checking what is after your match. And the presence or absence of an element before or after match item plays a role in declaring a match.

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
string pattern = @"\b91*9*\b";
string input = "99 95 919 929 9119 9219 999 9919 91119";
foreach (Match match in Regex.Matches(input, pattern))
   Console.WriteLine("'{0}' found at position {1}.", match.Value, match.Index);

// The example displays the following output:
//       '99' found at position 0.
//       '919' found at position 6.
//       '9119' found at position 14.
//       '999' found at position 24.
//       '91119' found at position 33.

### OR Operator
$a = "GeeksforGeeks";

if ($a =~ m/for/)
{
	print "Match Found\n";
}
else
{
	print "Match Not Found\n";
}



### Character Classes
using System;
using System.Text.RegularExpressions;

public class Example
{
   public static void Main()
   {
      string pattern = @"gr[ae]y\s\S+?[\s\p{P}]";
      string input = "The gray wolf jumped over the grey wall.";
      MatchCollection matches = Regex.Matches(input, pattern);
      foreach (Match match in matches)
         Console.WriteLine($"'{match.Value}'");
   }
}
// The example displays the following output:
//       'gray wolf '
//       'grey wall.'

### Flags
// outputs RegExp flags in alphabetical order

console.log(/foo/ig.flags);
// expected output: "gi"

console.log(/bar/myu.flags);
// expected output: "muy"


### Grouping and Capturing
using System;
using System.Text.RegularExpressions;

public class Example
{
   public static void Main()
   {
      string pattern = @"(\w+)\s(\1)\W";
      string input = "He said that that was the the correct answer.";
      foreach (Match match in Regex.Matches(input, pattern, RegexOptions.IgnoreCase))
         Console.WriteLine("Duplicate '{0}' found at positions {1} and {2}.",
                           match.Groups[1].Value, match.Groups[1].Index, match.Groups[2].Index);
   }
}
// The example displays the following output:
//       Duplicate 'that' found at positions 8 and 13.
//       Duplicate 'the' found at positions 22 and 26.

### Bracket Expressions
const re = /ab+c/;


const re = new RegExp('ab+c');


### Greedy and Lazy Match
let regexp = /".+"/g;

let str = 'a "witch" and her "broom" is one';

alert( str.match(regexp) ); // "witch" and her "broom"

### Boundaries
Input : txt = "geeksforgeeks", regex = "^geeks"
Output : Found from index 0 to 3
Explanation : Note that the result doesn't include "geeks" after
              "for" as we have used ^ in regex.

### Back-references
using System;
using System.Text.RegularExpressions;

public class Example
{
   public static void Main()
   {
      string pattern = @"(\w)\1";
      string input = "trellis llama webbing dresser swagger";
      foreach (Match match in Regex.Matches(input, pattern))
         Console.WriteLine("Found '{0}' at position {1}.",
                           match.Value, match.Index);
   }
}
// The example displays the following output:
//       Found 'll' at position 3.
//       Found 'll' at position 8.
//       Found 'bb' at position 16.
//       Found 'ss' at position 25.
//       Found 'gg' at position 33.
### Look-ahead and Look-behind
<p><div>Joh
n Lennon</d
iv> and <di
v>Mick Jagg
er</div></p

## Author

https://github.com/Arthur528

<a href="https://visitcount.itsvg.in">
  <img src="https://visitcount.itsvg.in/api?id=Arthur528&label=Profile%20Views&color=1&pretty=false" />
</a>
