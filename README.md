# python-practice-labs
It is my first repository for practice math and programming.
<br>
Author : Akash Sharma
# To create a quiz Bot for Mathmatical and General-Studies Quetions. 
# data of question
# import random first
import random
quiz_data = {
    'Math': [
        {'q':'What is the rank of Riemann curvature Tensor', 'a':'4'},
        {'q':"from which topic Young's Theorem belongs?", 'a': 'Partial Derivatives'}
         ],
         'General Studies': [
            {'q':'What is the full form of G.K ?', 'a': 'General Knowledge.'},
            {'q':'Where is the headquarters of Indian Railways?', 'a':'New Delhi'}
         ]

}
# select topic as input
def start_quiz():
    topic = input('select topic (Math/General Studies):')
    if topic in quiz_data:
        score = 0
        questions = quiz_data[topic]
        random.shuffle(questions)
        #for mix questions

        for item in questions:
            user_ans = input(f"{item['q']}:")
            if user_ans.lower() == item['a'].lower():
                print('Right Answer!')
                score += 1
            else:
                print(f'Wrong Answer:{item['a']}')


start_quiz()                


