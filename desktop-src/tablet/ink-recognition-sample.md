---
description: Это приложение демонстрирует создание приложения для распознавания рукописного текста. Пакет SDK для Windows Vista также предоставляет версии этого примера на C \# и Visual Basic .NET.
ms.assetid: 4b3fc078-731e-4263-8e95-2c273d69a457
title: Пример распознавания рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d97d9d15ef64a3d7a1fe1fc5d45b3cb0454ba7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263035"
---
# <a name="ink-recognition-sample"></a>Пример распознавания рукописного ввода

Это приложение демонстрирует создание приложения для распознавания рукописного текста. Пакет SDK для Windows Vista также предоставляет версии этого примера на C \# и Visual Basic .NET. Этот раздел относится к примеру Visual Basic .NET, но основные понятия одинаковы для разных версий.

## <a name="access-the-tablet-pc-interfaces"></a>Доступ к интерфейсам планшетных ПК

Сначала необходимо создать ссылку на API-интерфейс Tablet PC, который устанавливается вместе с пакетом SDK.


```VB
' The Ink namespace, which contains the Tablet PC Platform API
Imports Microsoft.Ink
```



## <a name="initialize-the-inkcollector"></a>Инициализация InkCollector

Пример добавляет код в обработчик событий [загрузки](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы, который служит для связывания объекта [InkCollector](/previous-versions/ms583683(v=vs.100)), минкколлектор с окном группы и включения объекта InkCollector.


```VB
Private Sub InkRecognition_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

   ' Create the recognizers collection
    myRecognizers = New Recognizers()

    ' Create an ink collector that uses the group box handle
    myInkCollector = New InkCollector(gbInkArea.Handle)

    ' Turn the ink collector on
    myInkCollector.Enabled = True

End Sub
```



## <a name="recognize-the-strokes"></a>Распознать штрихи

Обработчик событий [Click](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) объекта [Button](/dotnet/api/system.windows.forms.button?view=netcore-3.1) выполняет проверку, чтобы убедиться, что у пользователя установлен хотя бы один распознаватель, проверив свойство [Count](/previous-versions/ms828521(v=msdn.10)) коллекции [распознавателей](/previous-versions/ms828520(v=msdn.10)) .

Свойство [селектедтекст](/previous-versions/windows/) текстового поля устанавливается в соответствии с наилучшим соответствием для штрихов, использующих метод [ToString](/previous-versions/ms827836(v=msdn.10)) в коллекции [штрихов](/previous-versions/ms552701(v=vs.100)) . После распознавания штрихов они удаляются. Наконец, код заставляет перекрасить область рисования, сняв ее для дальнейшего использования рукописного ввода.


```VB
Private Sub btnRecognize_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles btnRecognize.Click

    ' Check to ensure that the user has at least one recognizer installed
    ' Note that this is a preventive check - otherwise, an exception 
    ' occurs during recognition
    If 0 = myRecognizers.Count Then
        MessageBox.Show("There are no handwriting recognizers installed.  You need to have at least one in order to run this sample.")
    Else
        ' ...
        txtResults.SelectedText = myInkCollector.Ink.Strokes.ToString

        ' If the mouse is pressed, do not perform the recognition -
        ' this prevents deleting a stroke that is still being drawn
        If Not myInkCollector.CollectingInk Then

            ' Delete the ink from the ink collector
            myInkCollector.Ink.DeleteStrokes(myInkCollector.Ink.Strokes)

            ' Force the Frame to redraw (so the deleted ink goes away)
            gbInkArea.Refresh()

        End If
    End If
End Sub
```



## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
