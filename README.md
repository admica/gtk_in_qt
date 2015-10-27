# gtk_in_qt

Testing Running Gtk apps within Qt containers.

* This is a qt application process spawning a seperate process to run a gtk app and devouring the gtk processes window ID to contain the whole process. This allows Qt to have complete control over the gtk app and see all events, mouse, keyboard, etc.

Also this test app is looking at performance of pixmap loading, drawing, and output saving without ever showing any widgets graphically.

* This would be useful for performing background batch pixmap processing.
