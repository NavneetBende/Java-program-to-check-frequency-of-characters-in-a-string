Check Frequency of Characters in a string
Finding the frequency of a character in a string, means we have to check how many times a particular character is present in that string. Here, we have coded a Java Program for the same. Let’s take an example of a string “prepinsta” . In which we have to check that how many times each of the characters gets repeated in the string.
 

Java program to check frequency of characters in a string
Algorithm
 Take string input from user and store it in the variable called “str”.
After that make freq array having size of length of string.
Convert string to char array .
Run for loop start from i=0 to str<length() store 1 to freq array.
Run j loop start from i=i+1 to j<str.length().
check condition if(string[i] == string[j]) then do freq[i]++  and set string[j]=’0′ .
After that display frequency of character one by one.
Code in Java (Check Frequency of Characters)
import java.util.Scanner;

public class FrequencyOfCharactersInAString {
   public static void main(String[] args) {
    Scanner sc =new Scanner(System.in);
     System.out.print("Enter String : ");
     String str = sc.nextLine(); 
     int[] freq = new int[str.length()]; 
     int i, j; 

     //Converts given string into character array 
     char string[] = str.toCharArray(); 
     for(i = 0; i <str.length(); i++) { 
        freq[i] = 1; 
          for(j = i+1; j <str.length(); j++) { 
            if(string[i] == string[j]) { 
            freq[i]++; 

           //Set string[j] to 0 to avoid printing visited character 
            string[j] = '0'; 
          } 
       } 
    } 
    //Displays the each character and their corresponding frequency 
    System.out.println("Characters and their corresponding frequencies"); 
    for(i = 0; i <freq.length; i++) { 
       if(string[i] != ' ' && string[i] != '0') 
          System.out.println(string[i] + "-" + freq[i]); 
       } 
   }
}
Output
Enter String : prepinsta
Characters and their corresponding frequencies
p-2
r-1
e-1
i-1
n-1
s-1
t-1
a-1
Related Pages
Juggling algorithm for array rotation
 
Balanced Parenthesis Problem
 
Toggle each character in a string

Count the number of vowels

Length of the string without using strlen() function

Prime Course Trailer

Related Banners
Get PrepInsta Prime & get Access to all 200+ courses offered by PrepInsta in One Subscription

Get Prime
Login/Signup to comment


Abhishek public static void main (String[]args)
{
HashMap map = new HashMap();
String str = “prepinsta”;
char ch[] = str.toCharArray();
for(Character ch1 : ch){
map.put(ch1, map.getOrDefault(ch1, 0)+1);
}
System.out.println(map);
}
}
0Log in to Reply

Shekhar Suman String str=”prepinsta”;
Map hm=new HashMap();
for (int i=0;i<str.length();i++){
char ch=str.charAt(i);
if(hm.containsKey(ch)){
hm.put(ch,hm.get(ch)+1);
}else{
hm.put(ch,+1);
}
}
System.out.println(hm);
0Log in to Reply

PrepInsta Support Hey there, Kindly join our discord channel for all Technical queries. Our mentors are right there to help you with it.
0Log in to Reply

ARYAN import java.util.*;
public class Main
{
public static void main(String[] args) {
String str=”my name is aryan kumar saw”;
HashMap map=new HashMap();
for(int i=0;i<str.length();i++){
char c=str.charAt(i);
if(Character.isAlphabetic(c)){
if(map.containsKey(c)){
map.put(c,map.get(c)+1);
}else map.put(c,1);
}
} System.out.println(map);
}
}
2Log in to Reply

PrepInsta Support Hey!! Join our Discord Community
0Log in to Reply

Trinadh Kamaparapu import java.util.*;
public class Frec
{
public static void main(String[] args)
{
String str =”TrinadhNaidu”;
str=str.toLowerCase();
char test[] = str.toCharArray();
int n = str.length(); Map a = new HashMap(); for(char c:test)
{
if(a.containsKey(c))
{
a.put(c,a.get(c)+1);
}
else
{
a.put(c,1);
}
} for(Map.Entry m:a.entrySet())
{
System.out.println(m.getKey()+” “+m.getValue());
}
}
}
0Log in to Reply

Tridip import java.util.*;
public class Frec{ public static void frechar(String str){ char test[] = str.toCharArray();
int n = str.length(); Map a = new HashMap(); for(int i=0 ; i<n ; i++){ if(a.containsKey(test[i])){ a.put(test[i],a.get(test[i])+1);
}
else{ a.put(test[i],1);
}
} for(Map.Entry p :a.entrySet()){ System.out.println(p.getKey() +”Occurs” + p.getValue()); } } public static void main(String[] args){ String str =”Tridip”; frechar(str); }
}
0Log in to Reply

PrepInsta Support Hey, Join our TA Support Group on Discord, where we will help you out with all your queries:
Discord
0Log in to Reply

Palak Gupta public static void checkFrequency(String str) {
String[] freq = new String[str.length()];
boolean[] counted = new boolean[str.length()]; for (int i = 0; i < str.length(); i++) {
int count = 0;
if (!counted[i]) {
for (int j = i + 1; j < str.length(); j++) {
if (str.charAt(i) == str.charAt(j)) {
count++;
counted[j] = true;
}
}
freq[i] = String.valueOf(str.charAt(i)) + String.valueOf(count + 1);
}
} for (int k = 0; k < str.length(); k++) {
if (freq[k] != null) {
System.out.println(freq[k]);
}
}
}
0Log in to Reply

Akhilesh package com.prep.strings; import java.util.HashMap; public class FrequencyAkash {
public static void main(String[] args) { // char [] arr = {‘a’, ‘k’, ‘h’, ‘k’, ‘s’ ,’d’}; OR
String name = “aeiouieaeeee”; char [] str = name.toCharArray(); HashMap map = new HashMap();
// int count = 1; for(int i=0; i<name.length(); i++) {
int count = 1; for(int j=i+1; j<name.length(); j++) {
if(str[i] == str[j]) {
count++;
}
}
map.putIfAbsent(str[i], count);
// count = 1;
}
System.out.println(map);
}
}
0Log in to Reply

Srinjay Kapri import java.util.*; class jp { public static void main(String[] args) {
String s=”prepinsta”;
HashMaphm=new HashMap ();
for(int i=0;i“+hm.get(ch));
}
}
0Log in to Reply

theeksh18 package practice; public class Top100 { public static void main(String[] args) {
// TODO Auto-generated method stub
String string=”prepinsta insta”;
String s =””;
char arr[]=string.toCharArray(); for(int i=0;i<arr.length;i++) {
int c=1;
for(int j=i+1;j<arr.length;j++) {
if(arr[i]==arr[j])
{
c=c+1;
arr[j]=0;
} } if(arr[i]==0)
continue;
System.out.println(string.charAt(i)+" appears "+c); } System.out.println(s); } }
0Log in to Reply

Ankitha public class FrequencyOfChar {
public static void main(String args[]) {
Scanner sc = new Scanner(System.in);
String str = sc.nextLine(); char ff=’ ‘;int count=1;
char[] strc= str.toCharArray();
Arrays.sort(strc);
for(int i=0; i<strc.length; i++) {
count=1;
if(ff!=strc[i]) {
ff=strc[i];
for(int j=i+1; j”+count); }
} } }
1Log in to Reply

Vivek static void countFrequency(char[] c){
HashMap map = new HashMap();
for(int i = 0 ; i<c.length ; i++){
if(map.containsKey(c[i])){
map.replace(c[i],(map.get(c[i])+1));
}
else
map.put(c[i],1);
}
System.out.println("Iterating HashMap");
for(Map.Entry m : map.entrySet()){
System.out.println(m.getKey()+" "+m.getValue());
}
}
public static void main(String[] args) {
System.out.println("Enter String");
Scanner sc = new Scanner(System.in);
String str = sc.nextLine();
countFrequency(str.toCharArray());
}
1Log in to Reply

Mahesh import java.util.*;
public class Main
{
public static void main(String[] args) {
String s=”prepinsta”;
Mapmap=new HashMap();
for(int i=0;i “+entry.getValue()+” “);
}
}
}
0Log in to Reply

Mahesh String s=”prepinsta”;
Mapmap=new HashMap();
for(int i=0;i “+entry.getValue()+” “);
}
