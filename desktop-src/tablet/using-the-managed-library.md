---
description: Обзор управляемой библиотеки и заметок об использовании управляемой библиотеки платформы Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Использование управляемой библиотеки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/10/2021
ms.locfileid: "105703413"
---
# <a name="using-the-managed-library"></a><span data-ttu-id="35ca8-103">Использование управляемой библиотеки</span><span class="sxs-lookup"><span data-stu-id="35ca8-103">Using the Managed Library</span></span>

<span data-ttu-id="35ca8-104">Среда CLR является основой платформы Microsoft .NET.</span><span class="sxs-lookup"><span data-stu-id="35ca8-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="35ca8-105">Среду CLR можно считать агентом, который управляет кодом во время выполнения, предоставляя базовые службы, такие как управление памятью, управление потоками и удаленное взаимодействие, в то же время обеспечивая строгую безопасность кода.</span><span class="sxs-lookup"><span data-stu-id="35ca8-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="35ca8-106">На самом деле концепция управления кодом является фундаментальным принципом среды CLR.</span><span class="sxs-lookup"><span data-stu-id="35ca8-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="35ca8-107">Код, предназначенный для среды CLR, называется управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="35ca8-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="35ca8-108">Код, который не предназначен для среды CLR, называется машинным кодом.</span><span class="sxs-lookup"><span data-stu-id="35ca8-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="35ca8-109">Библиотека классов Framework — это исчерпывающая, объектно-ориентированная коллекция многократно используемых классов, которую можно использовать для разработки приложений от традиционных приложений командной строки или графического пользовательского интерфейса (GUI) в приложениях на основе последних нововведений, предоставляемых ASP.NET и веб-службами.</span><span class="sxs-lookup"><span data-stu-id="35ca8-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="35ca8-110">Управляемая библиотека Tablet PC содержит набор управляемых объектов, которые расширяют платформу для обеспечения поддержки ввода и вывода рукописного текста на планшетном ПК, а также обмена данными с другими компьютерами.</span><span class="sxs-lookup"><span data-stu-id="35ca8-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="35ca8-111">Исключения</span><span class="sxs-lookup"><span data-stu-id="35ca8-111">Exceptions</span></span>

<span data-ttu-id="35ca8-112">Объекты управляемой библиотеки в API-интерфейсе Tablet PC заключают реализации библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="35ca8-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="35ca8-113">Если базовый объект библиотеки COM или элемент управления возвращает ошибку, то управляемый API выдаст исключение Marshal. Сровексцептионфорхр, которое предоставляет подробные сведения о внутреннем исключении COM.</span><span class="sxs-lookup"><span data-stu-id="35ca8-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="35ca8-114">Сведения о возможных ошибках, которые могут быть возвращены, см. в справочнике по значениям HRESULT в справке библиотеки COM.</span><span class="sxs-lookup"><span data-stu-id="35ca8-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="35ca8-115">Сравнение объектов</span><span class="sxs-lookup"><span data-stu-id="35ca8-115">Object Comparison</span></span>

<span data-ttu-id="35ca8-116">Для всех объектов в управляемой библиотеке платформы Tablet PC [**Equals**](/previous-versions/windows/) не переопределяется для правильного сравнения двух одинаковых объектов.</span><span class="sxs-lookup"><span data-stu-id="35ca8-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="35ca8-117">Управляемый программный интерфейс (API) не поддерживает сравнение объектов на равенство либо с помощью функции **Equals** , либо с помощью оператора Equals (= =).</span><span class="sxs-lookup"><span data-stu-id="35ca8-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="35ca8-118">Привязка к последней Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="35ca8-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="35ca8-119">Последняя сборка Microsoft.Ink.dll является совместимой заменой для Microsoft.Ink.dll версии 1,0 и Microsoft.Ink.15.dll.</span><span class="sxs-lookup"><span data-stu-id="35ca8-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="35ca8-120">В большинстве случаев нет необходимости вносить изменения в приложения, распространяемые с более старыми сборками.</span><span class="sxs-lookup"><span data-stu-id="35ca8-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="35ca8-121">Однако в некоторых случаях необходимо указать загрузчику среды CLR использовать более новую библиотеку динамической компоновки (DLL) в любом месте, где имеются ссылки на старые библиотеки DLL.</span><span class="sxs-lookup"><span data-stu-id="35ca8-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="35ca8-122">Единственный момент, когда необходимо явно выполнить привязку к новой сборке с помощью следующей методики, — это то, что приложение использует компонент, который ссылается на сборку версии 1,0 или 1,5 в сочетании с компонентом, который ссылается на более позднюю версию сборки, например 1,7, и если эти компоненты могут обмениваться данными.</span><span class="sxs-lookup"><span data-stu-id="35ca8-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="35ca8-123">Лучшим способом указания загрузчику среды CLR использовать более новую библиотеку DLL является перенаправление версий сборки на уровне приложения.</span><span class="sxs-lookup"><span data-stu-id="35ca8-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="35ca8-124">Можно указать, что приложение будет использовать более новую версию сборки, поместив сведения о привязке сборки в файл конфигурации приложения.</span><span class="sxs-lookup"><span data-stu-id="35ca8-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="35ca8-125">Дополнительные сведения о перенаправлении версий сборок на уровне приложения см. в разделе [Перенаправление версий сборки](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), в частности раздел «Указание привязки сборки в файлах конфигурации».</span><span class="sxs-lookup"><span data-stu-id="35ca8-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="35ca8-126">Необходимо будет создать файл конфигурации в том же каталоге, что и исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="35ca8-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="35ca8-127">Файл конфигурации должен иметь имя, совпадающее с именем исполняемого файла, за которым следует расширение config.</span><span class="sxs-lookup"><span data-stu-id="35ca8-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="35ca8-128">Например, для приложения MyApp.exe файл конфигурации должен быть MyApp.exe.configным файлом.</span><span class="sxs-lookup"><span data-stu-id="35ca8-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="35ca8-129">Файл конфигурации использует элемент [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) для принудительного сопоставления всех предыдущих версий с последней версией, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="35ca8-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="35ca8-130">Дополнительные сведения о файлах конфигурации, в том числе примеры создания язык XML (XML) для файла конфигурации, см. в разделе как [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) , так и [Перенаправление версий сборки](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span><span class="sxs-lookup"><span data-stu-id="35ca8-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="35ca8-131">Приложения, созданные с помощью пакета средств разработки Microsoft Windows XP Tablet PC Edition 1,7 и более поздних версий, автоматически привязываются к новой версии сборки Microsoft. Ink.</span><span class="sxs-lookup"><span data-stu-id="35ca8-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="35ca8-132">Дополнительные сведения о привязке сборок см. [в статье Обнаружение сборок в среде выполнения](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span><span class="sxs-lookup"><span data-stu-id="35ca8-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="35ca8-133">Использование политики приложения для привязки к обновленной сборке не работает для приложений, использующих класс [разделителя](/previous-versions/ms583616(v=vs.100)) или класс [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="35ca8-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="35ca8-134">Приложения, использующие любой из этих классов, должны либо продолжать использовать Microsoft.Ink.15.dll, либо быть перекомпилированы после ссылки на обновленную сборку.</span><span class="sxs-lookup"><span data-stu-id="35ca8-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="35ca8-135">Работа с событиями</span><span class="sxs-lookup"><span data-stu-id="35ca8-135">Working with Events</span></span>

<span data-ttu-id="35ca8-136">Если код в обработчике событий для любого из управляемых объектов вызывает исключение, это исключение не доставляется пользователю.</span><span class="sxs-lookup"><span data-stu-id="35ca8-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="35ca8-137">Чтобы обеспечить доставку исключений, используйте блоки try-catch в обработчиках событий для управляемых событий.</span><span class="sxs-lookup"><span data-stu-id="35ca8-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="35ca8-138">Управление формами</span><span class="sxs-lookup"><span data-stu-id="35ca8-138">Managing Forms</span></span>

<span data-ttu-id="35ca8-139">Класс [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) и его базовые классы не определяют метод завершения.</span><span class="sxs-lookup"><span data-stu-id="35ca8-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="35ca8-140">Чтобы очистить ресурсы в форме, напишите подкласс, предоставляющий метод завершения (например, деструктор C, \# использующий ~), который вызывает [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="35ca8-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="35ca8-141">Чтобы выполнить очистку, метод завершения переопределяет Dispose, а затем вызывает метод Dispose базового класса.</span><span class="sxs-lookup"><span data-stu-id="35ca8-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="35ca8-142">Не используйте ссылки на другие объекты, требующие метода [Finalize](/previous-versions/windows/) в методе Dispose, если логический параметр имеет **значение false**, поскольку эти объекты уже могут быть завершены.</span><span class="sxs-lookup"><span data-stu-id="35ca8-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="35ca8-143">Дополнительные сведения об освобождении ресурсов см. в разделе [методы Finalize и деструкторы](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span><span class="sxs-lookup"><span data-stu-id="35ca8-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="35ca8-144">Формы и Рекогнизерконтекст</span><span class="sxs-lookup"><span data-stu-id="35ca8-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="35ca8-145">События [рекогнизерконтекст](/previous-versions/ms552546(v=vs.100)) запускаются в потоке, отличном от потока, в котором находится форма.</span><span class="sxs-lookup"><span data-stu-id="35ca8-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="35ca8-146">Элементы управления в Windows Forms привязаны к определенному потоку и не являются потокобезопасными.</span><span class="sxs-lookup"><span data-stu-id="35ca8-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="35ca8-147">Поэтому для маршалирования вызова в нужный поток необходимо использовать один из методов Invoke элемента управления.</span><span class="sxs-lookup"><span data-stu-id="35ca8-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="35ca8-148">Четыре метода элемента управления являются потокобезопасными: методы [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)и [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="35ca8-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="35ca8-149">Для всех остальных вызовов методов используйте один из этих методов Invoke при вызове из другого потока.</span><span class="sxs-lookup"><span data-stu-id="35ca8-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="35ca8-150">Дополнительные сведения об использовании этих методов см. в разделе [Управление элементами управления из потоков](/previous-versions/757y83z4(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="35ca8-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="35ca8-151">Ожидание событий</span><span class="sxs-lookup"><span data-stu-id="35ca8-151">Waiting for Events</span></span>

<span data-ttu-id="35ca8-152">Среда планшетного ПК является многопоточной.</span><span class="sxs-lookup"><span data-stu-id="35ca8-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="35ca8-153">Используйте функцию [**коваитформултиплехандлес**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) вместо других методов ожидания, чтобы разрешить повторное использование вызовов модели COM для входа в многопоточное подразделение (MTA), пока приложение ожидает события.</span><span class="sxs-lookup"><span data-stu-id="35ca8-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="35ca8-154">Использование коллекций рукописных штрихов</span><span class="sxs-lookup"><span data-stu-id="35ca8-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="35ca8-155">Экземпляры коллекций [штрихов](/previous-versions/ms552701(v=vs.100)) , полученных из объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , не собираются сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="35ca8-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="35ca8-156">Чтобы избежать утечки памяти, в любой момент, когда вы работаете с одной из этих коллекций, используйте оператор using, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="35ca8-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="35ca8-157">Удаление управляемых объектов и элементов управления</span><span class="sxs-lookup"><span data-stu-id="35ca8-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="35ca8-158">Чтобы избежать утечки памяти, необходимо явно вызвать метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) для любого объекта или элемента управления Tablet PC, к которому был присоединен обработчик событий до того, как объект или элемент управления выходит из области действия.</span><span class="sxs-lookup"><span data-stu-id="35ca8-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="35ca8-159">Чтобы повысить производительность приложения, вручную избавиться от следующих объектов, элементов управления и коллекций, когда они больше не нужны.</span><span class="sxs-lookup"><span data-stu-id="35ca8-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="35ca8-160">[Разделитель](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="35ca8-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="35ca8-161">[Рукописный ввод](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="35ca8-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="35ca8-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="35ca8-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="35ca8-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="35ca8-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="35ca8-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="35ca8-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="35ca8-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="35ca8-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="35ca8-166">[пенинпутпанел](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="35ca8-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="35ca8-167">[рекогнизерконтекст](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="35ca8-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="35ca8-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="35ca8-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="35ca8-169">В следующем примере на языке C \# демонстрируются некоторые сценарии, в которых используется метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="35ca8-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 