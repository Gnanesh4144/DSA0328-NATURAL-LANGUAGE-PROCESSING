import nltk
from nltk.stem import PorterStemmer, LancasterStemmer, SnowballStemmer
from nltk.stem import WordNetLemmatizer
from nltk.tokenize import word_tokenize

nltk.download('punkt')
nltk.download('wordnet')
nltk.download('omw-1.4')

def perform_stemming(text):
    porter = PorterStemmer()
    lancaster = LancasterStemmer()
    snowball = SnowballStemmer(language='english')

    words = word_tokenize(text)

    porter_stems = [porter.stem(word) for word in words]
    lancaster_stems = [lancaster.stem(word) for word in words]
    snowball_stems = [snowball.stem(word) for word in words]

    print("Original Words:", words)
    print("Porter Stemmer:", porter_stems)
    print("Lancaster Stemmer:", lancaster_stems)
    print("Snowball Stemmer:", snowball_stems)

def perform_lemmatization(text):
    lemmatizer = WordNetLemmatizer()

    words = word_tokenize(text)

    lemmas = [lemmatizer.lemmatize(word) for word in words]

    print("Original Words:", words)
    print("Lemmatized Words:", lemmas)

def main():
    text = "The cats are chasing mice in the fields and running quickly."

    print("Performing Stemming:")
    perform_stemming(text)

    print("\nPerforming Lemmatization:")
    perform_lemmatization(text)

if __name__ == "__main__":
    main()
