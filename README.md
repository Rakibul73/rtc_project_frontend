> The main codebase is private as it is currently in production at PSTU. You can view the website https://csit.pstu.ac.bd:7020
<div align="center">
  <h1>🌟 PSTU RTC Project Management (Frontend)🌟 </h1>


> An innovative initiative to improve research and training at any university.

[![](https://skillicons.dev/icons?i=flutter,dart,vscode,py,mysql)]()
</div>
<hr/>
With the goal of improving research and training initiatives at any institution, the "PSTU RTC Project Management" is a ground-breaking project created with the Flutter framework (frontend), Python (Flask backend), and MySQL database. Administrators have full authority over the system, including monitoring, modifying, and managing research projects, while researchers may submit, manage, and update their project ideas. The Reviewer Panel, which enables designated reviewers to assess and offer input on research project proposals, is one of this system's key components.
<hr>

##### This Website uses this Python (Flask) backend [PSTU RTC Project Management `Backend`](https://github.com/Rakibul73/rtc_project_backend) 

##### This is Web build repo [PSTU RTC Project Management `Frontend` Build Repo](https://github.com/Rakibul73/rtc_project_frontend_build),  where we auto push from this main repo.  
<hr>

## Features

- [x] Streamlined administrative processes
    - [x] Admin can view , edit , delete and verify pending registered users
    - [x] Admin can view User Overview info
    - [x] Admin can search , view , edit and delete all users
    - [x] Admin can view Projects Overview info
    - [x] Admin can search , view , edit and delete all Projects
    - [x] Admin can approve / reject users project proposals based on review feedback
    - [x] Admin can set project review feedback
    - [x] Online notice board for project proposals
    - [ ] Project deletion request from normal user must be handled
    - [ ] Notification panel for admin must be handled
    - [x] Project funding functionality
    - [x] Project monitoring functionality



- [x] Role-based access control
- [x] User registration and secure login
- [x] User can give review to the project that he have assigned to
- [x] Author of the project can see his projects review if admin sends it to him
- [x] User profile section
- [x] Generate PDF report for every section
  - [x] Profile PDF
- [ ] Notification panel for user must be handled
- [x] Project funding functionality where user can manage their projects funds.
- [x] Project monitoring functionality where PI & reviewer can co-operate to handle the project completion.




## Installation

* You should have properly installed `Flutter version 3.16.0` | `Dart version 3.2.0` in your machine.
* Clone the repository to your local machine.
* Run this in terminal to install the required packages.
```bash
flutter packages get
```
* Run the app using
```bash
flutter run
```

<hr>

### if below error come from api calling

```bash
HandshakeException: Handshake error in client (OS Error: CERTIFICATE_VERIFY_FAILED: certificate has expired(handshake.cc:393))
```
Then use this video 
https://youtu.be/aaXMUM-_4lQ

or

Step 1:
In your main.dart file, add or import the following class:
```bash
class PostHttpOverrides extends HttpOverrides{
  @override
  HttpClient createHttpClient(context){
    return super.createHttpClient(context)
      ..badCertificateCallback = (X509Certificate cert, String host, int port)=> true;
  }
}
```
Step 2:
Add the following line after function definition In your main function:
```bash
HttpOverrides.global = new PostHttpOverrides();
```
Example :
```bash
import 'dart:io';
 
 
import 'package:flutter/material.dart';
import 'package:point/routes.dart';
import 'package:point/theme.dart';
 
import 'login/LoginScreen.dart';
 
class PostHttpOverrides extends HttpOverrides{
  @override
  HttpClient createHttpClient( context){
    return super.createHttpClient(context)
      ..badCertificateCallback = (X509Certificate cert, String host, int port)=> true;
  }
}
 
void main() {
  HttpOverrides.global = new PostHttpOverrides();
  runApp(MyApp());
}
 
class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
 
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'Flutter Demo',
      theme: theme(),
      // home: SplashScreen(),
      // We use routeName so that we dont need to remember the name
      initialRoute: LoginScreen.routeName,
      routes: routes,
    );
  }
}
```

<hr>

## Acknowledgements

- [Awesome Dialog](https://pub.dev/packages/awesome_dialog) library for making awesome dialog ui
- [Go Router](https://pub.dev/packages/go_router) library for making page route navigation
- [Flutter Form Builder](https://pub.dev/packages/flutter_form_builder) library for data collection forms
- [SharedPreferences](https://pub.dev/packages/shared_preferences) library for persistent storage
- [Flutter Secure Storage](https://pub.dev/packages/flutter_secure_storage) library to store data in secure storage

<br>
<br>
🚀 Explore the future of research automation! 🌐
