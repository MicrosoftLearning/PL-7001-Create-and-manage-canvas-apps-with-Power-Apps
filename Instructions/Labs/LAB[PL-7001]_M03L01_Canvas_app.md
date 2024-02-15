---
lab:
    title: 'Lab 3: Create a canvas app'
    module: 'Module 3: Customize a canvas app in Power Apps'
---

# Practice Lab 3 – Create a canvas app

In this lab you will design and build a canvas app from blank, add a data source and a gallery.

## What you will learn

- How to create a canvas app with a gallery linked to a data source
- How to format fields with Power Fx formulas

## High-level lab steps

- Create a canvas app from blank
- Add a data source to the app
- Add a gallery to the app
- Configure the fields in the gallery
  
## Prerequisites

- Must have completed **Lab 2: Data model**

## Detailed steps

## Exercise 1 – Create a canvas app

### Task 1.1 - Create the app

1. Navigate to the Power Apps Maker portal <https://make.powerapps.com>.

1. Make sure you are in the **Dev One** environment.

1. Select the **+ Create** tab from the left-side menu.

1. Select the **Blank app** tile under **Start from**.

    ![Screenshot of create from blank.](../media/create-from-blank.png)

1. Select **Create** under the **Blank canvas app** tile.

1. Enter `Booking Request app` for **App name**.

1. Select **Tablet** for **Format**.

    ![Screenshot of new app name.](../media/app-name-format.png)

1. Select **Create**.

1. Wait for the app to be built.

1. Select **Save** in the top-right of the Power Apps Studio.

### Task 1.2 - Add data source

1. In the app authoring menu, select **Data**.

    ![Screenshot of Data pane.](../media/studio-data-pane.png)

1. Select the drop-down caret next to **Add data** and enter `Booking` in **Search**.

    ![Screenshot of select data source.](../media/studio-data-search.png)

1. Select the **Booking Requests** Microsoft Dataverse table.

### Task 1.3 - Configure the main screen

1. In the app authoring menu, select **Tree view**.

1. Select **Screen1** in the tree view and select the ellipses (**...**) and select **Rename**.

1. Enter `MainScreen`.

1. In the app authoring menu, select **Insert (+)**.

1. Select **Rectangle**.

1. Drag the rectangle to the top left of the screen.

1. In the app authoring menu, select **Tree view**.

1. Rename the rectangle to `HeaderRect`.

1. Set the properties of the rectangle in the formula bar as follows:

   1. X=`0`
   1. Y=`0`
   1. Height=`80`
   1. Width=`Parent.Width`

1. In the app authoring menu, select **Insert (+)**.

1. Select **Text label**.

1. Drag the label to the top left of the screen.

1. In the app authoring menu, select **Tree view**.

1. Rename the label to `HeaderLabel`.

1. Set the properties of the label in the formula bar as follows:

   1. X=`0`
   1. Y=`0`
   1. Height=`80`
   1. Width=`Parent.Width`
   1. Align=`Align.Center`
   1. Size=`24`
   1. Text=`"Booking Request"`
   1. Color=`Color.White`

    ![Screenshot of the main screen with header.](../media/main-screen.png)

1. Select **Save** in the top-right of the Power Apps Studio.

### Task 1.4 - Add a gallery

1. In the app authoring menu, select **Insert (+)**.

1. Select **Vertical gallery**.

    ![Screenshot of adding a gallery.](../media/add-gallery.png)

1. Select **Booking Requests**.

    ![Screenshot of gallery properties.](../media/gallery-properties.png)

1. Select **Title, subtitle, and body** for **Layout**.

1. Select **7 selected** next to **Fields**

1. Select **Cost** for **Body**.

1. Select **Decision** for **Subtitle**.

1. Select **Pet Name** for **Title**.

    ![Screenshot of gallery fields.](../media/select-fields.png)

1. Close the Data pane.

1. In the app authoring menu, select **Tree view**.

1. Rename the gallery to `BookingRequestList`.

1. Set the properties of the gallery in the formula bar as follows:

   1. X=`0`
   1. Y=`80`
   1. Height=`575`
   1. Width=`250`

### Task 1.5 - Format the currency field

1. In the app authoring menu, select **Tree view**.

1. Expand the gallery.

1. Select the body.

    ![Screenshot of body field selected.](../media/body.png)

1. Set the **Text** property in the formula bar to the formula:

    ```powerappsfl
    Text(Value(ThisItem.Cost), "$#,##0.00")
    ```

1. Select **Save** in the top-right of the Power Apps Studio.

1. Select the **<- Back** button from the top left of the command bar, and select **Leave** to exit the app.
