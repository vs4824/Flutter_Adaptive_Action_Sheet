# Flutter Adaptive Action Sheet

A action bottom sheet that adapts to the platform (Android/iOS).

## Getting Started

Add the package to your pubspec.yaml:

   ```
   adaptive_action_sheet: ^2.0.2
   ```

In your dart file, import the library:

   ```
   import 'package:adaptive_action_sheet/adaptive_action_sheet.dart';
   ```

Instead of using a showModalBottomSheet use showAdaptiveActionSheet Widget:

   ```
   showAdaptiveActionSheet(
 context: context,
 title: const Text('Title'),
 androidBorderRadius: 30,
 actions: <BottomSheetAction>[
    BottomSheetAction(title: const Text('Item 1'), onPressed: (context) {}),
    BottomSheetAction(title: const Text('Item 2'), onPressed: (context) {}),
    BottomSheetAction(title: const Text('Item 3'), onPressed: (context) {}),
 ],
 cancelAction: CancelAction(title: const Text('Cancel')),// onPressed parameter is optional by default will dismiss the ActionSheet
);
   ```

## Parameters

### showAdaptiveActionSheet:

1. actions: The Actions list that will appear on the ActionSheet. (required)

2. cancelAction: The optional cancel button that show under the actions (grouped separately on iOS).

3. title: The optional title widget that show above the actions.

4. androidBorderRadius: The android border radius (default: 30).

5. isDismissible: Specifies whether the bottom sheet will be dismissed when user taps outside of the bottom sheet. It is true by default and cannot be null.

6. The optional backgroundColor and barrierColor can be passed in to customize the appearance and behavior of persistent material bottom sheets(Android only).

### BottomSheetAction:

1. title: The primary content of the action sheet item. (required)

2. onPressed: The callback that is called when the action item is tapped. (required)

3. leading: A widget to display before the title. Typically an Icon widget. (optional)

4. trailing: A widget to display after the title. Typically an Icon or a CircleAvatar widget. (optional)

### CancelAction:

1. title: The primary content of the cancel action sheet item. (required)

2. onPressed: The callback that is called when the action item is tapped. onPressed is optional by default will dismiss the Action Sheet.
