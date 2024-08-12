# Meta Info
- Difficulty : Medium
- Duration : 30
- Type : CODE
- Language : PYTHON
- Id : 

# Additional Resources

<details>
<summary>Skills</summary>

| 스킬 아이디 | 스킬 이름      |
|--------|------------|
| -  | - |
| -      | - |
| -      | -          |
</details>

<details>
<summary>Data Sets</summary>

| 순번   | 파일 링크                  | 설명 | 
|------|------------------------|----|
| 1    | [codepresso_util.py](codepresso_util.py) |    |
| 2    | [large_inputs_5M.txt](large_inputs_5M.txt) |    |
| 3    | [large_inputs_10M.txt](large_inputs_10M.txt) |    |
| 4    | [large_inputs_17M.txt](large_inputs_17M.txt) |    |
| 5    | https://www.github.com |    |
| 6    | https://www.github.com |    |
</details>

# Description 
## EN
## Question
Group the strings that are anagrams from the given list. An anagram is a word formed by rearranging the letters of another word. For example, "eat," "ate," and "tea" belong to the same anagram group since they consist of the same letters.

<img style="max-height:100%;max-width:100%;" src="https://codepresso-global.s3.ap-northeast-2.amazonaws.com/coderun-resource/anagram_c7d8d566-6e38-49bf-8a08-93d0be3bae42.png" alt="Anagram">

## Instruction
- The input is a single list of strings `words`.
- Each string in `words` consists only of lowercase English letters.
- The length of each string is between 1 and 20 characters, inclusive.
- Output the anagram groups as a two-dimensional array of strings, where each group is represented as an inner array.
- The order of the groups and the order of strings within each group do not matter.
- The solution will be evaluated for efficiency.
- You are allowed to use the Python standard library.
- If needed, you may use the following list of prime numbers.
  - [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, 101]


## Example
### Example1 
Input:
```
["bat", "eat", "tea", "tan", "ate", "nat"]
```
Output:
```
[['eat', 'ate', 'tea'], ['tan', 'nat'], ['bat']]
```

### Example2
Input:
```
["stop", "post", "opts", "dusty", "parep", "diaper", "repaid", "tops", "paper", "study"]
```
Output:
```
[['diaper', 'repaid'], ['dusty', 'study'], ['opts', 'post', 'stop', 'tops'], ['paper', 'parep']]
```

### Example3
Input:
```
["listen", "evil", "gods", "silent", "veal", "rat", "vile", "tar", "live", "god", "enlist", "dog", "art", "dogs"]
```
Output:
```
[['art', 'rat', 'tar'], ['dog', 'god'], ['dogs', 'gods'], ['enlist', 'listen', 'silent'], ['evil', 'live', 'vile'], ['veal']]
```

# Description
## KO
## 문제
주어진 문자열 리스트에서 아나그램인 문자열들을 같은 그룹으로 묶으세요. 아나그램은 문자를 재배열하여 다른 단어를 만들 수 있는 경우를 의미합니다. 예를 들어, "eat", "ate", "tea"는 같은 알파벳으로 이루어진 단어 그룹이므로, 하나의 동일 아나그램 그룹입니다.

<img style="max-height:100%;max-width:100%;" src="https://codepresso-global.s3.ap-northeast-2.amazonaws.com/coderun-resource/anagram_c7d8d566-6e38-49bf-8a08-93d0be3bae42.png" alt="Anagram">

## 지침
- 입력은 단일 문자열 리스트 `words`로 주어집니다.
- 'words`의 각 문자열은 소문자 알파벳으로만 이루어져 있습니다.
- 각 문자열의 길이는 1 이상, 20 이하입니다.
- 아나그램 그룹을 이차원 문자열 배열로 출력하세요. 각 그룹은 내부 배열로 나타냅니다.
- 각 그룹의 순서와 그룹 내 문자열의 순서는 상관없습니다.
- 본 문제는 효율성 테스트가 포함됩니다.
- Python 표준 라이브러리를 사용할 수 있습니다.
- 필요시엔 다음의 소수 리스트를 사용할 수 있습니다.
  - [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, 101]
  
## 예시
### 예시1 
입력:
```
["bat", "eat", "tea", "tan", "ate", "nat"]
```
출력:
```
[['eat', 'ate', 'tea'], ['tan', 'nat'], ['bat']]
```

### 예시2
입력:
```
["stop", "post", "opts", "dusty", "parep", "diaper", "repaid", "tops", "paper", "study"]
```
출력:
```
[['diaper', 'repaid'], ['dusty', 'study'], ['opts', 'post', 'stop', 'tops'], ['paper', 'parep']]
```

### 예시3
입력:
```
["listen", "evil", "gods", "silent", "veal", "rat", "vile", "tar", "live", "god", "enlist", "dog", "art", "dogs"]
```
출력:
```
[['art', 'rat', 'tar'], ['dog', 'god'], ['dogs', 'gods'], ['enlist', 'listen', 'silent'], ['evil', 'live', 'vile'], ['veal']]
```

# Editor
```python
from codepresso_util import validate

def find_anagram_groups(words):
    # $ANNOTATION_1




# $ANNOTATION_2
if __name__ == '__main__':
    validate(find_anagram_groups)
```

# Correct Answer
```python
from codepresso_util import validate
from collections import defaultdict

def find_anagram_groups(words):
    # $ANNOTATION_1
    anagrams = defaultdict(list)
    for s in words:
        key = ''.join(sorted(s))
        anagrams[key].append(s)
    return list(anagrams.values())

# $ANNOTATION_2
if __name__ == '__main__':
    validate(find_anagram_groups)
```

# Output
```
True
```
