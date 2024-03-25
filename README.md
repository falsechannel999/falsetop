import 'package:flutter/material.dart';



void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});


  @override
  Widget build(BuildContext context) {
    return const MaterialApp(
      title: 'Maserati Store',
      home: HomePage(),
    );
  }
}

class ExampleButton extends StatelessWidget {
  final String text;
  const ExampleButton({Key? key, required this.text}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Text(text, style: TextStyle(fontSize: 20),);
  }
}

class ExampleTextField extends StatelessWidget {
  final String HintText;
  final int MAXLength;
  const ExampleTextField({Key? key, required this.HintText, required this.MAXLength}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return TextField(
      decoration: InputDecoration(
          border: OutlineInputBorder(),
          prefixIcon: Icon(Icons.lock),
          hintText: HintText
      ),
      maxLength: MAXLength,
    );
  }
}


class HomePage extends StatelessWidget {
  const HomePage ({super.key});

  @override
  Widget build(BuildContext context) {
    return   Scaffold(
      body: Container(
        alignment: Alignment.center,
        color: Colors.white,
        child: Column(
          children: <Widget>[
            Expanded(

                flex: 4,
                child: Container(
                  alignment: Alignment.center,
                  child: Image.network('data:image/png;base64,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'),
                )
            ),
            Expanded(
                flex: 2,
                child: Container(
                  width: 200,
                  height: 10,
                  alignment: FractionalOffset(0.0, 0.8),
                  color: Colors.white,
                  child: TextField(
                    decoration: InputDecoration(
                        prefixIcon: Icon(Icons.account_box_sharp),
                        border: OutlineInputBorder(),
                        hintText: 'Введите логин:'
                    ),
                    maxLength: 30,
                  ),
                )
            ),
            Expanded(
                flex: 2,
                child: Container(
                    width: 200,
                    height: 10,
                    alignment: FractionalOffset(0.0, 0.02),
                    color: Colors.white,
                    child: ExampleTextField(HintText: 'Введите пароль:', MAXLength: 30)
                )
            ),
            Expanded(
                child: Container(

                  alignment: FractionalOffset(0.5, 0.01),
                  margin: EdgeInsets.only(bottom: 8),
                  child: ElevatedButton(
                      child: ExampleButton(text: 'Войти'),
                      onPressed: (){
                        Navigator.push(
                            context,
                            MaterialPageRoute(builder: (context) => const Login())
                        );
                      }
                  ),
                )
            ),
            Expanded(child: Container(
                alignment: FractionalOffset(0.5, 0.01),
                child: ElevatedButton(
                    child: ExampleButton(text: 'Зарегистрироваться'),
                    onPressed: (){
                      Navigator.push(context, MaterialPageRoute(builder: (context) => const Registration())
                      );
                    }
                )
            )
            )
          ],
        ),
      ),
      appBar: AppBar(title: Text('Регистрация'),),
    );
  }
}

class Login extends StatelessWidget {
  const Login({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {

    return Scaffold(
      body: ListView.builder(
          padding: EdgeInsets.all(20),
          itemBuilder: (BuildContext context, int index) {

            return DescriptionFlovers(name: DescriptionFlovers[index].name, : productlist[index].pathphoto, desciption_product: productlist[index].description, price_prpduct: productlist[index].price, id_product: productlist[index].id);
          }
      ),
      appBar: AppBar(title: Text('Flower'),),
    );

  }
}

class Registration extends StatelessWidget {
  const Registration({Key? key}) : super(key: key);
  @override
  Widget build(BuildContext context) {
    return  Scaffold(
      appBar: AppBar(title: Text('Авторизация'),
      ),
      body: Container(
        alignment: Alignment.center,
        child: Column(
          children: <Widget>[
            Expanded(
                flex: 1,
                child: Container(
                  padding: EdgeInsets.only( left: 10, right: 10),
                  alignment: FractionalOffset(0.5, 2),
                  margin: EdgeInsets.only(bottom: 8),
                  child: TextField(style: TextStyle(fontSize: 20, color: Colors.black
                  ),
                    decoration: InputDecoration(hintStyle: TextStyle(fontWeight: FontWeight.bold, fontSize: 20, color: Colors.black),
                        prefixIcon: Icon(Icons.mail),
                        hintText: 'Электронная почта',
                        border: OutlineInputBorder(
                            borderSide: BorderSide(color: Colors.black, width: 3)
                        )
                    ),
                  ),
                )

            ),
            Expanded(
                flex: 1,
                child: Container(
                  padding: EdgeInsets.only(left: 10, right: 10),
                  alignment: FractionalOffset(0.5, 1),
                  margin: EdgeInsets.only(bottom: 8),
                  child: TextField(style: TextStyle(fontSize: 20, color: Colors.black
                  ),
                    decoration: InputDecoration(hintStyle: TextStyle(fontWeight: FontWeight.bold, fontSize: 20, color: Colors.black),
                        prefixIcon: Icon(Icons.https),
                        hintText: 'Пароль',
                        border: OutlineInputBorder(
                            borderSide: BorderSide(color: Colors.black, width: 3)
                        )
                    ),
                  ),
                )
            ),
            Expanded(
                flex: 1,
                child: Container(
                  padding: EdgeInsets.only(left: 10,right: 10),
                  alignment: FractionalOffset(0.5, 0.001),
                  margin: EdgeInsets.only(bottom: 8),
                  child: TextField(style: TextStyle(fontSize: 20, color: Colors.black
                  ),
                    decoration: InputDecoration(hintStyle: TextStyle(fontWeight: FontWeight.bold, fontSize: 20, color: Colors.black),
                        prefixIcon: Icon(Icons.https),
                        hintText: 'Повторите пароль',
                        border: OutlineInputBorder(
                            borderSide: BorderSide(color: Colors.black, width: 3)
                        )
                    ),
                  ),
                )
            ),
            Expanded(

                child: Container(
                    alignment: FractionalOffset(0.5, 0.01),
                    child: ElevatedButton(
                        child: ExampleButton(text: 'Зарегистрироваться'),
                        onPressed: (){
                          Navigator.push(context, MaterialPageRoute(builder: (context) => const HomePage())
                          );
                        }
                    )
                )
            )

          ],
        ),
      ),


    );
  }
}

class CartProduct extends StatelessWidget {
  const CartProduct({Key? key, required this.name_product1, required this.photo_path1, required this.desciption_product1, required this.id_product1, required this.price_prpduct1}) : super(key: key);
  final String name_product1;
  final String photo_path1;
  final String desciption_product1;
  final double price_prpduct1;
  final int id_product1;
  @override
  Widget build(BuildContext context) {
    return Scaffold(
        appBar: AppBar(
          title: Text(name_product1,
            style: TextStyle(fontSize: 20, color: Colors.red[900]),
          ),
        ),
        body: ListView(
          padding: const EdgeInsets.all(8) ,
          children: <Widget>[
            Container(
              child: Image.network(photo_path1),
            ),
            Container(
              margin: EdgeInsets.only(bottom: 8),
              child: Text('Артикул: ${id_product1.toString()}', style: TextStyle(fontSize: 30, fontWeight: FontWeight.bold),),
            ),
            Container(
              margin: EdgeInsets.only(bottom: 8),
              child: Text('Полное название продукта: ${name_product1}', style: TextStyle(fontSize: 30, fontWeight: FontWeight.bold),),
            ),
            Container(
              margin: EdgeInsets.only(bottom: 8),
              child: Text('Описание товара: ${desciption_product1}', style: TextStyle(fontSize: 30, fontWeight: FontWeight.bold),),
            ),
            Container(
              margin: EdgeInsets.only(bottom: 8),
              child: Text('Цена товара: ${price_prpduct1.toString()}', style: TextStyle(fontSize: 30, fontWeight: FontWeight.bold),),
            ),
          ],

        )
    );
  }
}


class DescriptionFlovers extends StatefulWidget {
  final String name;
  final String price;
  final String description;
  final String specifications;
  //final String video;
  final List<String> fimage;

  const DescriptionFlovers({
    Key? key,
    required this.name,
    required this.price,
    required this.description,
    required this.specifications,
    //required this.video,
    required this.fimage,
  }) : super(key: key);

  @override
  _DescriptionFloversState createState() => _DescriptionFloversState();
}

class _DescriptionFloversState extends State<DescriptionFlovers> {
  int activeIndex = 0;


  @override
  Widget build(BuildContext context) {
    //YoutubePlayerController controller = YoutubePlayerController(
    //initialVideoId: widget.video,
    //flags: const YoutubePlayerFlags(
    //autoPlay: false,
    //));
    return Scaffold(
      backgroundColor: const Color.fromARGB(255, 240, 240, 240
      ),
      appBar: AppBar(
        title: Text(widget.name),
        centerTitle: true,
      ),
      body: SingleChildScrollView(
        child: Column(
          crossAxisAlignment: CrossAxisAlignment.center,
          children: [
            const SizedBox(height: 30),
            CarouselSlider.builder(
              options: CarouselOptions(
                height: 300,
                autoPlay: true,

                onPageChanged: (index, reason) {
                  setState(() {
                    activeIndex = index;
                  });
                },
              ),
              itemCount: widget.fimage.length,
              itemBuilder: (context, index, realIndex) {
                return Container(
                  margin: const EdgeInsets.symmetric(horizontal: 2),
                  child: Image.network(widget.fimage[index]),
                );
              },
            ),
            const SizedBox(height: 30),
            AnimatedSmoothIndicator(
              activeIndex: activeIndex,

              count: widget.fimage.length,
            ),
            const SizedBox(height: 30),
            Center(
              child: Container(
                decoration:BoxDecoration(
                  borderRadius: BorderRadius.circular(25
                  ),
                  color: const Color.fromARGB(255, 230, 230, 230,
                  ),
                ),
                padding: const EdgeInsets.only(left: 20, right: 20
                ),
                height: 170,
                width: 400,
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.center,
                  children: [
                    Text(
                      widget.name, //Название товара
                      style: const TextStyle(
                          fontSize: 20,
                          fontWeight: FontWeight.w600,
                          color: Colors.black
                      ),
                    ),
                    const SizedBox(height: 15
                    ),
                    Text(
                      widget.price, //Цена товара
                      style: const TextStyle(
                          fontSize: 19,
                          fontWeight: FontWeight.w400,
                          color: Colors.black
                      ),
                    ),
                    const SizedBox(height: 5),
                  ],
                ),
              ),
            ),
            const SizedBox(height: 25
            ),
            Center(
              child: Container(
                decoration:BoxDecoration(
                  borderRadius: BorderRadius.circular(25
                  ),
                  color: const Color.fromARGB(255, 230, 230, 230),
                ),
                padding: const EdgeInsets.only(
                    left: 20,
                    right: 20
                ),
                height: 200, //высота
                width: 400, //ширина
                child: SingleChildScrollView(
                  child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    children: [
                      const SizedBox(height: 17),
                      const Text(
                        "Описание:",
                        style:  TextStyle(fontSize: 23,
                          fontStyle: FontStyle.italic,
                          fontWeight: FontWeight.w500,
                          color:Colors.black,
                        ),
                      ),
                      const SizedBox(height: 20
                      ),
                      Text(
                        widget.description, //Описание Товара
                        style: const TextStyle(fontSize: 20,
                            color: Colors.black
                        ),
                      ),
                    ],
                  ),
                ),
              ),
            ),
            const SizedBox(height: 25
            ),
            Center(
              child: Container(
                decoration: BoxDecoration(
                  borderRadius: BorderRadius.circular(25
                  ),
                  color: const Color.fromARGB(255, 230, 230, 230
                  ),
                ),
                padding: const EdgeInsets.only(
                    left: 20,
                    right: 20
                ),
                height: 670, //высота
                width: 400, //ширина
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.center,
                  children: [
                    const Text(
                      "Состав:",
                      style: TextStyle(fontSize: 23,
                        fontStyle: FontStyle.italic,
                        fontWeight: FontWeight.w500,
                        color:Colors.black,
                      ),
                    ),
                    const SizedBox(height: 20
                    ),
                    Text(
                      widget.specifications, //Характеристики товара
                      style: const TextStyle(fontSize: 20,
                          color: Colors.black
                      ),
                    ),
                  ],
                ),
              ),
            ),
            const SizedBox(height: 25
            ),
            const SizedBox(height: 25
            ),
          ],
        ),
      ),
    );
  }
}
