combinations-of-well-formed-brackets
====================================

This is a typical job interview question. 

Write a function Brackets(int n) that prints all   combinations of well-formed brackets. For Brackets(3) the output would be:
 
 ((()))  
 (()())  
 (())()  
 ()(())  
 ()()()  
 
##solution
Written in ruby, but you get the idea. 

 ```ruby
def brackets output, open, close, pairs
  if open == pairs and close == pairs
    p output
  else
    foo output+'(', open+1, close, pairs if open<pairs      
    foo output+')', open, close+1, pairs if close<open      
  end
end

brackets('', 0, 0, 3)
 ```
