# Adding custom fonts

**You're totally free to add custom fonts to your Baker project, provided that you hold the necessary rights to do so.**

**Credits:**
This guides has been forked from the original [PugPig][1] documentation guide about [Embedding Fonts][2].


### Adding fonts:

1. Add fonts you wish to include in your app in a folder with a meaningful name i.e. “Fonts”
2. Open your Baker project in Xcode, right click inside the project navigator and select "Add fonts to your [Name] project" and choose the previously created directory.
3. Select radio button “create groups from added folders” and click “add”.
4. open the file: <project name>.plist
5. Select any of the keys in the plist file and press the ”+” button to add a new key. Add a new key named “Fonts provided by application” (array). Click the disclosure triangle to add fonts to your array. Under the value column of each item in the array, type the name of the font including the file's extension.


### Using embedded fonts

```css
@font-face {
font-family: 'MyFont Sans';
	src: local('MyFontSans'), url('fonts/MyFont-Sans.otf') format('opentype');
	font-weight: normal;
	font-style: normal;
}
```

The local definition in the font must match the font name that you have embedded in your app. Note that this doesn't necessarily match the filename - it will be the name you would use to load the font in iOS using UIFont's fontWithName call. If you are unsure of your font's name, you can use some helper code to find the font family. Locate your `BKRAppDelegate.m` file and use the following snippet :

```obj-c
NSArray \*fn = [UIFont familyNames];
NSLog(@"Families: %@", fn);
```
Now you see the actual font family name as it is seen by the system. To list all fonts from that family you could now use:

```obj-c
SArray \*fn = [UIFont familyNames];
NSLog(@"Families: %@", fn);
and then find the actual font name by listing all fonts from that family:
NSArray \*fn2 = [UIFont fontNamesForFamilyName:@"NameOfYourFontFamily"];
NSLog(@"Fonts: %@", fn2);
```

Once the font face has been defined, it can be used in the normal way. For example,

```css
h1 {
	font-family:'MyFont Sans'
}
```

### Using embedded fonts in Obj-C

UILabel example:

```obj-c
[yourLabelName setFont:[UIFont fontWithName:@"MyFontSans" size:18]];
```

### Dynamic type fonts support
Please refer to the Official Baker guide about the topic
[Dynamic type fonts support][3]

### Resources

- [iOS Fonts][4]
- [Google Fonts][5]
- [Font Squirrel][6]
- [The 30 Best Free Open-Source Web Fonts by Typewolf][7]

[1]:	http://pugpig.com/
[2]:	https://pugpig.zendesk.com/hc/en-us/articles/200967987-Embedding-Fonts
[3]:	https://github.com/bakerframework/baker/wiki/Dynamic-type-fonts-support
[4]:	http://iosfonts.com/
[5]:	http://www.google.com/fonts
[6]:	http://www.fontsquirrel.com/
[7]:	http://www.typewolf.com/open-source-web-fonts
