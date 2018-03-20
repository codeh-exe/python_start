# python_start
# Todolist App with Python 2.7.

# -*-coding: utf-8 -*-

print "Welcome to the todolist app"

todos = ['Einkaufen', 'Waesche waschen', 'Gartenarbeit']

todos [1] = 'relaxen' #ersetzt den Eintrag an 1.Stelle  - Vorsicht Liste beginnt bei 0

print todos  

print todos [0] #gibt den Eintrag an der vordersten Stelle aus

print len(todos) #zählt die Elemente in der Liste

# index = 0
# while index < len(todos):
#     print todos[index]
#     index = index + 1

for todo in todos: #todo ist hier eine neue Variable
    print todo

add_todo = True

while add_todo:
    answer = raw_input('continue? ' )
    if answer != 'y':
        add_todo = False
    else:
        new_todo = raw_input ("Enter a new item: ") 
        todos.append (new_todo)
print 'Todos'
for todo in todos:
    print '* ' + todo

todo_file = open("todo.txt", "w+")

for todo in todos:
    todo_file.write (todo + '\n') #\t steht beispielsweise für einen Tab zwischen den Einträgen

todo_file.close ()
