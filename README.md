# social_media_application
Social media application documentation
Introduction
Welcome to the comprehensive documentation of DhiWise generated Flutter application code. This guide is designed not just to help you navigate through the generated code but to fully harness the capabilities of our cutting-edge platform. By choosing our tool, you've equipped yourself with a sophisticated framework that significantly reduces the time and effort required in traditional app development.
Key Advantages:
•	Reusable Components: Dive into a library of pre-built, customizable UI components that accelerate the development process and ensure consistency across your app. Our tool's ability to reuse components reduces redundancy and enhances maintainability.
•	Efficient Asset Management: Spend minimal time setting up initial assets and even less when adding new ones. Our system is optimized to handle asset management swiftly, allowing you to focus on more critical aspects of your development.
•	Automated Content Transfer: With our tool, content from Figma design files is transferred seamlessly to your application, eliminating the common typos and errors associated with manual coding. This precision saves substantial time, especially noted across multiple screens.
•	Responsive UI Across Devices: Your application will look great on any device, thanks to the automatic responsive design adjustments made by our platform for all types of mobile devices.
•	Integrated Theming: Switch between light and dark themes with ease. Our platform provides a pre-configured theming setup that allows you to adapt the UI's look and feel according to your preferences without diving deep into the code.
•	Streamlined Route Definitions: Our tool simplifies the complexity of route management in Flutter applications, enabling you to define and modify navigational flows effortlessly.
•	Personalized Configuration: From selecting state management libraries to setting up personalized configurations, our platform molds itself to fit your technical and creative needs.
Experience the Future of App Development:
As you proceed through this guide, you'll discover how each feature can be tailored to suit your project requirements, enabling you to deliver exceptional user experiences with less coding and quicker turnarounds. This documentation is your first step toward mastering these tools, pushing the boundaries of what you can achieve with Flutter development.
Dive into the sections below to transform your app development process and make your ideas come to life more efficiently than ever before.
Table of Contents
Getting Started
Running the App
State Management
Project Structure Overview
Lib Directory Structure
Reusable Components
Modular Screen Design
Special Cases Implementation
Navigation Flow and Screen Management
App Navigation Screen
Utilities
Libraries
Theming and Appearance
Localization and Internationalization
API Implementation
Getting Started
Formatting the code
Run the following command in your terminal to format source code of your entire application dart format .
Installation and Setup Instructions
Flutter SDK: Installation Guide
•	Ensure you have the Flutter SDK installed. You can download it from Flutter website.
•	Recommended Flutter SDK version: 3.22.0 or greater
Dart SDK: Installation Guide
•	Ensure you have the Dart SDK installed. Dart comes bundled with the Flutter SDK, so if you have Flutter installed, you should have Dart too.
•	Recommended Dart SDK version: 3.4.0 or greater
Android and iOS SDK details
•	Ensure you have the necessary Android and iOS SDKs installed for cross-platform development.
•	Android SDK version: Android SDK 19 to latest
•	iOS SDK version: iOS 12 to latest
Running the App
1.	Fetch necessary dependencies using flutter pub get.
2.	Start the application with flutter run.
State Management
In this Flutter application, we employed the BLoC (Business Logic Component) state management library to efficiently manage the state of the application, enabling seamless data flow and separation of concerns.
Project Structure Overview
 
Top-Level Directories
android
Contains Android-specific application settings, resources, and native code.
ios
Houses iOS-specific assets, configurations, and native code.
lib
Main directory for all the Dart code of the application.
assets
Includes all static files like images and fonts used within the application.
test
Contains all test files for unit and widget tests.
Lib Directory Structure
core
Core functionalities and utilities that are fundamental to the application's operations.
•	constants/role.dart: Defines roles and permissions throughout the app.
•	network/network_info.dart: The NetworkInfo class in our code checks for internet connectivity by using the connectivity_plus flutter package. It employs a function called isConnected() to verify internet connectivity. The class also uses connectivityResult and onConnectivityChanged to verify the internet's state and react to connectivity changes. Additionally, it has methods to handle various types of failures and exceptions, like NoInternetException.
•	utils:
•	date_time_utils.dart (More Info) :
Utilities for date and time operations, it contains format constants and date & time format functions which are used in the generated code.
•	image_constant.dart (More Info) :
Constants for image paths, it contains the absolute path of the images in the string literal.
•	navigator_service.dart (More Info) :
Abstracts navigation to decouple it from UI logic, it contains the navigation functions like pushNamed, pushNamedAndRemoveUntil and popAndPushNamed which are useful for navigating through application screens.
•	pref_utils.dart (More Info) :
Utilities for handling shared preferences, along with that data storing methods are generated over here.
•	progress_dialog_utils.dart (More Info) :
Utility for showing and hiding progress dialogs, showProgressDialog used for showing and hideProgressDialog used for hiding progress dialog.
•	size_utils.dart (More Info) :
Provides consistent sizing across different screen sizes, helps to achieve responsiveness in various devices.
•	validation_functions.dart (More Info) :
Function which are reusable for validating the inputs provided by the user and setting restriction on inappropriate/wrong inputs.
data
Handles all data-related operations, particularly managing API interactions and local data handling.
•	apiClient (More Info) :
•	api_client.dart: Configures the API client for network requests functions with the header and request body params and handles callbacks of api calls.
•	network_interceptor.dart: Intercepts all network requests for logging and modifications, for tracking user's activities and analyze.
•	models:
•	loginDeviceAuth/post_login_device_auth_req.dart: Request model for device authentication.
•	loginDeviceAuth/post_login_device_auth_resp.dart: Response model for device authentication.
•	repository/repository.dart (More Info): Abstracts data operations from the network and local databases.
domain
Contains business logic that is crucial for the application but independent of the UI.
•	facebookauth:
•	facebook_auth_helper.dart: Manages Facebook authentication processes and return the facebook user details.
•	facebook_user.dart: Data model for Facebook user information which contains user details like name, username etc.
•	googleauth:
•	google_auth_helper.dart: Handles Google authentication processes and returns the authorized user information.
localization (More Info)
Support for internationalization and localization.
•	en_us/en_us_translations.dart: English translations for all the text used through the all screens in widgets.
•	app_localization.dart: Setup and configuration for localization, which handles the language selection and decides the translation manner.
presentation
All UI-related dart code is contained here, including screens and reusable widgets along with its list items.
•	dashboard_page (each screen has its own folder):
•	bloc: Contains BLoC files for state management.
•	dashboard_bloc.dart: Manages the state of the dashboard page.
•	dashboard_event.dart: Defines events that can trigger state changes.
•	dashboard_state.dart: Represents the state of the dashboard page.
•	models: Models specific to the dashboard page.
•	widgets: UI components for the dashboard page.
routes
•	app_routes.dart: Central definition of route names and configurations with their actual code file's class name.
•	navigation_args.dart: Definitions for arguments passed during navigations throughout the application flow.
theme (More Info)
•	bloc: [BLoC architecture for theme management]
•	theme_bloc.dart: Manages the theme state of the application.
•	theme_event.dart: Defines events that can trigger theme changes.
•	theme_state.dart: Represents the state of the theme.
•	custom_button_style.dart: Contains custom button styles for the application styling.
•	custom_text_style.dart: Contains custom text styles for the application styling.
•	theme_helper.dart: Helper functions for theme data.
•	app_decoration.dart: Manages common decorative styles such as borders, shapes, and shadows.
widgets (More Info)
•	base_button.dart (More Info): Reusable button widget with customizable styles.
•	custom_bottom_bar.dart (More Info): Provides unique icons and actions for navigation.
•	custom_elevated_button.dart (More Info): Button with elevation that lifts on press.
•	custom_outlined_button.dart (More Info): Outlined button for secondary actions.
•	custom_icon_button.dart (More Info): Button with an icon for actions like back, close, etc.
•	custom_dropdown.dart (More Info): Custom dropdown menu widget for selection from a list of items.
•	custom_image_view.dart (More Info): Wrapper around the Image widget for consistent image display.
•	custom_search_view.dart (More Info): Search input field customized for the application.
•	custom_text_form_field.dart (More Info): Custom TextFormField for text input.
Configuration and Miscellaneous Files
•	.gitignore: Specifies the files and directories which are ignored by Git.
•	pubspec.yaml: Manages the dependencies and project configuration.
•	README.md: Provides an introduction and setup instructions for the project.
Reusable Components
The Flutter app uses several reusable UI components for consistent styling and reduced code redundancy. Below are the reusable components along with their file names and examples of how they are used within the app.
base_button.dart
A foundational button component that provides a customizable button base for the app. It can be extended to create more specific button types with consistent padding, typography, and colors.
custom_bottom_bar.dart
This component creates a customized bottom navigation bar, allowing for easy navigation and consistent styling across different screens within the app.
CustomBottomBar(
  onChanged: (BottomBarEnum type) {
    Navigator.pushNamed(
      navigatorKey.currentContext!,
      getCurrentRoute(type)
    );
  },
);
custom_elevated_button.dart
A button with elevation that lifts (Material shadow effect) on press. It is typically used for primary actions in forms and dialogues throughout the app.
CustomElevatedButton(
  text: "lbl_sign_in".tr, // 'tr' is typically used for translation
  onPressed: () {
    callSignIn(context);
  },
);
custom_outlined_button.dart
This component is an outlined button, usually used for secondary actions. It features a border and is often used in contrast to the CustomElevatedButton.
CustomOutlinedButton(
          text: "lbl_login_with_google".tr,
          leftIcon: Container(
            margin: EdgeInsets.only(right: 30.h),
            child: CustomImageView(
              imagePath: ImageConstant.imgGoogleIcon,
              height: 24.adaptSize,
              width: 24.adaptSize,
            ),
          ),
          onPressed: () {
            onTapLoginWithGoogle(context);
          },
        )
custom_icon_button.dart
A button with an icon that can be used for actions like back, close, info, and more, ensuring icon buttons are uniformly styled across the app.
CustomIconButton(
              height: 70.adaptSize,
              width: 70.adaptSize,
              padding: EdgeInsets.all(23.h),
              child: CustomImageView(
                imagePath: arrowrightItemModelObj?.arrowRight,
              ),
            )
custom_drop_down.dart
A dropdown menu widget customized for the app's design language, allowing for selection from a list of items with custom dropdown menu styles.
CustomDropDown(
              width: 103.h,
              icon: Container(
                margin: EdgeInsets.only(left: 8.h),
                child: CustomImageView(
                  imagePath: ImageConstant.imgDownIcon,
                  height: 24.adaptSize,
                  width: 24.adaptSize,
                ),
              ),
              hintText: "lbl_category".tr,
              items: searchResultModelObj?.dropdownItemList ?? [],
            );
custom_image_view.dart
A wrapper around the Image widget that provides a consistent way of displaying images with common settings like fit, alignment, and error handling.
CustomIconButton(
            height: 72.adaptSize,
            width: 72.adaptSize,
            padding: EdgeInsets.all(24.h),
            decoration: IconButtonStyleHelper.outlinePrimary,
            child: CustomImageView(
              imagePath: ImageConstant.imgCheckmark,
            ),
          )
custom_search_view.dart
A search input field customized for the application, providing a consistent UI for search functionality throughout the app.
CustomSearchView(
        width: 263.h,
        controller: controller,
        hintText: "lbl_product_name".tr,
      )
custom_text_form_field.dart
A customizable TextFormField used for text input throughout the app, which includes validation, prefixes, and consistent styling.
CustomTextFormField(
  controller: passwordController,
  hintText: "lbl_password".tr,
  textInputAction: TextInputAction.done,
  textInputType: TextInputType.visiblePassword,
  prefix: Container(
    margin: EdgeInsets.fromLTRB(16.h, 12.v, 10.h, 12.v),
    child: CustomImageView(
      imagePath: ImageConstant.imgLocation,
      height: 24.adaptSize,
      width: 24.adaptSize,
    ),
  ),
  prefixConstraints: BoxConstraints(maxHeight: 48.v),
  validator: (value) {
    if (value == null || !isValidPassword(value, isRequired: true)) {
      return "err_msg_please_enter_valid_password".tr;
    }
    return null;
  },
  obscureText: true,
  contentPadding: EdgeInsets.only(
    top: 15.v,
    right: 30.h,
    bottom: 15.v,
  ),
);
Modular Screen Design
Modular design in Flutter screens enhances the maintainability and scalability of the application by breaking down complex interfaces into manageable components. This section discusses how screens are organized into sections and reusable components.
Screen Breakdown Structure
1. Sections
Screens are typically divided into logical sections where specific UI elements are encapsulated within distinct functions. This separation enhances readability and makes the code easier to manage.
Approach
•	Function per Section: Each major UI section is created in a separate function that returns a widget. This method is used for components like appbar, content blocks, etc.
•	Clear Naming Conventions: Functions are named clearly to reflect the UI component they represent, such as buildAppBar(), buildLoginForm().
Widget buildHeader() {
  return Text(
    'Welcome!',
    style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold),
  );
}

Widget buildLoginForm(BuildContext context) {
  return Column(
    children: [
      TextFormField(labelText: 'lbl_username'.tr),
      TextFormField(labelText: 'lbl_password'.tr, obscureText: true),
      ElevatedButton(
        onPressed: () => _login(context),
        child: Text('lbl_login'.tr),
      ),
    ],
  );
}
2. Reusable UI of the Screen
Reusable components are defined as separate functions or widgets, particularly for elements repeated across different parts of the screen. This approach fosters reusability and consistency throughout the application.
Approach
Reusable Widgets: Functions are created for frequently used widgets like buttons, input fields which can be customized through parameters. Parameterization: These components accept parameters to customize aspects like content, styling, and behavior, making them adaptable to various contexts.
Widget buildCustomButton(String label, VoidCallback onPressed) {
  return ElevatedButton(
    onPressed: onPressed,
    child: Text(label),
  );
}

Widget buildTitle(String title, String subtitle) {
  return Text(
          title,
          style: TextStyle(
            fontWeight: FontWeight.bold,
            fontSize: 18.0,
          ),
        );
}
Special Cases Implementation
BottomNavigationBar
In the Flutter project, BottomNavigationBar is treated as a special UI component due to its common use across multiple screens and its significance in navigation.
Implementation Strategy
Container and Page Files
When a BottomNavigationBar is included in the design, the system automatically segregates its implementation into two main file types: containers and pages.
Container
•	Filename Convention: The file that includes the BottomNavigationBar itself is typically named with the postfix container. This file acts as a wrapper or a scaffold that holds the navigation bar along with the screen content placeholders.
•	Functionality: The container manages the state of the selected tab and swaps the displayed page content accordingly without reloading the navigation bar itself. This setup enhances the user experience by providing smooth transitions and maintaining the state persistently across navigations.
// Example: dashboard_container.dart
BottomNavigationBar bottomNavBar() {
  return BottomNavigationBar(
    items: const <BottomNavigationBarItem>[
      BottomNavigationBarItem(
        icon: Icon(Icons.home),
        label: 'lbl_home'.tr,
      ),
      BottomNavigationBarItem(
        icon: Icon(Icons.business),
        label: 'lbl_business'.tr,
      ),
      BottomNavigationBarItem(
        icon: Icon(Icons.school),
        label: 'lbl_school'.tr,
      ),
    ],
    currentIndex: _selectedIndex,
    selectedItemColor: Colors.amber[800],
    onTap: _onItemTapped,
  );
}

void _onItemTapped(int index) {
  setState(() {
    _selectedIndex = index;
  });
}
Page
•	Filename Convention: Each screen that is accessible via the BottomNavigationBar items has a filename with the postfix page. These files contain the specific UI and logic of each screen that can be navigated to from the bottom bar.
•	Functionality: Pages are the content areas loaded by the container based on the BottomNavigationBar Item selection. Each page is designed to function independently, encapsulating its own UI and state where necessary.
// Example: dashboard_page.dart
class DashboardPage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('lbl_dashboard'.tr),
      ),
      body: Center(
        child: Text('lbl_welcome_to_dashboard'.tr),
      ),
    );
  }
}
TabBar
The TabBar widget in Flutter is a material design widget used for displaying a horizontal row of tabs. It is typically used in conjunction with a TabBarView widget for displaying the content associated with each tab.
Implementation Strategy
Container and Page Files
when a TabBar is included in the design, it's common to organize the implementation into container and page files, although the structure might slightly differ due to the nature of tabs being more content-driven.
Container
•	Filename Convention: The file that includes the TabBar itself might be named with a convention that reflects its purpose, often not needing a specific postfix like container. However, it acts as a container for the tabs and their content.
•	Functionality: The container file typically includes the TabBar and a TabBarView. It manages the state of the selected tab and displays the corresponding page content.
// Example: notification_container_screen.dart
Widget build(BuildContext context) {
  return SafeArea(
    child: Scaffold(
      body: SizedBox(
        width: double.maxFinite,
        child: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            TabBar(
              controller: controller.tabviewController,
              labelPadding: EdgeInsets.zero,
              labelColor:
                  theme.colorScheme.onPrimaryContainer.withOpacity(1),
              labelStyle: TextStyle(
                fontSize: 12.fSize,
                fontFamily: 'Plus Jakarta Sans',
                fontWeight: FontWeight.w600,
              ),
              unselectedLabelColor: appTheme.gray600,
              unselectedLabelStyle: TextStyle(
                fontSize: 12.fSize,
                fontFamily: 'Plus Jakarta Sans',
                fontWeight: FontWeight.w600,
              ),
              indicatorSize: TabBarIndicatorSize.tab,
              indicator: BoxDecoration(
                color: theme.colorScheme.primary,
                borderRadius: BorderRadius.circular(
                  12.h,
                ),
              ),
              tabs: [
                Tab(
                  child: Text(
                    "lbl_general".tr,
                  ),
                ),
                Tab(
                  child: Text(
                    "lbl_my_proposals".tr,
                  ),
                )
              ],
            ),
            SizedBox(
              height: 644.v,
              child: TabBarView(
                controller: controller.tabviewController,
                children: [
                  NotificationsMyProposalsPage(),
                  NotificationsMyProposalsPage()
                ],
              ),
            )
          ],
        ),
      ),
    ),
  );
}
Page
•	Filename Convention: Each content area displayed by selecting a tab is typically a separate widget, which might follow any naming convention but often reflects the content it displays, such as home_page.dart.
•	Functionality: Pages are the widgets displayed by the TabBarView based on the current tab selection. Each page is designed to function independently, encapsulating its own UI and state.
// Example: notifications_proposals_page.dart
class NotificationsMyProposalsPage extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('lbl_notifications_my_proposals'.tr),
      ),
      body: Center(
        child: Text('msg_welcome_to_the_notification_page'.tr),
      ),
    );
  }
}
Navigation Flow and Screen Management
Effective navigation flow and screen management are crucial for maintaining a large Flutter application. This project employs a centralized NavigatorService to streamline navigation actions such as moving between screens or popping to previous screens. This section explains how the navigation is implemented and managed.
Navigation Service
A NavigatorService is used to abstract and centralize all navigation actions. This service is especially useful in scenarios where navigation needs to be triggered outside of the widget tree or in business logic.
File: navigator_service.dart
The NavigatorService class encapsulates all navigation functionality, making it easy to perform common navigation tasks from any part of the app without requiring context.
class NavigatorService {
  final GlobalKey<NavigatorState> navigatorKey = GlobalKey<NavigatorState>();

  Future<void> pushNamed(String routeName) async {
    return navigatorKey.currentState?.pushNamed(routeName);
  }

  Future<void> popAndPushNamed(String routeName) async {
    return navigatorKey.currentState?.popAndPushNamed(routeName);
  }

  void pop() {
    navigatorKey.currentState?.pop();
  }
}
Usage:
The following example demonstrates how to use the NavigatorService to navigate between screens. In this case, we are navigating to the DashboardContainerScreen by popping the current route off the stack and pushing a new route. This method is typically used in scenarios like logging in, where you want to clear the previous screens from the navigation stack.
NavigatorService.popAndPushNamed(
  AppRoutes.dashboardContainerScreen,
);
App Navigation screen
The app_navigation_screen.dart serves as a central point for navigating to various screens within the app. This utility screen lists all available screens and allows you to open each one by clicking on the corresponding item. The purpose of providing this screen is to enable you to easily review the UI of the complete application, offering a quick way to verify the accuracy of the UI generated by DhiWise.
File Structure:
class AppNavigationScreen extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return SafeArea(
      child: Scaffold(
        backgroundColor: appTheme.whiteA700,
      //other widgets  
      ...
      _buildScreenTitle(
        context,
        screenTitle: "lbl_onboarding_one".tr,
        onTapScreenTitle: () => onTapScreenTitle(
             AppRoutes.onboardingOneScreen),
       ),
      ...
      //other widgets
      ),
    );
  }

  Widget _buildScreenTitle(
    BuildContext context, {
    required String screenTitle,
    Function? onTapScreenTitle,
  }) {
    return GestureDetector(
      onTap: () {
        onTapScreenTitle?.call();
      },
      child: Container(
        decoration: AppDecoration.fillWhiteA,
        child: Column(
          children: [
            Text(
              screenTitle,
              textAlign: TextAlign.center,
              style: TextStyle(
                color: appTheme.black900,
                fontSize: 20.fSize,
                fontFamily: 'Roboto',
                fontWeight: FontWeight.w400,
              ),
            ),
            SizedBox(height: 10.v),
            Divider(
              height: 1.v,
              thickness: 1.v,
              color: appTheme.blueGray40001,
            )
          ],
        ),
      ),
    );
  }

  void onTapScreenTitle(String routeName) {
    NavigatorService.pushNamed(routeName);
  }
}
Usage:
Set the AppNavigationScreen as the initial route in the MaterialApp widget of your main.dart file to display it as the starting point of your app.
  initialRoute: AppRoutes.appNavigationScreen,
Utility
DateTime Formatting Utility
•	This file, date_time_utils.dart, provides methods for formatting date-time strings according to a specified pattern and locale.
Usage:
•	Format DateTime:
String formattedDateTime = DateTime.now().format();
•	Customize Format:
String customFormattedDateTime = DateTime.now().format(pattern: 'yyyy-MM-dd HH:mm:ss');
•	Format DateTime with Locale:
String formattedDateTimeWithLocale = DateTime.now().format(locale: 'en_US');
Use this utility to ensure consistent and localized date-time formatting throughout your app.
App Image Constants
•	This file, image_constant.dart, centralizes all app image paths for easy access and maintenance.
Usage:
•	Access Image Path:
String splashScreenImage = ImageConstant.imgLogo;
•	Use in Widgets:
Image.asset(ImageConstant.imgClose);
With this setup, managing and accessing app images becomes straightforward and organized.
Navigator Service Utility
•	This file is a centralized navigation handler for Flutter apps.
•	It simplifies navigation management by providing methods to push, pop, and replace routes across the app.
Usage:
•	Push Named Route:
NavigatorService.pushNamed('/routeName', arguments: yourArguments);
•	Push Named Route and Remove Until:
NavigatorService.pushNamedAndRemoveUntil(
'/routeName',
routePredicate: (route) => route.isFirst,
arguments: yourArguments,
);
•	Pop and Push Named Route:
NavigatorService.popAndPushNamed('/routeName', arguments: yourArguments);
With this service, managing navigation flows becomes more efficient and structured.
Local Data Storage Utility
•	This file, pref_utils.dart, serves as a convenient handler for storing and retrieving local data in Flutter apps using SharedPreferences.
Usage:
•	Initialize Preferences:
await PrefUtils().init();
•	Clear All Stored Data:
PrefUtils().clearPreferencesData();
•	Set Theme Data:
PrefUtils().setThemeData('value');
•	Get Theme Data:
String themeData = PrefUtils().getThemeData();
•	To add another local data store method, simply define a new method similar to setThemeData and getThemeData, making sure to follow the same pattern for consistency and clarity.
Progress Dialog Utility
•	This file, progress_dialog_utils.dart, provides methods for showing and hiding a progress dialog during API calls in Flutter apps.
•	Integrate these methods into your API calling functions to enhance user experience by indicating loading states.
Usage:
•	Show Progress Dialog:
ProgressDialogUtils.showProgressDialog(context: context, isCancellable: true);
•	Hide Progress Dialog:
ProgressDialogUtils.hideProgressDialog();
Responsive UI Utility
This file, size_utils.dart, enables building responsive UIs in Flutter apps by adapting to different screen sizes and orientations.
...
extension ResponsiveExtension on num {
  double get _width => SizeUtils.width;
  double get _height => SizeUtils.height;
  double get h => ((this * _width) / FIGMA_DESIGN_WIDTH);
  double get v =>
      (this * _height) / (FIGMA_DESIGN_HEIGHT - FIGMA_DESIGN_STATUS_BAR);
  double get adaptSize {
    var height = v;
    var width = h;
    return height < width ? height.toDoubleValue() : width.toDoubleValue();
  }

  double get fSize => adaptSize;
}
...
Access Responsive Sizes:
•	Use .h for horizontal responsiveness.
•	Use .v for vertical responsiveness.
•	Use .adaptSize for adaptive sizing.
•	Use .fSize for font size adaptation.
Usage:
//usage of .v and .h
CustomImageView(
    imagePath: ImageConstant.imgFamily,
    height: 253.v,
    width: 380.h,
 ),

 //usage of fSize
 static get bodySmallGray => theme.textTheme.bodySmall!.copyWith(
        color: appTheme.gray,
        fontSize: 10.fSize,
      );

//usage of adaptive
CustomImageView(
     imagePath: ImageConstant.imgGlobe,
     height: 18.adaptSize,
     width: 18.adaptSize,
 ),
Validation
This file contains validation functions in validation_functions.dart that checks if the input string meets specific criteria and returns a boolean value indicating validity.
validation_functions.dart
bool isValidEmail(
  String? inputString, {
  bool isRequired = false,
}) {
  bool isInputStringValid = false;
  if (!isRequired && (inputString == null ? true : inputString.isEmpty)) {
    isInputStringValid = true;
  }
  if (inputString != null && inputString.isNotEmpty) {
    const pattern =
        r'^(([^<>()[]\.,;:s@"]+(.[^<>()[]\.,;:s@"]+)*)|(".+"))@(([[0-9]{1,3}.[0-9]{1,3}.[0-9]{1,3}.[0-9]{1,3}])|(([a-zA-Z-0-9]+.)+[a-zA-Z]{2,}))$';
    final regExp = RegExp(pattern);
    isInputStringValid = regExp.hasMatch(inputString);
  }
  return isInputStringValid;
}
Usage:
Widget _buildEmail() {
    return CustomTextFormField(
      controller: controller.emailController,
      textInputType: TextInputType.emailAddress,
      validator: (value) {
        if (value == null || (!isValidEmail(value, isRequired: true))) {
          return "err_msg_please_enter_valid_email".tr;
        }
        return null;
      },
    );
  }
Dialog
The onTapDialogTitle function is a reusable method for displaying a dialog box in generated code. It takes in the current BuildContext and a Widget to display as dialog content. This function is used to create consistent dialog boxes throughout the application.
void onTapDialogTitle(
    BuildContext context,
    Widget className,
    ) {
  showDialog(
    context: context,
    builder: (context) {
      return AlertDialog(
        contentPadding: EdgeInsets.zero,
        content: className,
        backgroundColor: Colors.transparent,
        insetPadding: EdgeInsets.zero,
      );
    },
  );
}
Usage:
_buildScreenTitle(
  context,
  screenTitle: "lbl_success_dialog".tr,
  onTapScreenTitle: () => onTapDialogTitle(
    context,
    SuccessDialog.builder(context),
  ),
)
BottomSheet
The onTapBottomSheetTitle function is a reusable method for displaying a modal bottom sheet in application. It takes the current BuildContext and a Widget to display as the bottom sheet content. This function ensures consistent bottom sheet behavior and appearance throughout the application.
void onTapBottomSheetTitle(
    BuildContext context,
    Widget className,
    ) {
  showModalBottomSheet(
    context: context,
    builder: (context) {
      return className;
    },
    isScrollControlled: true,
    backgroundColor: Colors.transparent,
  );
}
Usage:
_buildScreenTitle(
  context,
  screenTitle: "lbl_social_share_sheet".tr,
  onTapScreenTitle: () => onTapBottomSheetTitle(
    context,
    SocialShareBottomsheet.builder(context)
  ),
)
Libraries
This section provides an overview of the third-party libraries used in the Flutter project, including a brief description of each library and their versions.
flutter_bloc (More Info)
•	Description: A predictable state management library that helps implement the BLoC (Business Logic Component) pattern.
•	Version: ^8.1.3
connectivity_plus (More Info)
•	Description: Provides a cross-platform way to manage network connectivity changes.
•	Version: ^5.0.2
shared_preferences (More Info)
•	Description: Wraps NSUserDefaults (on iOS) and SharedPreferences (on Android), providing a persistent store for simple data.
•	Version: ^2.2.2
cached_network_image (More Info)
•	Description: Provides a widget that shows an image from the internet, caching it for performance.
•	Version: ^3.3.0
flutter_svg (More Info)
•	Description: Renders SVG files as Flutter widgets.
•	Version: ^2.0.9
equatable (More Info)
•	Description: Simplifies equality comparisons between objects, crucial for state management.
•	Version: ^2.0.5
google_sign_in (More Info)
•	Description: Provides Google authentication.
•	Version: ^6.2.1
flutter_login_facebook (More Info)
•	Description: Offers Facebook login capability.
•	Version: ^2.0.0
dio (More Info)
•	Description: A powerful HTTP client for Dart, which supports Interceptors, FormData, Request Cancellation, File Downloading, Timeout, etc.
•	Version: ^5.4.0
flutter_rating_bar (More Info)
•	Description: A customizable rating bar that allows users to rate with half ratings and gestures.
•	Version: ^4.0.1
carousel_slider (More Info)
•	Description: A carousel slider widget, supporting infinite scroll and custom child widgets.
•	Version: ^4.2.1
smooth_page_indicator (More Info)
•	Description: Displays custom animated page indicators with a smooth transition effect.
•	Version: ^1.1.0
another_stepper (More Info)
•	Description: A library that provides a stepper (progress tracker) widget with custom designs and flexible structures.
•	Version: ^1.2.2
fluttertoast (More Info)
•	Description: A plugin for displaying toast messages.
•	Version: ^8.2.4
pin_code_fields (More Info)
•	Description: provides customizable PIN code input fields for user authentication and verification purposes. It allows developers to easily integrate secure PIN code entry UIs into their applications.
•	Version: ^8.0.1
sms_autofill (More Info)
•	Description: The "sms_autofill" package provides functionality to automatically fill SMS verification codes in mobile applications, streamlining user authentication processes.
•	Version: ^2.3.0
Theming and Appearance
Theming and appearance management in Flutter applications involves defining a cohesive set of visual design choices that can be applied consistently across the app. This section explains how theming is implemented in the app, where to find the theme-related files, and how to add a new theme.
Implementation Overview
The app uses a combination of Flutter’s built-in ThemeData class along with custom classes for more granular control over styles like text and buttons. The implementation also utilizes the BLoC pattern to manage theme changes dynamically.
Theme Management Files
•	theme_helper.dart: Contains helper functions for theme data.
•	app_decoration.dart: Manages common decorative styles such as borders, shapes, and shadows.
•	custom_button_style.dart: Defines styles for different types of buttons.
•	custom_text_style.dart: Specifies custom text styles used throughout the app.
•	theme_bloc.dart, theme_event.dart, theme_state.dart: Files related to the BLoC pattern for handling theme data dynamically.
Theme Implementation
The application defines a base theme that can be easily extended or modified. The base theme typically includes default styles for various UI elements such as colors, font sizes, and padding.
Base Theme Setup
import 'package:flutter/material.dart';

ThemeData buildThemeData() {
  return ThemeData(
    primaryColor: Colors.blue,
    accentColor: Colors.blueAccent,
    scaffoldBackgroundColor: Colors.white,
    textTheme: TextTheme(
      headline1: TextStyle(fontSize: 24, fontWeight: FontWeight.bold),
      bodyText1: TextStyle(fontSize: 14),
    ),
  );
}
Using Custom Styles
Custom styles for buttons and text are defined in their respective files and can be easily included in the main theme data.
// In custom_button_style.dart
ButtonStyle raisedButtonStyle = ElevatedButton.styleFrom(
  onPrimary: Colors.white,
  primary: Colors.green,
  minimumSize: Size(88, 36),
  padding: EdgeInsets.symmetric(horizontal: 16),
  shape: const RoundedRectangleBorder(
    borderRadius: BorderRadius.all(Radius.circular(2)),
  ),
);
Applying in theme
ThemeData theme = buildThemeData().copyWith(
  elevatedButtonTheme: ElevatedButtonThemeData(style: raisedButtonStyle),
);
Managing Theme Dynamically
The app utilizes the BLoC architecture to enable dynamic theme switching, allowing users to switch themes on the file.
// In theme_bloc.dart
class ThemeBloc extends Bloc<ThemeEvent, ThemeState> {
  ThemeBloc(ThemeState initialState) : super(initialState) {
    on<ThemeChangeEvent>(_changeTheme);
  }

  _changeTheme(
    ThemeChangeEvent event,
    Emitter<ThemeState> emit,
  ) async {
    emit(state.copyWith(themeType: event.themeType));
  }
}
Adding Another Theme
Adding a new theme involves defining another set of ThemeData and possibly custom styles if needed.
Here’s how to add a "Dark" theme:
Define Dark Theme Data: Create a new ThemeData instance with dark-specific styles.
ThemeData buildDarkTheme() {
  return ThemeData(
    primaryColor: Colors.black,
    accentColor: Colors.red,
    scaffoldBackgroundColor: Colors.grey[850],
    textTheme: TextTheme(
      headline1: TextStyle(fontSize: 24, fontWeight: FontWeight.bold, color: Colors.white),
      bodyText1: TextStyle(fontSize: 14, color: Colors.white),
    ),
  );
}
Update Theme BLoC: Modify the ThemeBloc to handle a new event that switches to the dark theme.
class ThemeChangeToDark extends ThemeEvent {}

class ThemeBloc extends Bloc<ThemeEvent, ThemeState> {
  @override
  Stream<ThemeState> mapEventToState(ThemeEvent event) async* {
    if (event is ThemeChangeToDark) {
      yield ThemeState(themeData: buildDarkTheme());
    }
  }
}
Localization and Internationalization
Localization and Internationalization (often abbreviated as i18n and L10n) are critical for making your Flutter app accessible to a global audience by supporting multiple languages. This section describes how these practices are implemented in the app, where to find the related files, and how to extend support to more languages.
Implementation Overview
Localization in Flutter can be achieved through dedicated classes and libraries that handle language-specific resources and provide them dynamically based on the user's locale.
File Names
•	app_localization.dart: Contains the main logic for loading and retrieving localized strings.
•	en_us_translations.dart: Contains key-value pairs of strings for English translations.
Code Snippet of Implementation
The AppLocalization class is designed to fetch and deliver localized content within the app. It uses the flutter_localizations package to streamline localization processes.
app_localization.dart
import 'package:flutter/cupertino.dart';
import 'package:flutter/foundation.dart';
import '../core/app_export.dart';
import 'en_us/en_us_translations.dart';

extension LocalizationExtension on String {
  String get tr => AppLocalization.of().getString(this);
}

class AppLocalization {
  AppLocalization(this.locale);

  Locale locale;

  static final Map<String, Map<String, String>> _localizedValues = {'en': enUs};

  static AppLocalization of() {
    return Localizations.of<AppLocalization>(
        NavigatorService.navigatorKey.currentContext!, AppLocalization)!;
  }

  static List<String> languages() => _localizedValues.keys.toList();
  String getString(String text) =>
      _localizedValues[locale.languageCode]![text] ?? text;
}

class AppLocalizationDelegate extends LocalizationsDelegate<AppLocalization> {
  const AppLocalizationDelegate();

  @override
  bool isSupported(Locale locale) =>
      AppLocalization.languages().contains(locale.languageCode);
  //Returning a SynchronousFuture here because an async "load" operation
  //cause an async "load" operation
  @override
  Future<AppLocalization> load(Locale locale) {
    return SynchronousFuture<AppLocalization>(AppLocalization(locale));
  }

  @override
  bool shouldReload(AppLocalizationDelegate old) => false;
}

en_us_translations.dart
final Map<String, String> enUsTranslations = {
  'lbl_your_email': 'Your Email',
  'err_msg_please_enter_valid_email': 'Please enter a valid email address.'
};
Usage:
Localizing text within the app is straightforward with the .tr method provided by the easy_localization package, which automatically fetches the appropriate translation based on the user's locale settings.
TextField(
  hintText: "lbl_your_email".tr,
  validator: (value) {
    if (value == null || !isValidEmail(value, isRequired: true)) {
      return "err_msg_please_enter_valid_email".tr;
    }
    return null;
  },
);
Adding a New Language
To add a new language to the app, follow these steps:
•	Add Language File: Create a new Dart file under the translations directory, similar to en_us_translations.dart, but for the new language, say es_es_translations.dart.
•	Define Translations: Populate the new file with key-value pairs where keys match those in the existing language files and values are the translated strings.
•	Register Locale: Update AppLocalization.allLocales to include the new locale, such as Locale('es', 'ES').
•	Load Translations: Ensure the new translations are loaded correctly by modifying the load function to handle the new locale.
final Map<String, String> esEsTranslations = {
  'lbl_your_email': 'Tu correo electrónico',
  'err_msg_please_enter_valid_email': 'Por favor, introduce una dirección de correo válida.'
};
API Implementation
In this section, we discuss the conventions and standards applied during API integration (API calls), their categories, the API declaration, and the steps to perform API calls. This document also describes the use of BLoC (Business Logic Component) to implement different features effectively.
Introduction to API Calls with BLoC
API calls are used to communicate with a server to perform various tasks such as retrieving data or triggering changes in the server's data. In Flutter, API calls are often made in response to user interaction, and the results can update the application’s UI or store data for future reference.
To perform API calls in our project, we use BLoC with the 'dio' package to manage the data flow between our app and the server. We use BLoC for making API requests as it provides a clear separation between business logic and UI and efficiently manages the state of the application, which is crucial for complex apps.
Here is an overview of login API using BLoC:
1.	An event triggers the BLoC, and a function inside the BLoC makes an API call.
2.	The API returns a response in the form of data or errors, which is then transformed into a readable state.
3.	The BLoC outputs this state, which is picked up by widgets that listen to the BLoC’s state. These widgets rebuild, showing the new data on the screen.
File: SignUpScreen
In a Bloc-oriented structure, we use a Cubit/Bloc in the SignUpScreen to manage states. The UI reacts to state changes, and user interaction triggers events in the Cubit/Bloc, which consequently changes the current state.
onTapContinue(BuildContext context) {
  context.read<ScreenIntoSixBloc>().add(
    CreateLoginEvent(
      onCreateLoginEventSuccess: () {
        _onLoginDeviceAuthEventSuccess(context);
      },
      onCreateLoginEventError: () {
        _onLoginDeviceAuthEventError(context);
      },
    ),
  );
}
File: SignUpBloc
•	Calls the API with the provided event and emits the state.
•	Throws an error if an error occurs during the API call process.
FutureOr<void> _callLoginDeviceAuth(
    CreateLoginEvent event,
    Emitter<ScreenIntoSixState> emit,
    ) async {
  var postLoginDeviceAuthReq = PostLoginDeviceAuthReq(
    username: User.username,
    password: User.password,
  );
  await _repository.loginDeviceAuth(
    headers: {'Content-Type': 'application/json'},
    requestData: postLoginDeviceAuthReq.toJson(),
  ).then((value) async {
    event.onCreateLoginEventSuccess?.call();
  }).onError((error, stackTrace) {
    event.onCreateLoginEventError?.call();
  });
}
File: SignUpEvent
•	Event that is dispatched when the user calls the API.
class CreateLoginEvent extends ScreenIntoSixEvent {
  CreateLoginEvent(
      {this.onCreateLoginEventSuccess, this.onCreateLoginEventError});

  Function? onCreateLoginEventSuccess;

  Function? onCreateLoginEventError;

  @override
  List<Object?> get props =>
      [onCreateLoginEventSuccess, onCreateLoginEventError];
}
File: Repository
•	Repository class for managing API requests.
•	This class provides a simplified interface for making the API request using the ApiClient instance
class Repository {
  final _apiClient = ApiClient();

  Future<PostLoginDeviceAuthResp> loginDeviceAuth({
    Map<String, String> headers = const {},
    Map requestData = const {},
  }) async {
    return await _apiClient.loginDeviceAuth(
      headers: headers,
      requestData: requestData,
    );
  }
}
File: ApiClient
•	Method sends a POST request to the server's endpoint with the provided headers and request data
•	Returns a PostLoginDeviceAuthResp object representing the response.
•	Throws an error if the request fails or an exception occurs.
  Future<PostLoginDeviceAuthResp> loginDeviceAuth({
    Map<String, String> headers = const {},
    Map requestData = const {},
  }) async {
    ProgressDialogUtils.showProgressDialog();
    try {
      await isNetworkConnected();
      var response = await _dio.post(
        '$url/device/auth/login',
        data: requestData,
        options: Options(headers: headers),
      );
      ProgressDialogUtils.hideProgressDialog();
      if (_isSuccessCall(response)) {
        return PostLoginDeviceAuthResp.fromJson(response.data);
      } else {
        throw response.data != null
            ? PostLoginDeviceAuthResp.fromJson(response.data)
            : 'Something Went Wrong!';
      }
    } catch (error, stackTrace) {
      ProgressDialogUtils.hideProgressDialog();
      Logger.log(
        error,
        stackTrace: stackTrace,
      );
      rethrow;
    }
  }
API Integration in DhiWise
•	If you want to integrate the APIs inside the Flutter project, you can follow the below steps to manage API calls effectively.
1.	Selection of API Integration: Go to your application's screen listing page and select 'API Integration' from the left menu.
2.	API Management Options: You have the option to either import APIs or create new ones.
•	To import APIs, click on Import APIs, and choose either to upload Postman collection/ Environment/Swagger file or add URLs for your APIs.
•	If you wish to create new APIs, click on '+ Create an API'.
3.	Select screen: Start by selecting the screen where you want to set up the API. This can be done either from the screen list or by choosing the Configure option for a particular screen within your DhiWise application.
4.	Select widget: Next, you need to specify the widget to which you want to add the API integration. To do this, switch to the widget view and add an onClick property for setting up the action. From the list of available actions, choose "API integration".
5.	Set function name: Once you choose the API integration action, the first thing it will ask for is a valid function name for your API integration. This function will be generated for your screen code.
6.	Select your API: From the list of APIs added in DhiWise, select the API that you want to bind to the chosen widget or lifecycle method.
7.	Once you've selected the API, there are three key steps to complete the integration:
•	Step 1: Handle Request: You need to set the API's Header, Parameters, and Body. These values should match what you specified when adding the API, although they can be modified here. You can bind your request key with a view, constant, API response, value stored in preferences, or a saved argument from navigation.
•	Step 2: Handle Response: This step involves binding the response values with the views on your screen where you want to display the response. You can select the relevant key from the response, choose 'View' from the options, and then choose the view in which you would like to display the response. You also have the option to load data in your screens by binding the response body with the ListView/GridView or Slider view. Finally, you can choose to save the response data to preferences.
•	Step 3: Handle Actions: In this final part, you get to decide which actions to perform on success and failure after the API call. Select an action from the list and set it up with the required inputs.
8.	Once these steps are completed, click on "Submit" to complete the API integration.
These summaries give a straightforward understanding of the functionalities related to API calls within your application. For more details, please review below link : API Implementation

