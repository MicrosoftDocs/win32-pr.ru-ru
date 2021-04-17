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
# <a name="using-the-managed-library"></a>Использование управляемой библиотеки

Среда CLR является основой платформы Microsoft .NET. Среду CLR можно считать агентом, который управляет кодом во время выполнения, предоставляя базовые службы, такие как управление памятью, управление потоками и удаленное взаимодействие, в то же время обеспечивая строгую безопасность кода. На самом деле концепция управления кодом является фундаментальным принципом среды CLR. Код, предназначенный для среды CLR, называется управляемым кодом. Код, который не предназначен для среды CLR, называется машинным кодом.

Библиотека классов Framework — это исчерпывающая, объектно-ориентированная коллекция многократно используемых классов, которую можно использовать для разработки приложений от традиционных приложений командной строки или графического пользовательского интерфейса (GUI) в приложениях на основе последних нововведений, предоставляемых ASP.NET и веб-службами.

Управляемая библиотека Tablet PC содержит набор управляемых объектов, которые расширяют платформу для обеспечения поддержки ввода и вывода рукописного текста на планшетном ПК, а также обмена данными с другими компьютерами.

## <a name="exceptions"></a>Исключения

Объекты управляемой библиотеки в API-интерфейсе Tablet PC заключают реализации библиотеки COM. Если базовый объект библиотеки COM или элемент управления возвращает ошибку, то управляемый API выдаст исключение Marshal. Сровексцептионфорхр, которое предоставляет подробные сведения о внутреннем исключении COM. Сведения о возможных ошибках, которые могут быть возвращены, см. в справочнике по значениям HRESULT в справке библиотеки COM.

## <a name="object-comparison"></a>Сравнение объектов

Для всех объектов в управляемой библиотеке платформы Tablet PC [**Equals**](/previous-versions/windows/) не переопределяется для правильного сравнения двух одинаковых объектов. Управляемый программный интерфейс (API) не поддерживает сравнение объектов на равенство либо с помощью функции **Equals** , либо с помощью оператора Equals (= =).

## <a name="binding-to-the-latest-microsoftinkdll"></a>Привязка к последней Microsoft.Ink.dll

Последняя сборка Microsoft.Ink.dll является совместимой заменой для Microsoft.Ink.dll версии 1,0 и Microsoft.Ink.15.dll. В большинстве случаев нет необходимости вносить изменения в приложения, распространяемые с более старыми сборками. Однако в некоторых случаях необходимо указать загрузчику среды CLR использовать более новую библиотеку динамической компоновки (DLL) в любом месте, где имеются ссылки на старые библиотеки DLL.

Единственный момент, когда необходимо явно выполнить привязку к новой сборке с помощью следующей методики, — это то, что приложение использует компонент, который ссылается на сборку версии 1,0 или 1,5 в сочетании с компонентом, который ссылается на более позднюю версию сборки, например 1,7, и если эти компоненты могут обмениваться данными.

Лучшим способом указания загрузчику среды CLR использовать более новую библиотеку DLL является перенаправление версий сборки на уровне приложения. Можно указать, что приложение будет использовать более новую версию сборки, поместив сведения о привязке сборки в файл конфигурации приложения. Дополнительные сведения о перенаправлении версий сборок на уровне приложения см. в разделе [Перенаправление версий сборки](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), в частности раздел «Указание привязки сборки в файлах конфигурации».

Необходимо будет создать файл конфигурации в том же каталоге, что и исполняемый файл. Файл конфигурации должен иметь имя, совпадающее с именем исполняемого файла, за которым следует расширение config. Например, для приложения MyApp.exe файл конфигурации должен быть MyApp.exe.configным файлом. Файл конфигурации использует элемент [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) для принудительного сопоставления всех предыдущих версий с последней версией, как показано в следующем примере:

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

Дополнительные сведения о файлах конфигурации, в том числе примеры создания язык XML (XML) для файла конфигурации, см. в разделе как [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) , так и [Перенаправление версий сборки](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).

Приложения, созданные с помощью пакета средств разработки Microsoft Windows XP Tablet PC Edition 1,7 и более поздних версий, автоматически привязываются к новой версии сборки Microsoft. Ink. Дополнительные сведения о привязке сборок см. [в статье Обнаружение сборок в среде выполнения](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).

> [!Note]  
> Использование политики приложения для привязки к обновленной сборке не работает для приложений, использующих класс [разделителя](/previous-versions/ms583616(v=vs.100)) или класс [пенинпутпанел](/previous-versions/aa514041(v=msdn.10)) . Приложения, использующие любой из этих классов, должны либо продолжать использовать Microsoft.Ink.15.dll, либо быть перекомпилированы после ссылки на обновленную сборку.

 

## <a name="working-with-events"></a>Работа с событиями

Если код в обработчике событий для любого из управляемых объектов вызывает исключение, это исключение не доставляется пользователю. Чтобы обеспечить доставку исключений, используйте блоки try-catch в обработчиках событий для управляемых событий.

## <a name="managing-forms"></a>Управление формами

Класс [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) и его базовые классы не определяют метод завершения. Чтобы очистить ресурсы в форме, напишите подкласс, предоставляющий метод завершения (например, деструктор C, \# использующий ~), который вызывает [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1). Чтобы выполнить очистку, метод завершения переопределяет Dispose, а затем вызывает метод Dispose базового класса. Не используйте ссылки на другие объекты, требующие метода [Finalize](/previous-versions/windows/) в методе Dispose, если логический параметр имеет **значение false**, поскольку эти объекты уже могут быть завершены. Дополнительные сведения об освобождении ресурсов см. в разделе [методы Finalize и деструкторы](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).

## <a name="forms-and-the-recognizercontext"></a>Формы и Рекогнизерконтекст

События [рекогнизерконтекст](/previous-versions/ms552546(v=vs.100)) запускаются в потоке, отличном от потока, в котором находится форма. Элементы управления в Windows Forms привязаны к определенному потоку и не являются потокобезопасными. Поэтому для маршалирования вызова в нужный поток необходимо использовать один из методов Invoke элемента управления. Четыре метода элемента управления являются потокобезопасными: методы [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)и [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) . Для всех остальных вызовов методов используйте один из этих методов Invoke при вызове из другого потока. Дополнительные сведения об использовании этих методов см. в разделе [Управление элементами управления из потоков](/previous-versions/757y83z4(v=vs.140)).

## <a name="waiting-for-events"></a>Ожидание событий

Среда планшетного ПК является многопоточной. Используйте функцию [**коваитформултиплехандлес**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) вместо других методов ожидания, чтобы разрешить повторное использование вызовов модели COM для входа в многопоточное подразделение (MTA), пока приложение ожидает события.

## <a name="using-ink-strokes-collections"></a>Использование коллекций рукописных штрихов

Экземпляры коллекций [штрихов](/previous-versions/ms552701(v=vs.100)) , полученных из объекта [рукописного ввода](/previous-versions/aa515768(v=msdn.10)) , не собираются сборщиком мусора. Чтобы избежать утечки памяти, в любой момент, когда вы работаете с одной из этих коллекций, используйте оператор using, как показано ниже.


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a>Удаление управляемых объектов и элементов управления

Чтобы избежать утечки памяти, необходимо явно вызвать метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) для любого объекта или элемента управления Tablet PC, к которому был присоединен обработчик событий до того, как объект или элемент управления выходит из области действия.

Чтобы повысить производительность приложения, вручную избавиться от следующих объектов, элементов управления и коллекций, когда они больше не нужны.

-   [Разделитель](/previous-versions/ms583616(v=vs.100))
-   [Рукописный ввод](/previous-versions/aa515768(v=msdn.10))
-   [InkCollector](/previous-versions/ms583683(v=vs.100))
-   [InkEdit](/previous-versions/ms552265(v=vs.100))
-   [InkOverlay](/previous-versions/ms552322(v=vs.100))
-   [InkPicture](/previous-versions/aa514604(v=msdn.10))
-   [пенинпутпанел](/previous-versions/aa514041(v=msdn.10))
-   [рекогнизерконтекст](/previous-versions/ms552546(v=vs.100))
-   [Strokes](/previous-versions/ms552701(v=vs.100))

В следующем примере на языке C \# демонстрируются некоторые сценарии, в которых используется метод [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) .


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



 

 