<h1>ExpNo 8 : Solve Cryptarithmetic Problem,a CSP(Constraint Satisfaction Problem) using Python</h1> 
<h3>Name:               </h3>
<h3>Register Number/Staff Id:       </h3>
<H3>Aim:</H3>
<p>
    To solve Cryptarithmetic Problem,a CSP(Constraint Satisfaction Problem) using Python
</p>
<h3>Procedure:</h3>
Input and Output
<br>Input:
This algorithm will take three words.
<br> B A S E<br>
    B A L L<br>
           ----------<br>
           G A M E S<br>

Output:
It will show which letter holds which number from 0 – 9.
For this case it is like this.

              B A S E                         2 4 6 1
              B A L L                         2 4 5 5
             ---------                       ---------
            G A M E S                       0 4 9 1 6
Algorithm
For this problem, we will define a node, which contains a letter and its corresponding values.<br>

isValid(nodeList, count, word1, word2, word3)<br>

Input − A list of nodes, the number of elements in the node list and three words.<br>

Output − True if the sum of the value for word1 and word2 is same as word3 value.<br>
```
Initialize val1, val2, val3 to 0

m := 1
for each letter i from right to left in word1 do
    ch := word1[i]
    for each element j in nodeList do
        if nodeList[j].letter = ch then
            break  // Found matching letter
    end for
    val1 := val1 + (m * nodeList[j].value)
    m := m * 10
end for

m := 1
for each letter i from right to left in word2 do
    ch := word2[i]
    for each element j in nodeList do
        if nodeList[j].letter = ch then
            break
    end for
    val2 := val2 + (m * nodeList[j].value)
    m := m * 10
end for

m := 1
for each letter i from right to left in word3 do
    ch := word3[i]
    for each element j in nodeList do
        if nodeList[j].letter = ch then
            break
    end for
    val3 := val3 + (m * nodeList[j].value)
    m := m * 10
end for

if val3 = (val1 + val2) then
    return true
else
    return false
end if
```
<hr>
<h2>Sample Input and Output:</h2>
SEND = 9567<br>
MORE = 1085<br>
<hr>
MONEY = 10652<br>
<hr>
<h2>Result:</h2>
<p> Thus a Cryptarithmetic Problem was solved using Python successfully</p>
