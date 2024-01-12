class Solution {
public:
    bool halvesAreAlike(string s) {
        unordered_set<char> vowels = {'a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U'};
        int CountVowels = 0;
        int mid = s.length() / 2;

        for (int i = 0; i < mid; i++) {
            char charA = s[i];
            char charB = s[mid + i];
            if (vowels.count(charA)) CountVowels++;
            if (vowels.count(charB)) CountVowels--;
        }
        if (CountVowels==0){
            return true ;
        }
       else{
           return false ;

       } 
        //return CountVowels == 0;
    }
};
