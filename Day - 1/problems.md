## Common Problems Using This Pattern
### 🟢 Valid Anagram

#### Check if two strings contain the same characters with the same counts.

    int freq[26] = {0};
    
    for(char ch : s) freq[ch - 'a']++;
    for(char ch : t) freq[ch - 'a']--;
    
    for(int i = 0; i < 26; i++) {
        if(freq[i] != 0) return false;
    }
    return true;

### 🟡 First Non-Repeating Character

#### Find the first character that appears exactly once.

    int freq[26] = {0};
    
    for(char ch : s) freq[ch - 'a']++;
    
    for(char ch : s) {
        if(freq[ch - 'a'] == 1)
            return ch;
    }
    
    return '#';

### 🟡 Majority Element

#### Find the element that appears more than n/2 times.

    unordered_map<int, int> freq;
    int n = nums.size();
    
    for(int x : nums) freq[x]++;
    
    for(auto it : freq) {
        if(it.second > n / 2)
            return it.first;
    }

### 🔵 Sliding Window + Frequency

#### Used in substring problems (e.g., at most k distinct characters).

Key idea:
- Expand window → add frequency
- Shrink window → reduce frequency
