Java regex remove duplicated words

Regular Expressions are very handy for text processing. In this article we’ll show Java Regex to remove duplicated words, which is a common task.

Regular Expression to match subsequent
Java regex to remove duplicated words is not very complex, but can be problematic to write at the first time:

String regex = "\\b(\\w+)(\\s+\\1\\b)+";
What all that means:

\b: look for word boundary (match only beginning of word instead of somewhere in the middle);
(\w+): match one ore more word characters and remember them as a group (the parens) to which later we can refer to using a number; so this matches a complete word and remembers it;
\s+: match one or more space characters;
\1: match the word remembered in step 2;
\b: like in step 1 – make sure it’s not a part of some longer word;
(\s+\1\b)+: match one or more occurrences of the word captured in step 2.
That’s it! If you want to match words in case insensitive way then just compile the above Regular Expression with CASE_INSENSITIVE flag:

Pattern p = Pattern.compile(regex, Pattern.CASE_INSENSITIVE);
Replacement loop
The second important part of the word de-duplication is the replacement loop, which does the actual replacement of duplicated pattern with only one word:

String input = "The the string String string stringing.";
Matcher m = p.matcher(input);
while (m.find()) {
    input = input.replaceAll(m.group(), m.group(1));
}
It matches every occurrence of the Regular Expression defined above and replaces whole matched string/pattern (here m.group()) with the content of the first remembered group (m.group(1)), which is our single word.
When applied on the input string, m.group() and m.group(1) will have the following values in subsequent iterations of the while loop:

1) m.group(): “The the” and m.group(1): ‘The’
2) m.group(): “string String string” and m.group(1): “string”.
Remove duplicated words complete example
Whole Java application that removes duplicated words may look like this:

package com.farenda.java.util.regex;
import java.util.regex.Matcher;
import java.util.regex.Pattern;
public class Dedupper {
    public static void main(String[] args) {
        String input = "The the string String string stringing.";
        String regex = "\\b(\\w+)(\\s+\\1\\b)+";
 
        // Use compile(regex) if you want case sensitive.
        Pattern p = Pattern.compile(regex, Pattern.CASE_INSENSITIVE);
 
        Matcher m = p.matcher(input);
        while (m.find()) {
            input = input.replaceAll(m.group(), m.group(1));
        }
 
        System.out.println(input);
    }
}
The above code produces the following output:

The string stringing.
