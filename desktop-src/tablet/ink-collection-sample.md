---
description: Это приложение основано на объекте InkCollector и демонстрирует сбор рукописных данных.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Образец рукописного сбора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5f568abf38abfa31d9374a7a1874f9f73481a799a740c402f3e8f168963c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718263"
---
# <a name="ink-collection-sample"></a>Образец рукописного сбора

Это приложение основано на объекте [InkCollector](/previous-versions/ms836493(v=msdn.10)) и демонстрирует сбор рукописных данных. Приложение создает окно, прикрепляет к нему объект InkCollector и предоставляет пользователю варианты меню, которые можно использовать для изменения цвета рукописного ввода, ширины рукописного ввода, включения и отключения сбора рукописных данных.

> [!Note]  
> версия, описанная в этом разделе, — Visual Basic .net. Эти понятия одинаковы для других языковых версий в библиотеке Samples.

 

## <a name="declaring-the-inkcollector"></a>Объявление InkCollector

Сначала приложение импортирует пространство имен [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) . Затем приложение объявляет `myInkCollector` , которое содержит объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) для формы.


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a>Настройка

`InkCollection_Load`Метод формы обрабатывает событие [загрузки](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы. Он создает объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) , назначенный форме, изменяет свойство [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта InkCollector и включает объект InkCollector.


```C++
Private Sub InkCollection_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load

    ' Create an ink collector and assign it to this form's window
    myInkCollector = New InkCollector(Me.Handle)

    ' Set the pen width to be a medium width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth

    ' If you do not modify the default drawing attributes, the default 
    ' drawing attributes will use the following properties and values:
    ' ...

    ' Turn the ink collector on
    myInkCollector.Enabled = True
End Sub
```



Объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) назначается окну формы путем назначения маркера окна формы свойству [Handle](/previous-versions/ms836504(v=msdn.10)) объекта InkCollector. Сбор рукописных данных включен путем установки для свойства [Enabled](/previous-versions/ms836503(v=msdn.10)) объекта InkCollector значения **true**.

Свойство [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) задает атрибуты по умолчанию, назначенные новому курсору. Чтобы задать разные атрибуты нового курсора, используйте свойство [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) объекта [cursor](/previous-versions/ms839521(v=msdn.10)) . Чтобы изменить атрибуты рисования одного штриха, используйте свойство [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) .

## <a name="changing-the-properties"></a>Изменение свойств

Остальная часть этого простого приложения состоит из обработчиков для различных вариантов меню, которые пользователь может сделать. Например, если пользователь решил изменить цвет рукописного ввода на красный, выбрав пункт красный в меню рукописный ввод, цвет изменится с помощью свойства [Color](/previous-versions/ms837933(v=msdn.10)) в свойстве [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) в обработчике событий для меню.


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a>Закрытие формы

Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
