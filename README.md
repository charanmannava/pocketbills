# <img src="https://github.com/PranavTJ-05/PocketBills/blob/main/app/src/main/res/drawable/ic_logo.png" alt="logo" width="40"/> PocketBills 💲 
A Simple Expense Tracker App 📱 built to demonstrate the use of modern android architecture component with MVVM Architecture 🏗. 

<img src="https://github.com/PranavTJ-05/PocketBills/blob/main/app/src/main/res/drawable/Title_banner_pocketBills.png" alt="logo" width="2000"/>

<br />




## Built With 🛠
#### We have attached the Documentations we have read and come across to built this application.

- [Kotlin](https://kotlinlang.org/) - First class and official programming language for Android development.
- [Coroutines](https://kotlinlang.org/docs/reference/coroutines-overview.html) - For asynchronous and more..
- [Android Architecture Components](https://developer.android.com/topic/libraries/architecture) - Collection of libraries that help you design robust, testable, and maintainable apps.
  - [Stateflow](https://developer.android.com/kotlin/flow/stateflow-and-sharedflow) - StateFlow is a state-holder observable flow that emits the current and new state updates to its collectors. 
  - [Flow](https://kotlinlang.org/docs/reference/coroutines/flow.html) - A flow is an asynchronous version of a Sequence, a type of collection whose values are lazily produced.
  - [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel) - Stores UI-related data that isn't destroyed on UI changes. 
  - [Room](https://developer.android.com/topic/libraries/architecture/room) - SQLite object mapping library.
  - [Jetpack Navigation](https://developer.android.com/guide/navigation) - Navigation refers to the interactions that allow users to navigate across, into, and back out from the different pieces of content within your app
  - [DataStore](https://developer.android.com/topic/libraries/architecture/datastore) - Jetpack DataStore is a data storage solution that allows you to store key-value pairs or typed objects with protocol buffers. DataStore uses Kotlin coroutines and Flow to store data asynchronously, consistently, and transactionally.
- [Material Components for Android](https://github.com/material-components/material-components-android) - Modular and customizable Material Design UI components for Android.
- [Figma](https://figma.com/) - Figma is a vector graphics editor and prototyping tool which is primarily web-based.

<br />

## Package Structure 📦
    
    ├── app
    ├── .gitignore
    ├── build.gradle.kts
    ├── proguard-rules.pro
    └── src
    │   ├── androidTest
    │       └── java
    │       │   └── com
    │       │       └── engineers100X
    │       │           └── pocketbills
    │       │               └── ExampleInstrumentedTest.kt
    │   ├── main
    │       ├── AndroidManifest.xml
    │       ├── java
    │       │   └── com
    │       │   │   └── engineers100X
    │       │   │       └── pocketbills
    │       │   │           ├── app
    │       │   │               └── ExpenseTracker.kt
    │       │   │           ├── data
    │       │   │               └── local
    │       │   │               │   ├── AppDatabase.kt
    │       │   │               │   ├── TransactionDao.kt
    │       │   │               │   └── datastore
    │       │   │               │       └── UIModeDataStore.kt
    │       │   │           ├── di
    │       │   │               └── AppModule.kt
    │       │   │           ├── model
    │       │   │               └── Transaction.kt
    │       │   │           ├── repo
    │       │   │               └── TransactionRepo.kt
    │       │   │           ├── services
    │       │   │               └── exportcsv
    │       │   │               │   ├── CsvActivityContracts.kt
    │       │   │               │   ├── ExportCsvService.kt
    │       │   │               │   └── TransactionsCsv.kt
    │       │   │           ├── utils
    │       │   │               ├── Constants.kt
    │       │   │               ├── DEFAULT_FILENAME.kt
    │       │   │               ├── ViewExt.kt
    │       │   │               ├── viewModelFactory.kt
    │       │   │               └── viewState
    │       │   │               │   ├── DetailState.kt
    │       │   │               │   ├── ExportState.kt
    │       │   │               │   └── ViewState.kt
    │       │   │           └── view
    │       │   │               ├── about
    │       │   │                   ├── AboutFragment.kt
    │       │   │                   └── AboutViewModel.kt
    │       │   │               ├── adapter
    │       │   │                   └── TransactionAdapter.kt
    │       │   │               ├── add
    │       │   │                   └── AddTransactionFragment.kt
    │       │   │               ├── base
    │       │   │                   └── BaseFragment.kt
    │       │   │               ├── dashboard
    │       │   │                   └── DashboardFragment.kt
    │       │   │               ├── details
    │       │   │                   └── TransactionDetailsFragment.kt
    │       │   │               ├── dialog
    │       │   │                   └── ErrorDialog.kt
    │       │   │               ├── edit
    │       │   │                   └── EditTransactionFragment.kt
    │       │   │               └── main
    │       │   │                   ├── MainActivity.kt
    │       │   │                   └── viewmodel
    │       │   │                       └── TransactionViewModel.kt
    │       └── res
    │       │   ├── anim
    │       │       ├── slide_in_left.xml
    │       │       ├── slide_in_right.xml
    │       │       ├── slide_out_left.xml
    │       │       └── slide_out_right.xml
    │       │   ├── drawable-v24
    │       │       └── ic_launcher_foreground.xml
    │       │   ├── drawable
    │       │       ├── ic_logo.png
    │       │   ├── layout
    │       │       ├── activity_main.xml
    │       │       ├── content_add_transaction_layout.xml
    │       │       ├── content_empty_state_layout.xml
    │       │       ├── content_income_expense_card_layout.xml
    │       │       ├── content_transaction_details.xml
    │       │       ├── error_dialog_layout.xml
    │       │       ├── fragment_about.xml
    │       │       ├── fragment_add_transaction.xml
    │       │       ├── fragment_dashboard.xml
    │       │       ├── fragment_edit_transaction.xml
    │       │       ├── fragment_transaction_details.xml
    │       │       ├── item_autocomplete_layout.xml
    │       │       ├── item_filter_dropdown.xml
    │       │       ├── item_transaction_layout.xml
    │       │       └── total_balance_view.xml
    │       │   ├── menu
    │       │       ├── menu_share.xml
    │       │       └── menu_ui.xml
    │       │   ├── navigation
    │       │       └── nav_graph.xml
    │       │   ├── raw
    │       │       ├── empty.json
    │       │       └── failed.json
    │       │   ├── values-night
    │       │       ├── colors.xml
    │       │       └── themes.xml
    │       │   └── values
    │       │       ├── colors.xml
    │       │       ├── dimen.xml
    │       │       ├── filters.xml
    │       │       ├── font_certs.xml
    │       │       ├── preloaded_fonts.xml
    │       │       ├── strings.xml
    │       │       ├── styles.xml
    │       │       └── themes.xml
	├── beta_android.png
	├── build.gradle.kts
	├── gradle.properties
	├── gradle
	    └── wrapper
	    │   ├── gradle-wrapper.jar
	    │   └── gradle-wrapper.properties
	├── gradlew
	├── gradlew.bat
	└── settings.gradle

## Architecture 🗼
This app uses [***MVVM (Model View View-Model)***](https://developer.android.com/jetpack/docs/guide#recommended-app-arch) architecture.

## Build-tool 🧰
You need to have [Android Studio Beta 3 or above](https://developer.android.com/studio/preview) to build this project.
