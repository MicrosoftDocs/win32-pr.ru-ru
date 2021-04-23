---
description: Это приложение основано на объекте InkCollector и демонстрирует сбор рукописных данных.
ms.assetid: e799fb16-5a1e-4d57-a033-554f72e2e685
title: Образец рукописного сбора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f31ce83a55b6f352d76ad1cb8d184b41618c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144770"
---
# <a name="ink-collection-sample"></a><span data-ttu-id="de245-103">Образец рукописного сбора</span><span class="sxs-lookup"><span data-stu-id="de245-103">Ink Collection Sample</span></span>

<span data-ttu-id="de245-104">Это приложение основано на объекте [InkCollector](/previous-versions/ms836493(v=msdn.10)) и демонстрирует сбор рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="de245-104">This application is based on the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object and demonstrates the collection of ink.</span></span> <span data-ttu-id="de245-105">Приложение создает окно, прикрепляет к нему объект InkCollector и предоставляет пользователю варианты меню, которые можно использовать для изменения цвета рукописного ввода, ширины рукописного ввода, включения и отключения сбора рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="de245-105">The application creates a window, attaches an InkCollector object to it, and provides the user with menu choices that can be used to change the ink color, the ink width, and enable and disable ink collection.</span></span>

> [!Note]  
> <span data-ttu-id="de245-106">Версия, описанная в этом разделе, — Visual Basic .NET.</span><span class="sxs-lookup"><span data-stu-id="de245-106">The version discussed in this section is Visual Basic .NET.</span></span> <span data-ttu-id="de245-107">Эти понятия одинаковы для других языковых версий в библиотеке Samples.</span><span class="sxs-lookup"><span data-stu-id="de245-107">The concepts are the same between other language versions in the samples library.</span></span>

 

## <a name="declaring-the-inkcollector"></a><span data-ttu-id="de245-108">Объявление InkCollector</span><span class="sxs-lookup"><span data-stu-id="de245-108">Declaring the InkCollector</span></span>

<span data-ttu-id="de245-109">Сначала приложение импортирует пространство имен [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="de245-109">The application first imports the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)) namespace.</span></span> <span data-ttu-id="de245-110">Затем приложение объявляет `myInkCollector` , которое содержит объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) для формы.</span><span class="sxs-lookup"><span data-stu-id="de245-110">Then, the application declares `myInkCollector`, which holds the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the form.</span></span>


```C++
' The Ink namespace, which contains the Tablet PC Platform APIImports Microsoft.Ink
...
Public Class InkCollection
   Inherits Form
    ' Declare the Ink Collector object
    Private myInkCollector
```



## <a name="setting-things-up"></a><span data-ttu-id="de245-111">Настройка</span><span class="sxs-lookup"><span data-stu-id="de245-111">Setting Things Up</span></span>

<span data-ttu-id="de245-112">`InkCollection_Load`Метод формы обрабатывает событие [загрузки](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) формы.</span><span class="sxs-lookup"><span data-stu-id="de245-112">The form's `InkCollection_Load` method handles the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event.</span></span> <span data-ttu-id="de245-113">Он создает объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) , назначенный форме, изменяет свойство [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта InkCollector и включает объект InkCollector.</span><span class="sxs-lookup"><span data-stu-id="de245-113">It creates a [InkCollector](/previous-versions/ms836493(v=msdn.10)) object assigned to the form modifies the [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property of the InkCollector object and enables the InkCollector object.</span></span>


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



<span data-ttu-id="de245-114">Объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) назначается окну формы путем назначения маркера окна формы свойству [Handle](/previous-versions/ms836504(v=msdn.10)) объекта InkCollector.</span><span class="sxs-lookup"><span data-stu-id="de245-114">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) is assigned to the form's window by assigning the form's window handle to the InkCollector object's [Handle](/previous-versions/ms836504(v=msdn.10)) property.</span></span> <span data-ttu-id="de245-115">Сбор рукописных данных включен путем установки для свойства [Enabled](/previous-versions/ms836503(v=msdn.10)) объекта InkCollector значения **true**.</span><span class="sxs-lookup"><span data-stu-id="de245-115">Ink collection is turned on by setting the InkCollector object's [Enabled](/previous-versions/ms836503(v=msdn.10)) property to **TRUE**.</span></span>

<span data-ttu-id="de245-116">Свойство [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) задает атрибуты по умолчанию, назначенные новому курсору.</span><span class="sxs-lookup"><span data-stu-id="de245-116">The [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property sets the default attributes that are assigned to a new cursor.</span></span> <span data-ttu-id="de245-117">Чтобы задать разные атрибуты нового курсора, используйте свойство [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) объекта [cursor](/previous-versions/ms839521(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="de245-117">To set different attributes on a new cursor, use the [DrawingAttributes](/previous-versions/ms839523(v=msdn.10)) property of the [Cursor](/previous-versions/ms839521(v=msdn.10)) object.</span></span> <span data-ttu-id="de245-118">Чтобы изменить атрибуты рисования одного штриха, используйте свойство [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) объекта [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="de245-118">To change the drawing attributes of a single stroke, use the [DrawingAttributes](/previous-versions/ms827846(v=msdn.10)) property of the [Stroke](/previous-versions/ms827842(v=msdn.10)) object.</span></span>

## <a name="changing-the-properties"></a><span data-ttu-id="de245-119">Изменение свойств</span><span class="sxs-lookup"><span data-stu-id="de245-119">Changing the Properties</span></span>

<span data-ttu-id="de245-120">Остальная часть этого простого приложения состоит из обработчиков для различных вариантов меню, которые пользователь может сделать.</span><span class="sxs-lookup"><span data-stu-id="de245-120">The rest of this simple application consists of handlers for the various menu selections the user can make.</span></span> <span data-ttu-id="de245-121">Например, если пользователь решил изменить цвет рукописного ввода на красный, выбрав пункт красный в меню рукописный ввод, цвет изменится с помощью свойства [Color](/previous-versions/ms837933(v=msdn.10)) в свойстве [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) объекта [InkCollector](/previous-versions/ms836493(v=msdn.10)) в обработчике событий для меню.</span><span class="sxs-lookup"><span data-stu-id="de245-121">For example, when the user chooses to change the ink color to red by selecting Red from the Ink menu, the color is changed using the [Color](/previous-versions/ms837933(v=msdn.10)) property on [InkCollector](/previous-versions/ms836493(v=msdn.10)) object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property in the event handler for the menu.</span></span>


```C++
Private Sub miRed_Click(ByVal sender As System.Object, 
                        ByVal e As System.EventArgs) Handles miRed.Click
    myInkCollector.DefaultDrawingAttributes.Color = Color.Red
End Sub
```



## <a name="closing-the-form"></a><span data-ttu-id="de245-122">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="de245-122">Closing the Form</span></span>

<span data-ttu-id="de245-123">Метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) удаляет объект [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="de245-123">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
