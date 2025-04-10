# ezlibrary

Cross-Platform UI Libraries Documentation

This document outlines the usage, API, and extended features of a suite of cross-platform UI libraries created to simplify mobile development in Swift (iOS), Kotlin (Android), Dart (Flutter), and React Native. These libraries offer an intuitive and unified approach to building mobile apps rapidly with a focus on reducing boilerplate code and enhancing customization.

💼 Library Names

Swift: SimpleUIKit

Kotlin: KotlinEZUI

Dart: EZFlutterUI

React Native: rn-simple-ui

🛠 Installation & Setup

Swift (SimpleUIKit)

import SimpleUIKit

Kotlin (KotlinEZUI)

import com.kotlin.ezui.*

Dart (EZFlutterUI)

import 'package:ez_flutter_ui/ez_flutter_ui.dart';

React Native (rn-simple-ui)

import {
  SimpleLayout,
  SimpleMenu,
  SimpleNavBar,
  SimpleCard,
  SimpleInput,
  SimpleButton,
  SimpleIcon,
  SimpleGrid,
  SimpleScroll,
  SimpleBackground,
  connectToAPI,
  sendToBackend,
  setDatabase,
  setupPayment,
} from 'rn-simple-ui';

🔧 Core Components & Features

1. Layout System (Grid Based)

Layouts help divide your screen space and place elements precisely. Here’s how to use them:

Swift

SimpleLayout.columnFlex()
SimpleLayout.rowFlex()
SimpleLayout.grid(columns: 3, span: [2, 1])
SimpleLayout.fixed(width: 300)
SimpleLayout.adaptiveHeight(min: 200, max: 600)

Kotlin

SimpleLayout.columnFlex()
SimpleLayout.rowFlex()
SimpleLayout.grid(columns = 3, span = listOf(2, 1))
SimpleLayout.fixed(width = 300)
SimpleLayout.adaptiveHeight(min = 200, max = 600)

Dart

SimpleLayout.columnFlex()
SimpleLayout.rowFlex()
SimpleLayout.grid(columns: 3, span: [2, 1])
SimpleLayout.fixed(width: 300)
SimpleLayout.adaptiveHeight(min: 200, max: 600)

React Native

<SimpleLayout type="columnFlex" />
<SimpleLayout type="rowFlex" />
<SimpleLayout type="grid" columns={3} span={[2, 1]} />
<SimpleLayout type="fixed" width={300} />
<SimpleLayout type="adaptiveHeight" min={200} max={600} />

To integrate:

Import layout from the respective library.

Wrap child components inside.

Use grid, columnFlex, etc. to define screen structure.

2. Menus

Menus enable intuitive user navigation through the app.

Swift

SimpleMenu.dropdown(title: "Menu", items: ["Home", "Profile"])
SimpleMenu.sideDrawer(title: "Menu", items: ["Home", "Settings"])
SimpleMenu.bottomSheet(title: "Menu", items: ["Help", "Logout"])
SimpleMenu.hamburgerToggle(items: ["Feed", "Messages"])
SimpleMenu.floatingAction(actions: ["Add", "Scan"])

Kotlin

SimpleMenu.dropdown(title = "Menu", items = listOf("Home", "Profile"))
SimpleMenu.sideDrawer(title = "Menu", items = listOf("Home", "Settings"))
SimpleMenu.bottomSheet(title = "Menu", items = listOf("Help", "Logout"))
SimpleMenu.hamburgerToggle(items = listOf("Feed", "Messages"))
SimpleMenu.floatingAction(actions = listOf("Add", "Scan"))

Dart

SimpleMenu.dropdown(title: "Menu", items: ["Home", "Profile"])
SimpleMenu.sideDrawer(title: "Menu", items: ["Home", "Settings"])
SimpleMenu.bottomSheet(title: "Menu", items: ["Help", "Logout"])
SimpleMenu.hamburgerToggle(items: ["Feed", "Messages"])
SimpleMenu.floatingAction(actions: ["Add", "Scan"])

React Native

<SimpleMenu type="dropdown" title="Menu" items={["Home", "Profile"]} />
<SimpleMenu type="sideDrawer" title="Menu" items={["Home", "Settings"]} />
<SimpleMenu type="bottomSheet" title="Menu" items={["Help", "Logout"]} />
<SimpleMenu type="hamburger" items={["Feed", "Messages"]} />
<SimpleMenu type="fab" actions={["Add", "Scan"]} />

To integrate:

Import SimpleMenu.

Choose the menu type.

Pass props like title, items, or actions.

3. Bottom Navigation

Bottom navigation helps users switch between top-level views quickly.

Swift

SimpleNavBar.tabs(items: ["Home", "Search", "Profile"])
SimpleNavBar.icons(icons: ["house", "magnifyingglass", "person"])
SimpleNavBar.shifting(items: ["Feed", "Explore", "Account"])
SimpleNavBar.customStyle(items: ["A", "B", "C"], style: .rounded)
SimpleNavBar.fabIntegration(items: ["Home", "Add", "Settings"])

Kotlin

SimpleNavBar.tabs(items = listOf("Home", "Search", "Profile"))
SimpleNavBar.icons(icons = listOf("house", "magnify", "account"))
SimpleNavBar.shifting(items = listOf("Feed", "Explore", "Account"))
SimpleNavBar.customStyle(items = listOf("A", "B", "C"), style = Style.ROUNDED)
SimpleNavBar.fabIntegration(items = listOf("Home", "Add", "Settings"))

Dart

SimpleNavBar.tabs(items: ["Home", "Search", "Profile"])
SimpleNavBar.icons(icons: ["house", "magnify", "account"])
SimpleNavBar.shifting(items: ["Feed", "Explore", "Account"])
SimpleNavBar.customStyle(items: ["A", "B", "C"], style: Style.rounded)
SimpleNavBar.fabIntegration(items: ["Home", "Add", "Settings"])

React Native

<SimpleNavBar type="tabs" items={["Home", "Search", "Profile"]} />
<SimpleNavBar type="icons" icons={["house", "magnify", "account"]} />
<SimpleNavBar type="shifting" items={["Feed", "Explore", "Account"]} />
<SimpleNavBar type="customStyle" items={["A", "B", "C"]} style="rounded" />
<SimpleNavBar type="fabIntegration" items={["Home", "Add", "Settings"]} />

To integrate:

Import SimpleNavBar.

Choose the navigation pattern.

Customize items and icon sets accordingly.

4. Cards

Cards are versatile UI containers for displaying grouped content such as text, images, or actions.

Swift

SimpleCard.basic(title: "Welcome", content: "This is a basic card")
SimpleCard.withImage(imageName: "profile", title: "Profile", description: "User profile card")
SimpleCard.elevated(content: "Important info", elevation: 4)
SimpleCard.actionable(title: "Tap me", onTap: { print("Card tapped!") })

Kotlin

SimpleCard.basic(title = "Welcome", content = "This is a basic card")
SimpleCard.withImage(imageName = "profile", title = "Profile", description = "User profile card")
SimpleCard.elevated(content = "Important info", elevation = 4)
SimpleCard.actionable(title = "Tap me") { println("Card tapped!") }

Dart

SimpleCard.basic(title: "Welcome", content: "This is a basic card")
SimpleCard.withImage(imageName: "profile", title: "Profile", description: "User profile card")
SimpleCard.elevated(content: "Important info", elevation: 4)
SimpleCard.actionable(title: "Tap me", onTap: () => print("Card tapped!"))

React Native

<SimpleCard type="basic" title="Welcome" content="This is a basic card" />
<SimpleCard type="withImage" imageName="profile" title="Profile" description="User profile card" />
<SimpleCard type="elevated" content="Important info" elevation={4} />
<SimpleCard type="actionable" title="Tap me" onTap={() => console.log("Card tapped!")} />

To integrate:

Import SimpleCard.

Choose the card variant (basic, with image, elevated, actionable).

Pass in required props like title, content, onTap, or elevation.

🔗 How to Integrate with This Documentation

Copy and Paste: Choose the language tab and copy the code into your IDE.

Import Statement: Always begin with the import provided at the top.

Component Usage: Use the layout and UI building blocks just as shown.

Customize: Adjust the values of x, y, items, padding, etc. to meet your needs.

Preview: Run the code in a mobile emulator to see results in real time.

Use Previews and Layout Images: Refer to the attached image section in the documentation or emulator screenshots to help visualize layout results.

📆 Future Development Roadmap



You can continue expanding these features with provided visual and backend integration tools, ensuring accessibility, faster builds, and beautifully responsive UI designs.

Happy building 🚀
