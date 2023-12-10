class FootballTrainingApp:
    def __init__(self):
        self.drills = {
            'endurance': [
                ('Jogging', 'Maintain a steady pace for a set duration to build stamina.'),
                ('Sprint Intervals', 'Alternate between sprinting and walking to improve cardiovascular fitness.'),
                ('Hill Runs', 'Run uphill to increase leg strength and endurance.'),
                ('Circuit Training', 'Perform a series of exercises with minimal rest for overall endurance.'),
                ('Fartlek Training', 'Vary your speed and intensity during a continuous run.')
            ],
            'dribbling': [
                ('Cone Dribbling', 'Dribble around a series of cones to improve ball control.'),
                ('Wall Passes', 'Use a wall to practice passing and receiving to enhance touch.'),
                ('One-on-One Dribble', 'Practice dribbling against a single defender to improve under pressure.'),
                ('Figure-Eight Dribbling', 'Dribble in a figure-eight pattern around two objects to improve agility.'),
                ('Close Ball Control', 'Practice keeping the ball close in tight spaces.')
            ],
            'shooting': [
                ('Target Practice', 'Aim and shoot at specific targets in the goal to enhance accuracy.'),
                ('Shooting from Crosses', 'Practice shooting from crosses to improve timing and finishing.'),
                ('Penalty Kicks', 'Practice penalty kicks focusing on placement and composure.'),
                ('Long-Range Shots', 'Practice shooting from outside the penalty box.'),
                ('Volley Shots', 'Work on hitting the ball on the volley for dynamic shooting.')
            ],
            'defense': [
                ('Tackling Drills', 'Practice different tackling techniques to dispossess opponents.'),
                ('Positional Play', 'Learn to position correctly to intercept passes and block shots.'),
                ('Defensive Headers', 'Practice heading the ball clear from defensive situations.'),
                ('1v1 Defending', 'Work on defending against an attacker in one-on-one situations.'),
                ('Group Defending', 'Practice defending in groups to maintain team shape.')
            ],
            'goalkeeping': [
                ('Dive Saves', 'Practice diving to make saves in different directions.'),
                ('Handling Crosses', 'Work on catching or punching crosses in crowded areas.'),
                ('Shot Reaction', 'Improve reaction times to shots from close range.'),
                ('Footwork Drills', 'Practice quick foot movements to improve positioning.'),
                ('One-on-One Situations', 'Work on closing down attackers in one-on-one scenarios.')
            ]
        }

    def display_menu(self):
        print("Welcome to the Football Training App")
        print("Choose your training focus from the following options:")
        for focus in self.drills.keys():
            print(f"- {focus.capitalize()}")

    def get_user_choice(self):
        choice = input("Enter your training focus: ").lower()
        while choice not in self.drills:
            print("Invalid choice. Please try again.")
            choice = input("Enter your training focus: ").lower()
        return choice

    def display_drills(self, focus):
        print(f"\nRecommended Drills for {focus.capitalize()}:")
        for drill, description in self.drills[focus]:
            print(f"- {drill}: {description}")

    def run(self):
        self.display_menu()
        user_choice = self.get_user_choice()
        self.display_drills(user_choice)


if __name__ == "__main__":
    app = FootballTrainingApp()
    app.run()
