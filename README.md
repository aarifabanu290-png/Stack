# Stack
Data Structure Practicle program
5.Stack for Browser History (Real Time Example)

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class BrowserStack:
    def __init__(self):
        self.top = None

    def visit(self, page):
        new = Node(page)
        new.next = self.top
        self.top = new
        print("Visited:", page)

    def back(self):
        if self.top is None:
            print("No pages")
        else:
            print("Back from:", self.top.data)
            self.top = self.top.next

    def show(self):
        temp = self.top
        while temp:
            print(temp.data)
            temp = temp.next

b = BrowserStack()
b.visit("Google")
b.visit("YouTube")
b.visit("Instagram")
b.show()
b.back()

5.Output:

Visited: Google
Visited: YouTube
Visited: Instagram
Instagram
YouTube
Google
Back from: Instagram
