import re

def demonstrate_regex():
    text = """
    Hello, my email is gnaneshyarramanayuni2004@gmail.com and my phone number is 7780345601.
    You can also reach me at 192124169.sse@saveetha.com or 7780345601.
    """

    email_pattern = r'[\w\.-]+@[\w\.-]+'
    
    phone_pattern = r'\(?\d{3}\)?[-.\s]?\d{3}[-.\s]?\d{4}'

    print("Searching for email addresses:")
    emails = re.findall(email_pattern, text)
    for email in emails:
        print(f"Found email: {email}")

    print("\nSearching for phone numbers:")
    phones = re.findall(phone_pattern, text)
    for phone in phones:
        print(f"Found phone number: {phone}")

    print("\nMatching a specific pattern at the beginning of the text:")
    match = re.match(r'Hello', text)
    if match:
        print("Found 'Hello' at the beginning of the text.")
    else:
        print("Did not find 'Hello' at the beginning of the text."
)
    print("\nSearching for a pattern anywhere in the text:")
    search = re.search(r'gnanesh', text)
    if search:
        print(f"Found 'gnanesh' at position {search.start()}.")
    else:
        print("Did not find 'gnanesh' in the text.")

    print("\nExtracting groups using regex:")
    group_pattern = r'(\d{3})-(\d{3})-(\d{4})'
    group_match = re.search(group_pattern, text)
    if group_match:
        print(f"Full match: {group_match.group(0)}")
        print(f"Area code: {group_match.group(1)}")
        print(f"Central office code: {group_match.group(2)}")
        print(f"Line number: {group_match.group(3)}")
    else:
        print("No match found for the group pattern.")

if __name__ == "__main__":
    demonstrate_regex()
