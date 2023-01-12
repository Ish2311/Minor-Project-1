# Minor-Project-1
This Project include's Countdown Timer with features like Reset, Stop, Pause, Resume.
# Creating a CounDown Class
class CountDown:
    def __init__(self, root):
        self.window = root
        self.window.geometry("480x320+0+0")
        self.window.title('CountDown Timer')
        # Tkinter window background color
        self.window.configure(bg='gray35')
        # Fixing the Window length constant
        self.window.resizable(width = False, height = False)

        # Declaring a variable to pause the countdown time
        self.pause = False

        # The Start and Pause buttons are placed
        # inside this frame
        self.button_frame = Frame(self.window, bg="gray35", \
        width=240, height=40)
        self.button_frame.place(x=230, y=150)
        # This frame is used to show the countdown time label
        self.time_frame = Frame(self.window, bg="gray35", \
        width=480, height=120).place(x=0, y=210)

        # Tkinter Labels
        time_label = Label(self.window, text="Set Time", 
        font=("times new roman",20, "bold"), bg='gray35',fg='yellow')
        time_label.place(x=180, y=30)

        hour_label = Label(self.window, text="Hour", 
        font=("times new roman",15), bg='gray35', fg='white')
        hour_label.place(x=50, y=70)
