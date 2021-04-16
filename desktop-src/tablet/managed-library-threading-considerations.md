---
description: Следующие вопросы о потоках для планшетных ПК относятся к управляемой библиотеке.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Рекомендации по потокам управляемых библиотек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702593"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="57892-103">Рекомендации по потокам управляемых библиотек</span><span class="sxs-lookup"><span data-stu-id="57892-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="57892-104">Следующие вопросы о потоках для планшетных ПК относятся к управляемой библиотеке.</span><span class="sxs-lookup"><span data-stu-id="57892-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="57892-105">Безопасность потоков</span><span class="sxs-lookup"><span data-stu-id="57892-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="57892-106">Приложения STA и MTA</span><span class="sxs-lookup"><span data-stu-id="57892-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="57892-107">Windows Forms вопросы о потоках</span><span class="sxs-lookup"><span data-stu-id="57892-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="57892-108">Рекомендации по буферу обмена</span><span class="sxs-lookup"><span data-stu-id="57892-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="57892-109">Исключения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="57892-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="57892-110">Удаление объектов и элементов управления</span><span class="sxs-lookup"><span data-stu-id="57892-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="57892-111">API-интерфейсы Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="57892-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="57892-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="57892-112">Thread-Safety</span></span>

<span data-ttu-id="57892-113">Классы управляемых библиотек платформы планшетных ПК обычно не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="57892-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="57892-114">Следующие коллекции являются потокобезопасными на уровне членов. Однако эти коллекции не гарантируют, что перечислитель защищен, если другой поток одновременно работает с коллекцией:</span><span class="sxs-lookup"><span data-stu-id="57892-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="57892-115">[курсорбуттонс](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="57892-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="57892-116">[Курсоры](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="57892-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="57892-117">[дивисионунитс](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="57892-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="57892-118">[рекогнитионалтернатес](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="57892-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="57892-119">[Распознаватели](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="57892-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="57892-120">[Планшеты](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="57892-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="57892-121">Приложения STA и MTA</span><span class="sxs-lookup"><span data-stu-id="57892-121">STA and MTA Applications</span></span>

<span data-ttu-id="57892-122">Управляемые приложения, созданные с помощью мастеров, содержащихся в Microsoft Visual Studio .NET, по умолчанию являются однопотоковыми апартаментами (STA).</span><span class="sxs-lookup"><span data-stu-id="57892-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="57892-123">Вы можете изменить подразделение приложения, задав для потока STA или атрибута потока многопотокового подразделения (MTA) точку входа приложения.</span><span class="sxs-lookup"><span data-stu-id="57892-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="57892-124">Если приложение выполняется в MTA, необходимо написать потокобезопасный код. Тем не менее, это позволяет повысить производительность обработки определенных событий.</span><span class="sxs-lookup"><span data-stu-id="57892-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="57892-125">Дополнительные сведения об атрибутах потоков STA и MTA см. в разделе класс [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) и класс [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="57892-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="57892-126">Windows Forms вопросы о потоках</span><span class="sxs-lookup"><span data-stu-id="57892-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="57892-127">Элементы управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) и [InkEdit](/previous-versions/ms552265(v=vs.100)) расширяют элементы управления Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="57892-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="57892-128">Windows Forms элементы управления используют модель однопотокового подразделения (STA), поскольку Windows Forms основаны на собственных окнах Win32, которые по сути являются отдельными потоками.</span><span class="sxs-lookup"><span data-stu-id="57892-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="57892-129">В управляемом коде элементы управления рукописного ввода должны создаваться в том же потоке, что и основной поток для формы.</span><span class="sxs-lookup"><span data-stu-id="57892-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="57892-130">В приложении STA определенные события происходят в потоке, отличном от потока пользовательского интерфейса приложения.</span><span class="sxs-lookup"><span data-stu-id="57892-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="57892-131">При вызове любого Windows Forms объекта или элемента управления, включая элементы управления [InkPicture](/previous-versions/aa514604(v=msdn.10)) и [InkEdit](/previous-versions/ms552265(v=vs.100)) , из обработчика событий планшетного ПК используйте наследуемый метод [Control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) объекта или элемента управления.</span><span class="sxs-lookup"><span data-stu-id="57892-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="57892-132">Свойство [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , унаследованное от класса Control, может использоваться для определения необходимости.</span><span class="sxs-lookup"><span data-stu-id="57892-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="57892-133">Например, в следующем обработчике события для события [распознавания](/previous-versions/ms829424(v=msdn.10)) проверяется свойство [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , а при **значении true** обработчик событий вызывается повторно из потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="57892-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="57892-134">Если вы поместили элемент [управления UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) на авебпажеин браузере (см. раздел [веб-элементы управления](web-controls.md)), он выполняется как приложение STA.</span><span class="sxs-lookup"><span data-stu-id="57892-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="57892-135">Для интеллектуальных клиентских приложений (см. раздел [без сенсорного развертывания](no-touch-deployment.md)) разработчик имеет полный контроль над [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="57892-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="57892-136">(По умолчанию обычно используется STA, но в зависимости от используемой версии среды CLR это может быть MTA.) О проблемах с потоками, связанных с [**RealTimeStylus**](realtimestylus-class.md), см. [в разделе вопросы многопоточности для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="57892-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="57892-137">Дополнительные сведения о вызове Windows Forms из приложения MTA см. в разделе [Пример многопоточного Windows Forms управления](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="57892-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="57892-138">Рекомендации по буферу обмена</span><span class="sxs-lookup"><span data-stu-id="57892-138">Clipboard Considerations</span></span>

<span data-ttu-id="57892-139">Объект [Clipboard](../dataxchg/clipboard.md) работает только из потока STA.</span><span class="sxs-lookup"><span data-stu-id="57892-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="57892-140">При попытке скопировать или вставить из буфера обмена из потока, который не является STA, вы получаете [среадстатиксцептион](/previous-versions/windows/).</span><span class="sxs-lookup"><span data-stu-id="57892-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="57892-141">Если приложение является MTA, создайте поток STA для обработки вызовов методов буфера обмена и некоторых других аспектов пользовательского интерфейса приложения.</span><span class="sxs-lookup"><span data-stu-id="57892-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="57892-142">Исключения в обработчиках событий</span><span class="sxs-lookup"><span data-stu-id="57892-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="57892-143">Исключения не могут быть вызваны в обработчиках событий планшетных ПК.</span><span class="sxs-lookup"><span data-stu-id="57892-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="57892-144">Например, если делегат обработчика событий для объекта или коллекции Tablet PC имеет три зарегистрированных обработчика, а первый — исключение, то происходит следующая последовательность.</span><span class="sxs-lookup"><span data-stu-id="57892-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="57892-145">Первый обработчик завершает работу.</span><span class="sxs-lookup"><span data-stu-id="57892-145">The first handler exits.</span></span>
2.  <span data-ttu-id="57892-146">Исключение потеряно.</span><span class="sxs-lookup"><span data-stu-id="57892-146">The exception is lost.</span></span>
3.  <span data-ttu-id="57892-147">Остальные обработчики не вызываются.</span><span class="sxs-lookup"><span data-stu-id="57892-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="57892-148">Удаление объектов и элементов управления</span><span class="sxs-lookup"><span data-stu-id="57892-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="57892-149">Чтобы избежать утечки памяти, необходимо явно вызвать метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) для любого объекта или элемента управления Tablet PC, к которому был присоединен обработчик событий до того, как объект или элемент управления выходит из области действия.</span><span class="sxs-lookup"><span data-stu-id="57892-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="57892-150">Чтобы повысить производительность приложения, вручную удалите любой объект или элемент управления Tablet PC, реализующий метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) , когда объект или элемент управления больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="57892-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="57892-151">API-интерфейсы Стилусинпут</span><span class="sxs-lookup"><span data-stu-id="57892-151">StylusInput APIs</span></span>

<span data-ttu-id="57892-152">Дополнительные сведения о создании потоков для объекта [**RealTimeStylus**](realtimestylus-class.md) и интерфейсов прикладного программирования (API) стилусинпут см. [в статье вопросы использования потоков для интерфейсов API стилусинпут](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="57892-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
