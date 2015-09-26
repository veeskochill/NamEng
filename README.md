Reccomendation Engine For names:

Steps:
Extract features from names
features : num and type of syllables, char frequency, word length, first and last char
additional features : who prefers name

output : pick from list of names.
alternative : generate name

Extracting Syllables
http://www.nltk.org/
http://stackoverflow.com/questions/405161/detecting-syllables-in-a-word
'''
from nltk.corpus import cmudict
d = cmudict.dict()
def nsyl(word):
  return [len(list(y for y in x if y[-1].isdigit())) for x in d[word.lower()]]
'''
