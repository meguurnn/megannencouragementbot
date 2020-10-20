# megannencouragementbot
print("Title of program: megannencouragementbot")
print()
while True:
  description = input("describe how you feel in a sentence :)")

  list_of_words = description.split()

  feelings_list = []
  encouragement_list = []
  counter = 0

  for each_word in list_of_words:

    if each_word == "happy":
      feelings_list.append("happy")
      encouragement_list.append("happy for you too! enjoy yourself")
      counter += 1
    if each_word == "disappointed":
      feelings_list.append("disappointed")
      encouragement_list.append("there is always a next time to do well! cheer up :)")
      counter += 1
    if each_word == "tired":
      feelings_list.append("tired")
      encouragement_list.append("go get some rest, you deserve it <3")
      counter += 1
    if each_word == "sad":
      feelings_list.append("sad")
      encouragement_list.append("talk to someone, you'll feel better :")")
      counter += 1

  if counter == 0:

      output = "sorry, i could not really comprehend it. could you try using simpler words?"

  elif counter == 1:

      output = "It seems that you are feeling quite " + feelings_list[0] + ". However, do remember that "+ encouragement_list[0] + "! Hope you feel better :)"  

  else:

    feelings = ""    
    for i in range(len(feelings_list)-1):
      feelings += feelings_list[i] + ", "
    feelings += "and " + feelings_list[-1]

    encouragement = ""    
    for j in range(len(encouragement_list)-1):
      encouragement += encouragement_list[i] + ", "
    encouragement += "and " + encouragement_list[-1]

    output = "It seems that you are feeling quite " + feelings + ". Please always remember "+ encouragement + "! Hope you feel better :)"

  print()
  print(output)
  print()
