<div align="center">

## Random String in C\#


</div>

### Description

This is the simplest and most straightforward random string generator I could come up with. Have fun. (Please don't use this if you're too lazy to rate it.)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Jon Davis](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/jon-davis.md)
**Level**          |Intermediate
**User Rating**    |4.4 (35 globes from 8 users)
**Compatibility**  |C\#
**Category**       |[Strings](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/strings__10-26.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/jon-davis-random-string-in-c__10-1058/archive/master.zip)





### Source Code

```
public static Random AppRandom = new Random((int)DateTime.Now.Ticks);
public static string RandomString(int length, bool nums) {
	const string abc = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
		+ "abcdefghijklmnopqrstuvwxyz";
	const string abc123 = abc + "0123456789";
	string charlist;
	if (nums) {
		charlist = abc123;
	} else {
		charlist = abc;
	}
	System.Text.StringBuilder sb = new System.Text.StringBuilder();
	for (int i=0;i<length;i++) {
		int r = AppRandom.Next(0, charlist.Length);
		sb.Append(charlist.Substring(r, 1));
	}
	return sb.ToString();
}
```

