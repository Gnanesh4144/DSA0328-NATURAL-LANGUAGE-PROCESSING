class FiniteStateAutomaton:
    def __init__(self):
        self.current_state = 'q0'

    def transition(self, input_char):
        if self.current_state == 'q0':
            if input_char == 'a':
                self.current_state = 'q1'
            elif input_char == 'b':
                self.current_state = 'q0'
        elif self.current_state == 'q1':
            if input_char == 'a':
                self.current_state = 'q1'
            elif input_char == 'b':
                self.current_state = 'q2'
        elif self.current_state == 'q2':
            if input_char == 'a':
                self.current_state = 'q1'
            elif input_char == 'b':
                self.current_state = 'q0'

    def is_accepting(self):
        return self.current_state == 'q2'

    def recognize(self, input_string):
        self.current_state = 'q0'
        for char in input_string:
            self.transition(char)
        return self.is_accepting()

if __name__ == "__main__":
    fsa = FiniteStateAutomaton()

    test_strings = [
        "ab",
        "aab",
        "bab",
        "abab",
        "a",
        "b",
        "ba",
        "abb",
        "abc",
    ]

    for test_string in test_strings:
        result = fsa.recognize(test_string)
        print(f"String: '{test_string}' -> {'Accepted' if result else 'Rejected'}")
