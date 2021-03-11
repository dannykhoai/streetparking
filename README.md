# streetparking
Custom trained car recognition for street parking

I live in a great neighborhood: perfect nature, good accessibilty, cool peeps living around. <br>
Except its parking access.

In short, I need to know whether those street parking spaces are available in order to fit my car in.
I could do it with manually by keep looking out from the window.<br>
Or I use Object detection - Machine learning?



Tensorflow comes to the rescue. And here is my plan:
1. Set up a camera pointing out of the window (DONE)
2. RTSP stream that takes image outside for the interval of every 1min (DONE) <br>
 $ffmpeg -y -i rtsp://admin@192.168.1.xyz:554/live -vframes 1 pic.jpg <br>
3. Tensorflow reads how many cars occupying the space <br>
3a. So many good models out there, however none seems to be suitable with webcam blurry resolution & varied Finnish weather conditions.<br>
 So I trained a custom model using Tensorflow Objectdecection API (Ran on Mac Pro CPU, takes 5days xD)  <br>
 
 ![alt text](https://github.com/dannykhoai/streetparking/blob/master/snow%20ok.png?raw=true)
 It works <br>
 ![alt text](https://github.com/dannykhoai/streetparking/blob/master/dark%20ok.png?raw=true)

 
3b. Figuring out the zone for desired detection (Ongoing) <br>
4. Converting to a TF Lite model and implement it on Raspberry Pi (Ongoing) <br>
5. Send data to a frontend site / or Telegram Bot sending signal. (Pending) <br>

