---
layout: post
title:  "Thinking in c++ Part-1,Chapter-2"
date:   2018-07-14 15:07:19
categories: [cpp]
comments: true
---
As `Chapter 2` contains QA's so lets start .
`Q1.Create a program that opens a file and counts the whitespace-separated words in that file!`

<!--more-->

chapter2.cpp:

{% highlight cpp %}
#include <iostream>
#include <string>
#include <fstream>
using namespace std;
class chapter2{
    //q.3
    int countWhiteSpacesFromFile(string s){
        string word;
        int count = 0;
        ifstream in(s);
        while (in >> word){
            count++;
        }
        return count;
    }
};

{% endhighlight %}

`Q2.Create a program that counts the occurrence of a
particular word in a file (use the string class’ operator
‘==’ to find the word).`

chapter2.cpp:

{% highlight cpp %}

#include <iostream>
#include <string>
#include <fstream>
using namespace std;
class chapter2{
    //q.3
    int wordOccurenceFromFile(string s){
        int count = 0;
        ifstream in(s);
        string word;
        while(in >> word){
            if(s == word)
                count++;
        }
        return count;
    }
};
{% endhighlight %}

`Q3.Change Fillvector.cpp so that it prints the lines
(backwards) from last to first.`

chapter2.cpp:

{% highlight cpp %}

#include <iostream>
#include <string>
#include <fstream>
#include <vector>	
using namespace std;
class chapter2{
    //q.3
     vector<string> printBackwardFromFile(string filename){
        vector<string> vs;
        string line;
        ifstream in(filename);
        while(getline(in,line)){
            vs.push_back(line);
        }
        return vs;
    }
};
{% endhighlight %}
