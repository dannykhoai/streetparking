# streetparking
Custom trained car recognition for street parking

I live in a great city: perfect nature, good accessibilty, cool people, peaceful neighborhood. 
Except its parking access.

In short, I need to know whether those street parking spaces are available in order to fit my car in. I could do it with manually by keep checking out from the window.
Or I use Object detection - Machine learning?

Tensorflow comes to the rescue. And here is my plan:
1. Set up a camera pointing out of the window (DONE)
2. RTSP stream that takes image outside for the interval of every 1min (DONE)
3. Tensorflow reads how many cars occupying the space 
3a. So many good models out there, however none seems to be suitable with webcam blurry resolution.
 So I trained a custom model using Tensorflow Objectdecection API (Ran on Mac Pro CPU, takes 5days) 
3b. Figuring out the zone for desired detection (Ongoing)
4. Send data to a frontend site / or Telegram Bot sending signal.

