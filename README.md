import 'package:flutter/material.dart';

 
void main() => runApp(new MyApp());

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return new MaterialApp(
        title: 'Usuarios',
        theme: new ThemeData(primarySwatch: Colors.green),
        home: Scaffold(
            appBar: AppBar(title: Text('Usuarios')),
            body: new ListView(children: [
              _buildItem('John Alomoto!'),
              _buildItem('Ronal Roserp!'),
              _buildItem('Martha Alban!'),
              _buildItem('Matel del cisne!')
            ])));
  }
}

Widget _buildItem(String textTitle) {
  return new ListTile(
    title: new Text(textTitle),
    subtitle: new Text('Nombre de Usuario'),
    leading: new Icon(Icons.person),
    onTap: () {
      print(textTitle);
    },
  );
}
