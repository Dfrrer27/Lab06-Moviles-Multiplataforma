# Lab06-Moviles-Multiplataforma - CODIGO DEL ARCHIVO main.dart

    import 'package:flutter/material.dart';
    
    void main() {
      runApp(const MyApp());
    }
    
    //Stateless, son metodos estaticos
    class MyApp extends StatelessWidget {
      const MyApp({super.key});
    
      // This widget is the root of your application.
      @override
      Widget build(BuildContext context) {
        return MaterialApp(
          title: 'Flutter Demo',
          theme: ThemeData(
            primarySwatch: Colors.amber,
          ),
          debugShowCheckedModeBanner: false,
          home: Scaffold(
            body: Column(
              children: <Widget>[
    
                Expanded(  
                    child: Container(
                      color: Colors.red,
                      margin: const EdgeInsets.all(20),
                      child: Row(
                        mainAxisAlignment: MainAxisAlignment.center,
                        children: const <Widget>[
                          Text("Parchis Colors:", 
                              style: TextStyle(
                                fontSize: 12, fontWeight: FontWeight.bold)),
                        ],
                      )
                    ),
                ),
    
                Expanded(
                  child: Row(children: <Widget>[
    
                    Expanded(
                      child: CustomButton(
                        number: "7",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: "8",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: "9",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButtonOperation(
                        number: "x",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                  ]),
                ),        
               
                Expanded(
                  child: Row(children: <Widget>[
    
                    Expanded(
                      child: CustomButton(
                        number: "4",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: "5",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: "6",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButtonOperation(
                        number: "-",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                  ]),
                ), 
    
                Expanded(
                  child: Row(children: <Widget>[
    
                    Expanded(
                      child: CustomButton(
                        number: "1",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: "2",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: "3",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButtonOperation(
                        number: "+",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                  ]),
                ), 
    
                Expanded(
                  child: Row(children: <Widget>[
    
                    Expanded(
                      child: CustomButton(
                        number: "0",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButton(
                        number: ",",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                    Expanded(
                      child: CustomButtonOperation(
                        number: "=",
                        onPressed: () {
                          print('wasa');
                        },
                      )
                    ),
    
                  ]),
                ), 
    
              ],
            ),
            
          )
        );
      }
    }
    
    class CustomButton extends StatelessWidget {
      final String number;
      final VoidCallback onPressed;
    
      const CustomButton({
        required this.number,
        required this.onPressed,
      });
    
      @override
      Widget build(BuildContext context) {
        return Container(
          margin: const EdgeInsets.all(5),
          width: 50,
          height: 50,
          decoration: BoxDecoration(
            color: Color.fromARGB(26, 104, 100, 100),
            borderRadius: BorderRadius.circular(100),
          ),
          child: TextButton(
            onPressed: onPressed,
            child: Text(
              '$number',
              style: TextStyle(
                color: Colors.black,
                fontSize: 24,
              ),
            ),
          ),
        );
      }
    }
    
    class CustomButtonOperation extends StatelessWidget {
      final String number;
      final VoidCallback onPressed;
    
      const CustomButtonOperation({
        required this.number,
        required this.onPressed,
      });
    
      @override
      Widget build(BuildContext context) {
        return Container(
          margin: const EdgeInsets.all(20),
          width: 50,
          height: 50,
          decoration: BoxDecoration(
            color: Colors.blueAccent,
            borderRadius: BorderRadius.circular(100),
          ),
          child: TextButton(
            onPressed: onPressed,
            child: Text(
              '$number',
              style: TextStyle(
                color: Colors.white,
                fontSize: 24,
              ),
            ),
          ),
        );
      }
    }
