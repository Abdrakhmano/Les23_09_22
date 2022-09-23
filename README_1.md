### Task №1(6kyu)
Create a function taking a positive integer as its parameter and returning a string containing the Roman Numeral representation of that integer.

Modern Roman numerals are written by expressing each digit separately starting with the left most digit and skipping any digit with a value of zero. In Roman numerals 1990 is rendered: 1000=M, 900=CM, 90=XC; resulting in MCMXC. 2008 is written as 2000=MM, 8=VIII; or MMVIII. 1666 uses each Roman symbol in descending order: MDCLXVI.

[Task_link](https://www.codewars.com/kata/51b62bf6a9c58071c600001b/train/java)

#### Solution
~~~ Java
public class Conversion {

    public String solution(int n) {
      String result = "";
        if (n < 4000 && n != 0) {
            if (n / 1000 != 0) {
                if (n / 1000 == 1) result = result + "M";
                if (n / 1000 == 2) result = result + "MM";
                if (n / 1000 == 3) result = result + "MMM";
                if (n / 100 % 10 == 1) result = result + "C";
                if (n / 100 % 10 == 2) result = result + "CC";
                if (n / 100 % 10 == 3) result = result + "CCC";
                if (n / 100 % 10 == 4) result = result + "CD";
                if (n / 100 % 10 == 5) result = result + "D";
                if (n / 100 % 10 == 6) result = result + "DC";
                if (n / 100 % 10 == 7) result = result + "DCC";
                if (n / 100 % 10 == 8) result = result + "DCCC";
                if (n / 100 % 10 == 9) result = result + "CM";
                if (n % 100 / 10 == 1) result = result + "X";
                if (n % 100 / 10 == 2) result = result + "XX";
                if (n % 100 / 10 == 3) result = result + "XXX";
                if (n % 100 / 10 == 4) result = result + "XL";
                if (n % 100 / 10 == 5) result = result + "L";
                if (n % 100 / 10 == 6) result = result + "LX";
                if (n % 100 / 10 == 7) result = result + "LXX";
                if (n % 100 / 10 == 8) result = result + "LXXX";
                if (n % 100 / 10 == 9) result = result + "XC";
                if (n % 1000 % 100 % 10 == 1) result = result + "I";
                if (n % 1000 % 100 % 10 == 2) result = result + "II";
                if (n % 1000 % 100 % 10 == 3) result = result + "III";
                if (n % 1000 % 100 % 10 == 4) result = result + "IV";
                if (n % 1000 % 100 % 10 == 5) result = result + "V";
                if (n % 1000 % 100 % 10 == 6) result = result + "VI";
                if (n % 1000 % 100 % 10 == 7) result = result + "VII";
                if (n % 1000 % 100 % 10 == 8) result = result + "VIII";
                if (n % 1000 % 100 % 10 == 9) result = result + "IX";
            } else if (n / 1000 == 0) {
                if (n / 100 == 1) result = result + "C";
                if (n / 100 == 2) result = result + "CC";
                if (n / 100 == 3) result = result + "CCC";
                if (n / 100 == 4) result = result + "CD";
                if (n / 100 == 5) result = result + "D";
                if (n / 100 == 6) result = result + "DC";
                if (n / 100 == 7) result = result + "DCC";
                if (n / 100 == 8) result = result + "DCCC";
                if (n / 100 == 9) result = result + "CM";
                if (n / 10 % 10 == 1) result = result + "X";
                if (n / 10 % 10 == 2) result = result + "XX";
                if (n / 10 % 10 == 3) result = result + "XXX";
                if (n / 10 % 10 == 4) result = result + "XL";
                if (n / 10 % 10 == 5) result = result + "L";
                if (n / 10 % 10 == 6) result = result + "LX";
                if (n / 10 % 10 == 7) result = result + "LXX";
                if (n / 10 % 10 == 8) result = result + "LXXX";
                if (n / 10 % 10 == 9) result = result + "XC";
                if (n % 100 % 10 == 1) result = result + "I";
                if (n % 100 % 10 == 2) result = result + "II";
                if (n % 100 % 10 == 3) result = result + "III";
                if (n % 100 % 10 == 4) result = result + "IV";
                if (n % 100 % 10 == 5) result = result + "V";
                if (n % 100 % 10 == 6) result = result + "VI";
                if (n % 100 % 10 == 7) result = result + "VII";
                if (n % 100 % 10 == 8) result = result + "VIII";
                if (n % 100 % 10 == 9) result = result + "IX";
            } else if (n / 100 == 0) {
                if (n / 10 == 1) result = result + "X";
                if (n / 10 == 2) result = result + "XX";
                if (n / 10 == 3) result = result + "XXX";
                if (n / 10 == 4) result = result + "XL";
                if (n / 10 == 5) result = result + "L";
                if (n / 10 == 6) result = result + "LX";
                if (n / 10 == 7) result = result + "LXX";
                if (n / 10 == 8) result = result + "LXXX";
                if (n / 10 == 9) result = result + "XC";
                if (n % 10 == 1) result = result + "I";
                if (n % 10 == 2) result = result + "II";
                if (n % 10 == 3) result = result + "III";
                if (n % 10 == 4) result = result + "IV";
                if (n % 10 == 5) result = result + "V";
                if (n % 10 == 6) result = result + "VI";
                if (n % 10 == 7) result = result + "VII";
                if (n % 10 == 8) result = result + "VIII";
                if (n % 10 == 9) result = result + "IX";
            } else if (n / 100 == 0) {
                if (n == 1) result = result + "I";
                if (n == 1) result = result + "II";
                if (n == 1) result = result + "III";
                if (n == 1) result = result + "IV";
                if (n == 1) result = result + "V";
                if (n == 1) result = result + "VI";
                if (n == 1) result = result + "VII";
                if (n == 1) result = result + "VIII";
                if (n == 1) result = result + "IX";
            }
        } else result = result + "Число,превышающее 3999";
        return result;
    }
}
~~~ 

#### Fav Solution
~~~ Java
public class Conversion {

    public String solution(int number) {
        String romanNumbers[] = {"M", "CMXC", "CM", "D", "CDXC", "CD", "C", "XC", "L", "XL", "X", "IX", "V", "IV", "I"};
        int arab[] = {1000, 990, 900, 500, 490, 400, 100, 90, 50, 40, 10, 9, 5, 4, 1};
        StringBuilder result = new StringBuilder();
        int i = 0;
        while (number > 0 || arab.length == (i - 1)) {
            while ((number - arab[i]) >= 0) {
                number -= arab[i];
                result.append(romanNumbers[i]);
            }
            i++;
        }
        return result.toString();
    }
}
~~~

#### Comment:
Во время выполнения задачи №1 было интересно заниматься с Римскими цифрами.

### Task №2(7kyu)

Return the number (count) of vowels in the given string.

We will consider a, e, i, o, u as vowels for this Kata (but not y).

The input string will only consist of lower case letters and/or spaces.

[Task_link](https://www.codewars.com/kata/54ff3102c1bad923760001f3/train/java)

#### Solution

~~~ Java 
public class Vowels {
    public static int getCount(String str) {
        int i = 0;
        int j = 0;
        int k = str.length() - 1;
        while (j <= k) {
            if (str.charAt(j) == 'a' || str.charAt(j) == 'e' || str.charAt(j) == 'i' || str.charAt(j) == 'o' || str.charAt(j) == 'u') {
                i++;
            }
            j++;
        }
        return i;
    }
}
~~~

#### Fav Solution

~~~ Java
public class Vowels {

    public static int getCount(String str) {
        return str.replaceAll("(?i)[^aeiou]", "").length();
    }

}
~~~

