---
description: В примере Auto Claims рассматривается гипотетический сценарий для страхового полиса.
ms.assetid: bec4333a-62ca-4254-a39b-04bc2c556992
title: Пример формы Auto Claims
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c5ff78a3c38036ef9352660b4d7959e2ad87e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346892"
---
# <a name="auto-claims-form-sample"></a><span data-ttu-id="321ef-103">Пример формы Auto Claims</span><span class="sxs-lookup"><span data-stu-id="321ef-103">Auto Claims Form Sample</span></span>

<span data-ttu-id="321ef-104">В примере Auto Claims рассматривается гипотетический сценарий для страхового полиса.</span><span class="sxs-lookup"><span data-stu-id="321ef-104">The Auto Claims sample addresses a hypothetical scenario for an insurance assessor.</span></span> <span data-ttu-id="321ef-105">Для работы по оценке необходимо, чтобы он был посещен клиентами дома или бизнеса и вводил свои сведения о заявках в форму.</span><span class="sxs-lookup"><span data-stu-id="321ef-105">The assessor's work requires him or her to visit with clients at their home or business and to enter their claim information into a form.</span></span> <span data-ttu-id="321ef-106">Чтобы повысить продуктивность оценки, ИТ-отдел разрабатывает приложение для планшетов, которое позволяет ему быстро и точно вводить сведения о заявках с помощью двух элементов управления рукописного ввода: [InkEdit](/previous-versions/ms835842(v=msdn.10)) и [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="321ef-106">To increase the assessor's productivity, his IT department develops a tablet application that enables him or her to quickly and accurately enter claim information through two ink controls: [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls.</span></span>

<span data-ttu-id="321ef-107">В этом примере для каждого текстового поля ввода используется элемент управления [InkEdit](/previous-versions/ms835842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="321ef-107">In this sample, a [InkEdit](/previous-versions/ms835842(v=msdn.10)) control is used for each text input field.</span></span> <span data-ttu-id="321ef-108">Пользователь вводит соответствующую информацию о страховой полисе и транспорте в эти поля с помощью пера.</span><span class="sxs-lookup"><span data-stu-id="321ef-108">A user enters the relevant information about an insurance policy and vehicle into these fields with a pen.</span></span> <span data-ttu-id="321ef-109">Элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) используется для добавления рукописного ввода в изображение автомобиля для выделения поврежденных областей автомобиля.</span><span class="sxs-lookup"><span data-stu-id="321ef-109">The [InkPicture](/previous-versions/ms583740(v=vs.100)) control is used to add ink over an automobile image to highlight damaged areas of the automobile.</span></span> <span data-ttu-id="321ef-110">Образец Auto Claims доступен для C \# и Microsoft Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="321ef-110">The Auto Claims sample is available for C\# and Microsoft Visual Basic .NET.</span></span> <span data-ttu-id="321ef-111">В этом разделе описывается Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="321ef-111">This topic describes the Visual Basic .NET.</span></span>

<span data-ttu-id="321ef-112">Класс автозаявок определяется как подкласс [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , а вложенный класс определяется для создания и управления уровнями рукописного ввода для различных типов повреждений.</span><span class="sxs-lookup"><span data-stu-id="321ef-112">The AutoClaims Class is defined as a subclass of [System.Windows.Forms.Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , and a nested class is defined for creating and managing layers of ink for different types of damage.</span></span> <span data-ttu-id="321ef-113">Для выполнения следующих задач определены четыре обработчика событий:</span><span class="sxs-lookup"><span data-stu-id="321ef-113">Four event handlers are defined to perform the following tasks:</span></span>

-   <span data-ttu-id="321ef-114">Инициализация формы и слоев рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="321ef-114">Initializing the form and ink layers.</span></span>
-   <span data-ttu-id="321ef-115">Перерисовка элемента управления [InkPicture](/previous-versions/ms583740(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="321ef-115">Redrawing the [InkPicture](/previous-versions/ms583740(v=vs.100)) control.</span></span>
-   <span data-ttu-id="321ef-116">Выбор слоя рукописного ввода с помощью списка.</span><span class="sxs-lookup"><span data-stu-id="321ef-116">Selecting an ink layer through the list box.</span></span>
-   <span data-ttu-id="321ef-117">Изменение видимости слоя рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="321ef-117">Changing the visibility of an ink layer.</span></span>

> [!Note]  
> <span data-ttu-id="321ef-118">Версии этого образца доступны в C \# и Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="321ef-118">Versions of this sample are available in C\# and Visual Basic .NET.</span></span> <span data-ttu-id="321ef-119">Версия, описанная в этом разделе, — Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="321ef-119">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="321ef-120">Эти понятия одинаковы для разных версий.</span><span class="sxs-lookup"><span data-stu-id="321ef-120">The concepts are the same between versions.</span></span>

 

## <a name="defining-the-form-and-ink-layers"></a><span data-ttu-id="321ef-121">Определение формы и слоев рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="321ef-121">Defining the Form and Ink Layers</span></span>

<span data-ttu-id="321ef-122">Необходимо импортировать пространство имен [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="321ef-122">You need to import the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace:</span></span>


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



<span data-ttu-id="321ef-123">Затем в классе автозаявок определяется вложенный `InkLayer` класс и объявляется массив из четырех `InkLayer` объектов.</span><span class="sxs-lookup"><span data-stu-id="321ef-123">Next, in the AutoClaims Class, a nested `InkLayer` class is defined and an array of four `InkLayer` objects is declared.</span></span> <span data-ttu-id="321ef-124">(Инклайер содержит объект [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) для хранения рукописных данных, а также значения [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) и **Boolean** для сохранения цвета и скрытого состояния слоя.) Пятый объект рукописного ввода объявляется для обработки рукописного ввода [, когда все](/previous-versions/ms583740(v=vs.100)) слои рукописного ввода скрыты.</span><span class="sxs-lookup"><span data-stu-id="321ef-124">(InkLayer contains an [Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100)) object for storing ink, and [System.Drawing.Color](/dotnet/api/system.drawing.color?view=netcore-3.1) and **Boolean** values for storing the color and hidden state of the layer.) A fifth Ink object is declared to handle ink for the [InkPicture](/previous-versions/ms583740(v=vs.100)) when all of the ink layers are hidden.</span></span>


```VB
' Declare the array of ink layers used the vehicle illustration.
Dim inkLayers(3) As InkLayer

' Declare an empty ink object (used when we don't want to draw
' any ink).
Dim emptyInk As Ink

' Declare a value to hold the index of selected ink
Dim selectedIndex As Integer

' Declare a value to hold whether the selected ink is hidden
Dim selectedHidden As Boolean 
```




```VB
// Declare the array of ink layers used the vehicle illustration.
InkLayer[] inkLayers;

// Declare an empty ink object (used when we don't want to draw
// any ink).
Ink emptyInk;

// Declare a value to hold the index of selected ink
int selectedIndex = -1;

// Declare a value to hold whether the selected ink is hidden
bool selectedHidden = false;
```



<span data-ttu-id="321ef-125">Каждый слой имеет собственный объект [рукописного ввода](/previous-versions/ms583670(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="321ef-125">Each layer has its own [Ink](/previous-versions/ms583670(v=vs.100)) object.</span></span> <span data-ttu-id="321ef-126">В форме заявки (текст, Windows, завершение и фары) имеется четыре дискретных области, поэтому используются четыре объекта Инклайер.</span><span class="sxs-lookup"><span data-stu-id="321ef-126">There are four discrete areas of interest in the claim form (body, windows, tires, and headlights), so four InkLayer objects are used.</span></span> <span data-ttu-id="321ef-127">Пользователь может просматривать любое сочетание слоев одновременно.</span><span class="sxs-lookup"><span data-stu-id="321ef-127">A user can view any combination of layers at once.</span></span>

## <a name="initializing-the-form-and-ink-layers"></a><span data-ttu-id="321ef-128">Инициализация формы и слоев рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="321ef-128">Initializing the Form and Ink Layers</span></span>

<span data-ttu-id="321ef-129">`Load`Обработчик событий инициализирует объект [рукописного ввода](/previous-versions/ms583670(v=vs.100)) и четыре `InkLayer` объекта.</span><span class="sxs-lookup"><span data-stu-id="321ef-129">The `Load` event handler initializes the [Ink](/previous-versions/ms583670(v=vs.100)) object and the four `InkLayer` objects.</span></span>


```VB
' Initialize the empty ink
emptyInk = New Ink()

' Initialize the four different layers of ink on the vehicle diagram:  
' vehicle body, windows, tires, and headlights.
inkLayers(0) = New InkLayer(New Ink(), Color.Red, False)
inkLayers(1) = New InkLayer(New Ink(), Color.Violet, False)
inkLayers(2) = New InkLayer(New Ink(), Color.LightGreen, False)
inkLayers(3) = New InkLayer(New Ink(), Color.Aqua, False)
```




```VB
// Initialize the empty ink
emptyInk = new Ink();

// Initialize the four different layers of ink on the vehicle diagram:  
// vehicle body, windows, tires, and headlights.
inkLayers = new InkLayer[4];
inkLayers[0] = new InkLayer(new Ink(), Color.Red, false);
inkLayers[1] = new InkLayer(new Ink(), Color.Violet, false);
inkLayers[2] = new InkLayer(new Ink(), Color.LightGreen, false);
inkLayers[3] = new InkLayer(new Ink(), Color.Aqua, false);
```



<span data-ttu-id="321ef-130">Затем выберите первую запись (текст) в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="321ef-130">Then, select the first entry (Body) in the list box.</span></span>


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



<span data-ttu-id="321ef-131">Наконец, установите цвет рукописного ввода для элемента управления [InkPicture](/previous-versions/ms583740(v=vs.100)) на выбранную в текущий момент запись в поле со списком.</span><span class="sxs-lookup"><span data-stu-id="321ef-131">Finally, set the ink color for the [InkPicture](/previous-versions/ms583740(v=vs.100)) control to the currently selected list box entry.</span></span>


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a><span data-ttu-id="321ef-132">Перерисовка элемента управления InkPicture</span><span class="sxs-lookup"><span data-stu-id="321ef-132">Redrawing the InkPicture Control</span></span>

<span data-ttu-id="321ef-133">В наследуемом обработчике событий [рисования](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) элемента управления [InkPicture](/previous-versions/ms583740(v=vs.100)) слои рукописного ввода проверяются, чтобы определить, какие из них скрыты.</span><span class="sxs-lookup"><span data-stu-id="321ef-133">In the [InkPicture](/previous-versions/ms583740(v=vs.100)) Control's inherited [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event handler, the ink layers are checked to determine which are hidden.</span></span> <span data-ttu-id="321ef-134">Если слой не скрыт, процедура события отображает его с помощью метода [Draw](/previous-versions/ms828488(v=msdn.10)) свойства средства [визуализации](/previous-versions/ms582196(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="321ef-134">If a layer is not hidden, the event procedure displays it by using the [Renderer](/previous-versions/ms582196(v=vs.100)) property's [Draw](/previous-versions/ms828488(v=msdn.10)) method.</span></span> <span data-ttu-id="321ef-135">Если взглянуть на обозреватель объектов, вы увидите, что свойство Microsoft. Ink. InkPicture. Render определено как объект [Microsoft. Ink. Render](/previous-versions/ms828481(v=msdn.10)) :</span><span class="sxs-lookup"><span data-stu-id="321ef-135">If you look in the Object Browser, you'll see that the Microsoft.Ink.InkPicture.Renderer property is defined as a [Microsoft.Ink.Renderer](/previous-versions/ms828481(v=msdn.10)) object:</span></span>


```VB
Private Sub inkPictVehicle_Paint(ByVal sender As System.Object, ByVal e As System.Windows.Forms.PaintEventArgs) Handles inkPictVehicle.Paint
    Dim layer As InkLayer

    ' Cycle through each ink layer.  If it is visible, paint it.
    ' Note that it is necessary to customize the paint
    ' behavior, since we want to hide/show different ink layers.
    For Each layer In inkLayers
        If (Not layer.Hidden) Then
            inkPictVehicle.Renderer.Draw(e.Graphics, layer.ActiveInk.Strokes)
        End If
    Next
End Sub
```




```VB
private void inkPictVehicle_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    // Cycle through each ink layer.  If it is visible, paint it.
    // Note that it is necessary to customize the paint
    // behavior, since we want to hide/show different ink layers.
    foreach (InkLayer layer in inkLayers)
    {
        if (!layer.Hidden)
        {
             inkPictVehicle.Renderer.Draw(e.Graphics,layer.ActiveInk.Strokes);
        }
    }          
}
```



## <a name="selecting-an-ink-layer-through-the-list-box"></a><span data-ttu-id="321ef-136">Выбор слоя рукописного ввода с помощью списка</span><span class="sxs-lookup"><span data-stu-id="321ef-136">Selecting an Ink Layer through the List Box</span></span>

<span data-ttu-id="321ef-137">Когда пользователь выбирает элемент в списке, [обработчик событий в](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) начале проверяет, что выделение изменилось и элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) в настоящее время не собирает рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="321ef-137">When the user selects an item in the list box, the [SelectedIndexChanged](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="321ef-138">Затем он устанавливает цвет чернил элемента управления InkPicture на соответствующий цвет для выбранного слоя рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="321ef-138">It then sets the ink color of the InkPicture control to the appropriate color for the selected ink layer.</span></span> <span data-ttu-id="321ef-139">Кроме того, он обновляет флажок скрыть слой, чтобы отразить состояние выбранного слоя рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="321ef-139">Also, it updates the Hide Layer check box to reflect the selected ink layer's hidden status.</span></span> <span data-ttu-id="321ef-140">Наконец, наследуемый метод [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) элемента управления InkPicture используется для вывода только нужных слоев внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="321ef-140">Finally, the InkPicture control's inherited [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
       Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
       End If
   End If
End Sub
```




```VB
private void lstAnnotationLayer_SelectedIndexChanged(object sender, System.EventArgs e)
{
    // Provided that the new selected index value is different than
    // the previous value...
    if (lstAnnotationLayer.SelectedIndex != selectedIndex) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Set the ink and visiblity of the current ink layer
            inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
            chHideLayer.Checked = inkLayers[lstAnnotationLayer.SelectedIndex].Hidden;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;
    
            selectedIndex = lstAnnotationLayer.SelectedIndex;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the selection to its previous value.
            lstAnnotationLayer.SelectedIndex = selectedIndex;
            MessageBox.Show("Cannot change active ink while collecting ink.");
        }
    }
}
```



## <a name="changing-the-visibility-of-an-ink-layer"></a><span data-ttu-id="321ef-141">Изменение видимости слоя рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="321ef-141">Changing the Visibility of an Ink Layer</span></span>

<span data-ttu-id="321ef-142">`CheckedChanged`Обработчик событий сначала проверяет, что выделение изменилось и элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) в настоящее время не собирает рукописный ввод.</span><span class="sxs-lookup"><span data-stu-id="321ef-142">The `CheckedChanged` event handler first checks that the selection has changed and that the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is not currently collecting ink.</span></span> <span data-ttu-id="321ef-143">Затем он обновляет скрытое состояние выбранного слоя рукописного ввода, устанавливает Инкенаблед элемента управления InkPicture в **значение false**,.</span><span class="sxs-lookup"><span data-stu-id="321ef-143">It then updates the selected ink layer's hidden status, sets the InkPicture control's InkEnabled to **FALSE**, .</span></span>

<span data-ttu-id="321ef-144">Далее, перед обновлением свойства рукописного ввода свойство Инкенаблед элемента управления InkPicture имеет значение **false** .</span><span class="sxs-lookup"><span data-stu-id="321ef-144">Next, the InkPicture control's InkEnabled property is set to **FALSE** before updating its Ink property.</span></span>

<span data-ttu-id="321ef-145">Наконец, элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) либо включен, либо отключен для определенной части автомобиля в зависимости от того, установлен ли флажок скрыть слой, а метод [обновления](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) элемента управления InkPicture используется для отображения только нужных слоев внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="321ef-145">Finally, the [InkPicture](/previous-versions/ms583740(v=vs.100)) control is either enabled or disabled for the particular vehicle part based on whether the Hide Layer check box is selected, and the InkPicture control's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method is used to display only the desired layers within the control.</span></span>


```VB
Private Sub chHideLayer_CheckedChanged(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles chHideLayer.CheckedChanged

    ' Provided that the new checked hidden value is different than
    ' the previous value...
    If (Not (chHideLayer.Checked = selectedHidden)) Then
        If (Not (inkPictVehicle.CollectingInk)) Then

            ' Update the array indicating the visibility of each ink layer
            inkLayers(lstAnnotationLayer.SelectedIndex).Hidden = chHideLayer.Checked

            ' Set the active ink object to the selected ink
            ' Note that if the current layer is not visible, empty
            ' ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = False
            If (chHideLayer.Checked) Then
                inkPictVehicle.Ink = emptyInk
            Else
                inkPictVehicle.Ink = inkLayers(lstAnnotationLayer.SelectedIndex).ActiveInk
            End If

            ' Update the previous checkbox value to the current
            selectedHidden = chHideLayer.Checked

            ' If the layer is marked hidden, disable ink collection
            inkPictVehicle.InkEnabled = Not chHideLayer.Checked

            Me.Refresh()
        Else
            ' If ink collection is enabled, the active ink cannot be changed
            ' and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden
            MessageBox.Show("Cannot change visiblity while collecting ink.")
        End If
    End If
End Sub
```




```VB
private void chHideLayer_CheckedChanged(object sender, System.EventArgs e)
{
    // Provided that the new checked hidden value is different than
    // the previous value...
    if (chHideLayer.Checked != selectedHidden) 
    {
        if (!inkPictVehicle.CollectingInk)
        {
            // Update the array indicating the visibility of each ink layer
            inkLayers[lstAnnotationLayer.SelectedIndex].Hidden = chHideLayer.Checked;

            // Set the active ink object to the selected ink
            // Note that if the current layer is not visible, empty
            // ink is used to prevent flicker.
            inkPictVehicle.InkEnabled = false;
            inkPictVehicle.Ink = chHideLayer.Checked?emptyInk:inkLayers[lstAnnotationLayer.SelectedIndex].ActiveInk;
 
            // If the layer is marked hidden, disable ink collections
            inkPictVehicle.InkEnabled = !chHideLayer.Checked;

            // Update the previous checkbox value to reflect the current
            selectedHidden = chHideLayer.Checked;

            this.Refresh();
        }
        else 
        {
            // If ink collection is enabled, the active ink cannot be changed
            // and it is necessary to restore the checkbox to its previous value.
            chHideLayer.Checked = selectedHidden;
            MessageBox.Show("Cannot change visiblity while collecting ink.");
        }
    }
}
```



## <a name="closing-the-form"></a><span data-ttu-id="321ef-146">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="321ef-146">Closing the Form</span></span>

<span data-ttu-id="321ef-147">В коде, созданном конструктором форм Windows Forms, элементы управления [InkEdit](/previous-versions/ms835842(v=msdn.10)) и [InkPicture](/previous-versions/ms583740(v=vs.100)) добавляются в список компонентов формы при инициализации формы.</span><span class="sxs-lookup"><span data-stu-id="321ef-147">In the Windows Form Designer generated code, the [InkEdit](/previous-versions/ms835842(v=msdn.10)) and [InkPicture](/previous-versions/ms583740(v=vs.100)) controls are added to the form's component list when the form is initialized.</span></span> <span data-ttu-id="321ef-148">При закрытии формы элементы управления InkEdit и InkPicture удаляются, а также другие компоненты формы методом [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) формы.</span><span class="sxs-lookup"><span data-stu-id="321ef-148">When the form closes, the InkEdit and InkPicture controls are disposed, as well as the other components of the form, by the form's [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) method.</span></span> <span data-ttu-id="321ef-149">Метод Dispose формы также удаляет объекты [рукописного ввода](/previous-versions/ms583670(v=vs.100)) , созданные для формы.</span><span class="sxs-lookup"><span data-stu-id="321ef-149">The form's Dispose method also disposes the [Ink](/previous-versions/ms583670(v=vs.100)) objects that are created for the form.</span></span>

## <a name="related-topics"></a><span data-ttu-id="321ef-150">См. также</span><span class="sxs-lookup"><span data-stu-id="321ef-150">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="321ef-151">[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="321ef-151">[Microsoft.Ink.Ink](/previous-versions/ms583670(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="321ef-152">Элемент управления InkPicture</span><span class="sxs-lookup"><span data-stu-id="321ef-152">InkPicture Control</span></span>](inkpicture-control.md)
</dt> <dt>

[<span data-ttu-id="321ef-153">Элемент управления InkEdit</span><span class="sxs-lookup"><span data-stu-id="321ef-153">InkEdit Control</span></span>](inkedit-control.md)
</dt> </dl>

 

 
