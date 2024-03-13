

import os

def search_string(path, str):
    f = os.walk(path)
    for root, dirs, files in f:
        for file in files:
            j = open(path + file, 'r', encoding='utf-8-sig')
            file_contents = j.readlines()
            for content in file_contents:
                if str in content:
                    print(file)
                    
path = r"C:\\code"
str = 'str'
search_string(path, str)
