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
# <a name="auto-claims-form-sample"></a>Пример формы Auto Claims

В примере Auto Claims рассматривается гипотетический сценарий для страхового полиса. Для работы по оценке необходимо, чтобы он был посещен клиентами дома или бизнеса и вводил свои сведения о заявках в форму. Чтобы повысить продуктивность оценки, ИТ-отдел разрабатывает приложение для планшетов, которое позволяет ему быстро и точно вводить сведения о заявках с помощью двух элементов управления рукописного ввода: [InkEdit](/previous-versions/ms835842(v=msdn.10)) и [InkPicture](/previous-versions/ms583740(v=vs.100)) .

В этом примере для каждого текстового поля ввода используется элемент управления [InkEdit](/previous-versions/ms835842(v=msdn.10)) . Пользователь вводит соответствующую информацию о страховой полисе и транспорте в эти поля с помощью пера. Элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) используется для добавления рукописного ввода в изображение автомобиля для выделения поврежденных областей автомобиля. Образец Auto Claims доступен для C \# и Microsoft Visual Basic .NET. В этом разделе описывается Visual Basic .NET.

Класс автозаявок определяется как подкласс [System. Windows. Forms. Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) , а вложенный класс определяется для создания и управления уровнями рукописного ввода для различных типов повреждений. Для выполнения следующих задач определены четыре обработчика событий:

-   Инициализация формы и слоев рукописного ввода.
-   Перерисовка элемента управления [InkPicture](/previous-versions/ms583740(v=vs.100)) .
-   Выбор слоя рукописного ввода с помощью списка.
-   Изменение видимости слоя рукописного ввода.

> [!Note]  
> Версии этого образца доступны в C \# и Visual Basic .NET. Версия, описанная в этом разделе, — Visual Basic .NET. Эти понятия одинаковы для разных версий.

 

## <a name="defining-the-form-and-ink-layers"></a>Определение формы и слоев рукописного ввода

Необходимо импортировать пространство имен [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) :


```VB
Imports Microsoft.Ink
```




```VB
// The Ink namespace, which contains the Tablet PC Platform API
using Microsoft.Ink;
```



Затем в классе автозаявок определяется вложенный `InkLayer` класс и объявляется массив из четырех `InkLayer` объектов. (Инклайер содержит объект [Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100)) для хранения рукописных данных, а также значения [System. Drawing. Color](/dotnet/api/system.drawing.color?view=netcore-3.1) и **Boolean** для сохранения цвета и скрытого состояния слоя.) Пятый объект рукописного ввода объявляется для обработки рукописного ввода [, когда все](/previous-versions/ms583740(v=vs.100)) слои рукописного ввода скрыты.


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



Каждый слой имеет собственный объект [рукописного ввода](/previous-versions/ms583670(v=vs.100)) . В форме заявки (текст, Windows, завершение и фары) имеется четыре дискретных области, поэтому используются четыре объекта Инклайер. Пользователь может просматривать любое сочетание слоев одновременно.

## <a name="initializing-the-form-and-ink-layers"></a>Инициализация формы и слоев рукописного ввода

`Load`Обработчик событий инициализирует объект [рукописного ввода](/previous-versions/ms583670(v=vs.100)) и четыре `InkLayer` объекта.


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



Затем выберите первую запись (текст) в поле со списком.


```VB
' By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0
```




```VB
// By default, select the first ink layer
lstAnnotationLayer.SelectedIndex = 0;
```



Наконец, установите цвет рукописного ввода для элемента управления [InkPicture](/previous-versions/ms583740(v=vs.100)) на выбранную в текущий момент запись в поле со списком.


```VB
inkPictVehicle.DefaultDrawingAttributes.Color =
      inkLayers(lstAnnotationLayer.SelectedIndex).ActiveColor
```




```VB
inkPictVehicle.DefaultDrawingAttributes.Color = inkLayers[lstAnnotationLayer.SelectedIndex].ActiveColor;
```



## <a name="redrawing-the-inkpicture-control"></a>Перерисовка элемента управления InkPicture

В наследуемом обработчике событий [рисования](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) элемента управления [InkPicture](/previous-versions/ms583740(v=vs.100)) слои рукописного ввода проверяются, чтобы определить, какие из них скрыты. Если слой не скрыт, процедура события отображает его с помощью метода [Draw](/previous-versions/ms828488(v=msdn.10)) свойства средства [визуализации](/previous-versions/ms582196(v=vs.100)) . Если взглянуть на обозреватель объектов, вы увидите, что свойство Microsoft. Ink. InkPicture. Render определено как объект [Microsoft. Ink. Render](/previous-versions/ms828481(v=msdn.10)) :


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



## <a name="selecting-an-ink-layer-through-the-list-box"></a>Выбор слоя рукописного ввода с помощью списка

Когда пользователь выбирает элемент в списке, [обработчик событий в](/dotnet/api/system.windows.forms.listbox.selectedindexchanged?view=netcore-3.1) начале проверяет, что выделение изменилось и элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) в настоящее время не собирает рукописный ввод. Затем он устанавливает цвет чернил элемента управления InkPicture на соответствующий цвет для выбранного слоя рукописного ввода. Кроме того, он обновляет флажок скрыть слой, чтобы отразить состояние выбранного слоя рукописного ввода. Наконец, наследуемый метод [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) элемента управления InkPicture используется для вывода только нужных слоев внутри элемента управления.


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



## <a name="changing-the-visibility-of-an-ink-layer"></a>Изменение видимости слоя рукописного ввода

`CheckedChanged`Обработчик событий сначала проверяет, что выделение изменилось и элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) в настоящее время не собирает рукописный ввод. Затем он обновляет скрытое состояние выбранного слоя рукописного ввода, устанавливает Инкенаблед элемента управления InkPicture в **значение false**,.

Далее, перед обновлением свойства рукописного ввода свойство Инкенаблед элемента управления InkPicture имеет значение **false** .

Наконец, элемент управления [InkPicture](/previous-versions/ms583740(v=vs.100)) либо включен, либо отключен для определенной части автомобиля в зависимости от того, установлен ли флажок скрыть слой, а метод [обновления](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) элемента управления InkPicture используется для отображения только нужных слоев внутри элемента управления.


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



## <a name="closing-the-form"></a>Закрытие формы

В коде, созданном конструктором форм Windows Forms, элементы управления [InkEdit](/previous-versions/ms835842(v=msdn.10)) и [InkPicture](/previous-versions/ms583740(v=vs.100)) добавляются в список компонентов формы при инициализации формы. При закрытии формы элементы управления InkEdit и InkPicture удаляются, а также другие компоненты формы методом [Dispose](/previous-versions/dotnet/netframework-3.5/ms571303(v=vs.90)) формы. Метод Dispose формы также удаляет объекты [рукописного ввода](/previous-versions/ms583670(v=vs.100)) , созданные для формы.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Microsoft. Ink. Ink](/previous-versions/ms583670(v=vs.100))
</dt> <dt>

[Элемент управления InkPicture](inkpicture-control.md)
</dt> <dt>

[Элемент управления InkEdit](inkedit-control.md)
</dt> </dl>

 

 
