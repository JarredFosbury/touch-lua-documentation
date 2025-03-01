System Library extends basic Lua API to be useful for iPhone platform.
Plus the ability to print stylized text.
Module name is **sys**.

**print** - same as Lua standard print but without adding new line
    
    sys.print( value_list)

**printin** - exactly as Lua standard print
    
    sys.printin( value_list)

**clear** - clears screen
    
    sys.clear()

**input** - prompts user to read line - without adding new line after prompt text
    
    v = sys.input prompt()
    prompt: prompt string
    v: user input

**sleep** - wait for specified time
    
    sys.sleep ( ms)
    ms: time is in milliseconds ( 1 second = 1000 millisecond )

**locate** - position cursor at specified location
    
    sys.locate (row, col) 
    row: cursor new row
    col: cursor new column
    
please note this is not like ordinary cursor locating this function only locates the cursor on previously printed text

**alert** - plays alert sound 
    
    sys.alert( name )
    name: text value
    
    one of: 'tink', 'tock', 'dtfm0', 'neg', 'drop', or 'vib'
    'vib' makes vibration

**gettime** - returns time in seconds (high resolution timer)
    
    time = sys.gettime()
    time : time in seconds since reference time
    
Hint: you usually use difference of two times.

**dir** - returns table of file names
    
    files = sys.dir( path)
    files = sys.dir()
    path: path of directory when omitted current path is used files: table populated with file/directory names

**docspath** - returns path of documents
    
    path = sys.docspath()

    out:
        path: string, absolute path of documents directory

**color** - create new color
    
    color = sys.color( red, green, blue, alpha)

    in:
        red: number, red component of color 
        green: number, green component of color 
        blue: number, blue component of color 
        alpha: number, alpha component of color 
    
    out:
        color: table, returned color (with red, green, blue, alpha)

Note:all values range in [0, 1]

**setcolor** - change text print color 
    
    sys.setcolor( color )

    in:
        color: table, new color (with red, green, blue, alpha) all new text printed with print functions will be colored with color

**setbgcolor** - change output view background color
    
    sys.setbgcolor color()
    
    in:
        color: table, views new background color (with red, green, blue, alpha)

**setfont** - change text font
    
    b = sys.setfont( name, size)
    
    in:
        name: string, font name
        size: number, font size (recommended values: 12 - 32, default: 18)
    
    out:
        b: bool, true is successful

**cprint** - print string with provided colors (no new line at end)
    
    sys.print( string, forecolor, backcolor )
    sys.cprint( string, forecolor ) 
    
    in:
        string: string, text to print forecolor: table, printed text color
        backcolor: table (Optional), printed text background color

**cprintin** - print string with provided colors (adds new line at end)
    
    sys.cprintln( string, forecolor, backcolor )
    sys.cprintin( string, forecolor ) 
    
    in:
        string: string, text to print forecolor: table, printed text color
        backcolor: table (Optional), printed text background color

**halt** - halt program (waits until user breaks program)
    
    sys.halt()
