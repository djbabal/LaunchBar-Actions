(* Takes a string in the format 
	notetitle : notebody
Adds this to evernote as a new note in the default notebook
The : is used to split the note title and body*)
on handle_string(notetext)
	set {astid, AppleScript's text item delimiters} to {AppleScript's text item delimiters, ": "}
	set {notetitle, notebody} to {text item 1 of notetext, text item 2 of notetext}
	set AppleScript's text item delimiters to astid
	tell application "Evernote" to create note title notetitle with text notebody
	tell application "LaunchBar" to display in large type "Note Added"
end handle_string
