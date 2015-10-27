# gtk_in_qt

![input pixmap](https://github.com/admica/gtk_in_qt/blob/master/input.png)

Testing Running Gtk apps within Qt containers.

* This is a qt application process spawning a seperate process to run a gtk app and devouring the gtk processes window ID to contain the whole process. This allows Qt to have complete control over the gtk app and see all events, mouse, keyboard, etc.

Also this test app is looking at performance of pixmap loading, drawing, and output saving without ever showing any widgets graphically.

* This would be useful for performing background batch pixmap processing.

win.show() is never called unless you connect to the tcp socket server, so this is also a test of QTcpServer.

* I did it this way because chicken-egg. Only the connect signal is implemented so you have a way to show the window after running it.
* netcat would be a simple way to test this, for example: <i>nc 127.0.0.1 8000</i>

All of the tests are run from the main. You may need to uncomment the method calls because it would be checked in with some commented out as I was testing one at a time in the end.
