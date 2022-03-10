In this project I will show you how to manipulate objects detected with Tensorflow Models. This can be done by editing a single file. The "draw_bounding_box_on_image" functions in the visualization_utils.py file under the utils directory of TensorFlow Models has been added. You can view the added code block below.

In this project, since the name of the detected object will be recorded in the Firebase database, adding it to the Firebase database is also shown.

    # ***************************
    
    # Get detected object name
    
    str_arr = display_str_list[0].split(":")

    
    # firebase-begin
    
    if(str_arr[0] == DetectedObjectName):
            fb = firebase.FirebaseApplication('yourFirebaseConnection', None)
            fb.put('/',"firebaseDirectory",str_arr[0])
    else:
            fb = firebase.FirebaseApplication('yourFirebaseConnection', None)
            fb.put('/',"firebaseDirectory",str_arr[0])
    
    # firebase-end
    
    
    # ***************************
