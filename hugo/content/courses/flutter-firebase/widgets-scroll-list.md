---
title: Scroll
description: ListView and GridView for scrollable widgets
weight: 15
lastmod: 2019-07-13T10:13:30-04:00
draft: false
emoji: 🐦
vimeo: 336025503
---

## Example Code

{{< file "dart" "main.dart" >}}
{{< highlight dart >}}
class MyApp extends StatelessWidget {
 @override
 Widget build(BuildContext context) {
   return MaterialApp(
     home: Scaffold(
       body: ListView(
         scrollDirection: Axis.horizontal,
         children: _cards(),
       )
     ),
   );
 }

 List<Widget> _cards() {
   return [1,2,3,4,5,6,7,8,9].map((v) => Container(
       color: Colors.blue,
       margin: EdgeInsets.all(20),
       height: 100,
       child: Text('$v'),
     )
   ).toList();
 }

{{< /highlight >}}