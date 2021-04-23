---
title: Создание приложения для ленты
description: Платформа Windows Ribbon состоит из двух отдельных, но зависимых платформ разработки языка разметки, основанного на XAML (XAML) для объявления элементов управления и их визуального макета, а также набора интерфейсов на основе модели компонентов C++ (COM) для определения функциональных возможностей команд и обработчиков приложений. Эта часть работы в архитектуре ленты Ribbon требует, чтобы разработчик, желающий воспользоваться преимуществами возможностей пользовательского интерфейса, предоставляемый платформой, должен разработать и описать пользовательский интерфейс в разметке, а затем использовать интерфейсы COM платформы Ribbon для подключения платформы к ведущему приложению.
ms.assetid: 1bd3dbb5-822b-4551-8330-8b202a4cecdf
keywords:
- Лента Windows, создание приложений
- Лента, создание приложений
- Лента Windows, план
- Лента, план
- Лента Windows, разметка
- Лента, разметка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a10f683c7fbb07b9992e418a4c09dc9aecba280
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413385"
---
# <a name="creating-a-ribbon-application"></a><span data-ttu-id="7f40a-110">Создание приложения для ленты</span><span class="sxs-lookup"><span data-stu-id="7f40a-110">Creating a Ribbon Application</span></span>

<span data-ttu-id="7f40a-111">Платформа Windows Ribbon состоит из двух отдельных, но зависимых платформ разработки: языка разметки на основе XAML (XAML) для объявления элементов управления и их визуального макета, а также набора интерфейсов на основе модели компонентов C++ для определения функциональных возможностей команд и обработчиков приложений.</span><span class="sxs-lookup"><span data-stu-id="7f40a-111">The Windows Ribbon framework is composed of two distinct, yet dependent, development platforms: a markup language based on Extensible Application Markup Language (XAML) to declare controls and their visual layout, and a C++ Component Object Model (COM)-based set of interfaces to define command functionality and application hooks.</span></span> <span data-ttu-id="7f40a-112">Эта часть работы в архитектуре ленты Ribbon требует, чтобы разработчик, желающий воспользоваться преимуществами возможностей пользовательского интерфейса, предоставляемый платформой, должен разработать и описать пользовательский интерфейс в разметке, а затем использовать интерфейсы COM платформы Ribbon для подключения платформы к ведущему приложению.</span><span class="sxs-lookup"><span data-stu-id="7f40a-112">This division of labor within the Ribbon framework architecture requires that a developer who wants to take advantage of the rich UI capabilities offered by the framework must design and describe the UI in markup, and then use the Ribbon framework COM interfaces to connect the framework to the host application.</span></span>

-   [<span data-ttu-id="7f40a-113">Путеводитель по лентам</span><span class="sxs-lookup"><span data-stu-id="7f40a-113">Ribbon Roadmap</span></span>](#ribbon-roadmap)
-   [<span data-ttu-id="7f40a-114">Написание разметки</span><span class="sxs-lookup"><span data-stu-id="7f40a-114">Write the Markup</span></span>](#write-the-markup)
    -   [<span data-ttu-id="7f40a-115">Компиляция разметки</span><span class="sxs-lookup"><span data-stu-id="7f40a-115">Compile the Markup</span></span>](#compile-the-markup)
-   [<span data-ttu-id="7f40a-116">Создание приложения</span><span class="sxs-lookup"><span data-stu-id="7f40a-116">Build the Application</span></span>](#build-the-application)
    -   [<span data-ttu-id="7f40a-117">Инициализация ленты</span><span class="sxs-lookup"><span data-stu-id="7f40a-117">Initialize the Ribbon</span></span>](#initialize-the-ribbon)
    -   [<span data-ttu-id="7f40a-118">Связывание разметки с приложением</span><span class="sxs-lookup"><span data-stu-id="7f40a-118">Link the Markup to the Application</span></span>](#link-the-markup-to-the-application)
    -   [<span data-ttu-id="7f40a-119">Компиляция приложения</span><span class="sxs-lookup"><span data-stu-id="7f40a-119">Compile the Application</span></span>](#link-the-markup-to-the-application)
-   [<span data-ttu-id="7f40a-120">Обновления и выполнения во время выполнения</span><span class="sxs-lookup"><span data-stu-id="7f40a-120">Run Time Updates and Executions</span></span>](#run-time-updates-and-executions)
-   [<span data-ttu-id="7f40a-121">Поддержка OLE</span><span class="sxs-lookup"><span data-stu-id="7f40a-121">OLE Support</span></span>](#ole-support)
-   [<span data-ttu-id="7f40a-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7f40a-122">Related topics</span></span>](#related-topics)

## <a name="ribbon-roadmap"></a><span data-ttu-id="7f40a-123">Путеводитель по лентам</span><span class="sxs-lookup"><span data-stu-id="7f40a-123">Ribbon Roadmap</span></span>

<span data-ttu-id="7f40a-124">Визуальные аспекты приложения на ленте, такие как отображаемые элементы управления и место их размещения, объявляются в разметке (см. раздел [объявление команд и элементов управления с разметкой ленты](windowsribbon-schema.md)).</span><span class="sxs-lookup"><span data-stu-id="7f40a-124">The visual aspects of a Ribbon application, such as what controls are displayed and where they are placed, are declared in markup (see [Declaring Commands and Controls with Ribbon Markup](windowsribbon-schema.md)).</span></span> <span data-ttu-id="7f40a-125">Логика команды приложения, например, что происходит при нажатии кнопки, реализуется в коде.</span><span class="sxs-lookup"><span data-stu-id="7f40a-125">The application command logic, such as what happens when a button is pressed, is implemented in code.</span></span>

<span data-ttu-id="7f40a-126">Процесс реализации ленты и его включения в приложение Windows требует выполнения четырех основных задач: написание разметки, компиляция разметки, написание кода и компиляция и связывание всего приложения.</span><span class="sxs-lookup"><span data-stu-id="7f40a-126">The process of implementing a Ribbon and incorporating it into a Windows application requires four basic tasks: write the markup, compile the markup, write the code, and compile and link the entire application.</span></span>

<span data-ttu-id="7f40a-127">На следующей схеме показан рабочий процесс для типичной реализации ленты.</span><span class="sxs-lookup"><span data-stu-id="7f40a-127">The following diagram illustrates the workflow for a typical Ribbon implementation.</span></span>

![Диаграмма, показывающая рабочий процесс для типичной реализации ленты.](images/overviews/ribbonroadmap.png)

<span data-ttu-id="7f40a-129">В следующих разделах этот процесс описан более подробно.</span><span class="sxs-lookup"><span data-stu-id="7f40a-129">The following sections describe this process in more detail.</span></span>

## <a name="write-the-markup"></a><span data-ttu-id="7f40a-130">Написание разметки</span><span class="sxs-lookup"><span data-stu-id="7f40a-130">Write the Markup</span></span>

<span data-ttu-id="7f40a-131">После разработки Ribbon в первую очередь разработчик приложения должен описать пользовательский интерфейс с разметкой ленты.</span><span class="sxs-lookup"><span data-stu-id="7f40a-131">After the Ribbon UI has been designed, the first task for an application developer is to describe the UI with Ribbon markup.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7f40a-132">Файл схемы разметки платформы Ribbon, УИКК. xsd, устанавливается вместе с пакетом средств разработки программного обеспечения Microsoft Windows (SDK) для Windows 7 и платформа .NET Framework 4,0.</span><span class="sxs-lookup"><span data-stu-id="7f40a-132">The Ribbon framework markup schema file, UICC.xsd, is installed with the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0.</span></span> <span data-ttu-id="7f40a-133">При использовании стандартного пути установки файл находится в папке bin% ProgramFiles% \\ Microsoft SDK \\ \\ \[ номер версии Windows, где на \] \\ него могут ссылаться многие редакторы XML для указания и автоматического завершения.</span><span class="sxs-lookup"><span data-stu-id="7f40a-133">Using the standard installation path, the file is located in the %ProgramFiles%\\Microsoft SDKs\\Windows\\\[version number\]\\Bin folder where it can be referenced by many XML editors to provide hinting and auto-completion.</span></span>

 

<span data-ttu-id="7f40a-134">Элементы управления ленты, команды Ribbon (независимые от элемента управления элементы, которые предоставляют базовую функциональность для элементов управления ленты), а все макеты элементов управления и визуальные связи объявляются в разметке.</span><span class="sxs-lookup"><span data-stu-id="7f40a-134">Ribbon controls, Ribbon Commands (the control-independent elements that provide the base functionality for Ribbon controls), and all control layout and visual relationships are declared in markup.</span></span> <span data-ttu-id="7f40a-135">Структура разметки ленты подчеркивает различие между элементами управления и командами ленты через две иерархии первичных узлов: [команды и дерево ресурсов](windowsribbon-reference-elements-command.md) , а также дерево [представлений](windowsribbon-reference-elements-view.md) .</span><span class="sxs-lookup"><span data-stu-id="7f40a-135">The structure of the Ribbon markup emphasizes the distinction between Ribbon controls and Commands through two primary node hierarchies: a [Commands and Resources](windowsribbon-reference-elements-command.md) tree and a [Views](windowsribbon-reference-elements-view.md) tree.</span></span>

<span data-ttu-id="7f40a-136">Все контейнеры и действия, предоставляемые лентой, объявляются в дереве [команды и ресурсы](windowsribbon-reference-elements-command.md) .</span><span class="sxs-lookup"><span data-stu-id="7f40a-136">All containers and actions that are exposed by the Ribbon are declared in the [Commands and Resources](windowsribbon-reference-elements-command.md) tree.</span></span> <span data-ttu-id="7f40a-137">Каждый элемент команды связан с набором ресурсов в соответствии с требованиями дизайна пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7f40a-137">Each Command element is associated with a set of resources, as required by the UI design.</span></span>

<span data-ttu-id="7f40a-138">После создания команд для приложения следует объявить элементы управления в дереве [представлений](windowsribbon-reference-elements-view.md) и привязать каждый элемент управления к команде, чтобы предоставить возможность команды.</span><span class="sxs-lookup"><span data-stu-id="7f40a-138">After you create the Commands for an application, you declare controls in the [Views](windowsribbon-reference-elements-view.md) tree and bind each control to a Command to expose the Command functionality.</span></span> <span data-ttu-id="7f40a-139">Платформа Ribbon определяет фактическое позиционирование элементов управления на основе иерархии элементов управления, объявленной здесь.</span><span class="sxs-lookup"><span data-stu-id="7f40a-139">The Ribbon framework determines the actual positioning of the controls based on the Control hierarchy declared here.</span></span>

<span data-ttu-id="7f40a-140">В следующем примере кода показано, как объявить элемент управления "Кнопка", "выход из приложения" и связать его с командой exit.</span><span class="sxs-lookup"><span data-stu-id="7f40a-140">The following code example illustrates how to declare a Button control, labeled Exit application, and associate it with an Exit Command.</span></span>


```
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
  <Application.Commands>
    <Command Name="cmdExit" LabelTitle="Exit application" />
  </Application.Commands>

  <Application.Views>
    <Ribbon>
      <Ribbon.Tabs>
        <Tab>
          <Group>
            <Button CommandName="cmdExit" />
          </Group>
        </Tab>
      </Ribbon.Tabs>
    </Ribbon>
  </Application.Views>
</Application>
        
```



> [!TIP]
> <span data-ttu-id="7f40a-141">Хотя для файла разметки ленты можно использовать любое расширение файла, расширение XML является рекомендуемым расширением, используемым во всей документации.</span><span class="sxs-lookup"><span data-stu-id="7f40a-141">While it is possible to use any file name extension for the Ribbon markup file, .xml is the recommended extension that is used throughout the documentation.</span></span>

 

### <a name="compile-the-markup"></a><span data-ttu-id="7f40a-142">Компиляция разметки</span><span class="sxs-lookup"><span data-stu-id="7f40a-142">Compile the Markup</span></span>

<span data-ttu-id="7f40a-143">После создания файла разметки ленты его необходимо скомпилировать в двоичный формат с помощью компилятора разметки ленты, компилятора команд пользовательского интерфейса (УИКК), который входит в состав пакета средств разработки программного обеспечения (SDK) для Windows.</span><span class="sxs-lookup"><span data-stu-id="7f40a-143">After the Ribbon markup file is created, it must be compiled into a binary format by the Ribbon markup compiler, UI Command Compiler (UICC), that is included with the Windows software development kit (SDK).</span></span> <span data-ttu-id="7f40a-144">Ссылка на этот двоичный файл передается методу [**иуифрамеворк:: лоадуи**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) во время инициализации платформы Ribbon ведущим приложением.</span><span class="sxs-lookup"><span data-stu-id="7f40a-144">A reference to this binary file is passed to the [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) method during initialization of the Ribbon framework by the host application.</span></span>

<span data-ttu-id="7f40a-145">УИКК можно выполнить непосредственно из окна командной строки или добавить в качестве настраиваемого этапа сборки в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7f40a-145">UICC can be executed directly from a command-line window or added as a "Custom Build Step" in Visual Studio.</span></span>

<span data-ttu-id="7f40a-146">На следующем рисунке показан компилятор разметки УИКК в окне оболочки CMD пакета SDK для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7f40a-146">The following image shows the UICC markup compiler in the Windows 7 SDK CMD Shell window.</span></span>

![снимок экрана, отображающий uicc.exe в окне командной строки.](images/overviews/screenshot-intentcl-commandline.png)

<span data-ttu-id="7f40a-148">На следующем рисунке показано, как УИКК добавлен в Visual Studio в качестве настраиваемого этапа сборки.</span><span class="sxs-lookup"><span data-stu-id="7f40a-148">The following image shows UICC added as a Custom Build Step in Visual Studio.</span></span>

![снимок экрана, отображающий uicc.exe, добавленный в виде настраиваемого этапа сборки в Visual Studio.](images/overviews/screenshot-vs-intentcl-custombuildstep.png)

<span data-ttu-id="7f40a-150">УИКК создает три файла: двоичная версия разметки (. БМЛ), заголовок определения идентификатора (h-файл) для предоставления элементов разметки ведущему приложению ленты, а также [скрипт определения ресурса](../menurc/about-resource-files.md) (RC-файл) для связывания изображения ленты и строковых ресурсов с ведущим приложением во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="7f40a-150">The UICC generates three files: a binary version of the markup (.bml), an ID definition header (.h file) to expose markup elements to the Ribbon host application, and a [resource-definition script](../menurc/about-resource-files.md) (.rc file) to link Ribbon image and string resources to the host application at compile time.</span></span>

<span data-ttu-id="7f40a-151">Дополнительные сведения о компиляции разметки платформы ленты см. в разделе [Компиляция разметки ленты](windowsribbon-intentcl.md).</span><span class="sxs-lookup"><span data-stu-id="7f40a-151">For more detail on compiling Ribbon framework markup, see [Compiling Ribbon Markup](windowsribbon-intentcl.md).</span></span>

## <a name="build-the-application"></a><span data-ttu-id="7f40a-152">Построение приложения</span><span class="sxs-lookup"><span data-stu-id="7f40a-152">Build the Application</span></span>

<span data-ttu-id="7f40a-153">После того как предварительный пользовательский интерфейс для приложения ленты разрабатывается и реализован в разметке, необходимо написать код приложения, который инициализирует платформу, использует разметку и привязывает команды, объявленные в разметке к соответствующим обработчикам команд в приложении.</span><span class="sxs-lookup"><span data-stu-id="7f40a-153">Once the preliminary UI for a Ribbon application has been designed and implemented in markup, application code must be written that initializes the framework, consumes the markup, and binds the Commands declared in the markup to the appropriate Command handlers in the application.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="7f40a-154">Так как платформа Ribbon основана на модели COM, рекомендуется использовать \_ \_ оператор ууидоф () для ссылки на идентификаторы GUID для интерфейсов платформы Ribbon (идентификаторов IID).</span><span class="sxs-lookup"><span data-stu-id="7f40a-154">Since the Ribbon framework is COM-based, it is recommended that Ribbon projects use the \_\_uuidof() operator to reference the GUIDs for Ribbon framework interfaces (IIDs).</span></span> <span data-ttu-id="7f40a-155">В тех случаях, когда невозможно использовать \_ \_ оператор ууидоф (), например, если используется компилятор, отличный от Майкрософт, или ведущее приложение на языке C, идентификаторов IID должно быть определено приложением, так как они не содержатся в UUID. lib.</span><span class="sxs-lookup"><span data-stu-id="7f40a-155">In those cases where it is not possible to use the \_\_uuidof() operator, such as when a non-Microsoft compiler is used or the host application is C-based, the IIDs must be defined by the application since they are not contained in uuid.lib.</span></span>
>
> <span data-ttu-id="7f40a-156">Если идентификаторов IID определены приложением, необходимо использовать идентификаторы GUID, указанные в Уириббон. idl.</span><span class="sxs-lookup"><span data-stu-id="7f40a-156">If the IIDs are defined by the application then the GUIDs specified in UIRibbon.idl must be used.</span></span>
>
> <span data-ttu-id="7f40a-157">Уириббон. idl поставляется в составе [пакета средств разработки программного обеспечения (SDK) для Windows](https://msdn.microsoft.com/windows/bb980924.aspx) и находится по стандартному пути установки% ProgramFiles% \\ пакеты SDK Microsoft \\ Windows \\ v 7.0 \\ включают.</span><span class="sxs-lookup"><span data-stu-id="7f40a-157">UIRibbon.idl ships as part of the [Windows Software Development Kit (SDK)](https://msdn.microsoft.com/windows/bb980924.aspx) and can be found at the standard installation path of %ProgramFiles%\\Microsoft SDKs\\Windows\\v7.0\\Include.</span></span>

 

### <a name="initialize-the-ribbon"></a><span data-ttu-id="7f40a-158">Инициализация ленты</span><span class="sxs-lookup"><span data-stu-id="7f40a-158">Initialize the Ribbon</span></span>

<span data-ttu-id="7f40a-159">На следующей схеме показаны шаги, необходимые для реализации простого приложения на ленте.</span><span class="sxs-lookup"><span data-stu-id="7f40a-159">The following diagram illustrates the steps required to implement a simple Ribbon application.</span></span>

![Схема, на которой показаны шаги, необходимые для реализации простой реализации ленты.](images/overviews/initializationsteps.png)

<span data-ttu-id="7f40a-161">Следующие шаги подробно описывают, как реализовать простое приложение на ленте.</span><span class="sxs-lookup"><span data-stu-id="7f40a-161">The following steps describe in detail how to implement a simple Ribbon application.</span></span>

1.  <span data-ttu-id="7f40a-162">CoCreateInstance</span><span class="sxs-lookup"><span data-stu-id="7f40a-162">CoCreateInstance</span></span>

    <span data-ttu-id="7f40a-163">Приложение вызывает стандартную функцию CoCreateInstance COM с ИДЕНТИФИКАТОРом класса платформы Ribbon для получения указателя на платформу.</span><span class="sxs-lookup"><span data-stu-id="7f40a-163">The application calls the standard COM CoCreateInstance function with the Ribbon framework class ID to obtain a pointer to the framework.</span></span>

    ```
    IUIFramework* pFramework = NULL;
    HRESULT hr = ::CoCreateInstance(
                CLSID_UIRibbonFramework, 
                NULL,
                CLSCTX_INPROC_SERVER, 
                IID_PPV_ARGS(&pFramework));
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

2.  <span data-ttu-id="7f40a-164">Initialize (HWND, Иуиаппликатион \* )</span><span class="sxs-lookup"><span data-stu-id="7f40a-164">Initialize(hwnd, IUIApplication\*)</span></span>

    <span data-ttu-id="7f40a-165">Приложение вызывает [**иуифрамеворк:: Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), передавая два параметра: указатель на окно верхнего уровня, которое будет содержать ленту, и указатель на реализацию [**иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) , которая позволяет платформе выполнять обратные вызовы к приложению.</span><span class="sxs-lookup"><span data-stu-id="7f40a-165">The application calls [**IUIFramework::Initialize**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-initialize), passing in two parameters: the handle to the top-level window that will contain the Ribbon and a pointer to the [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) implementation that allows the framework to make callbacks to the application.</span></span>

    > <span data-ttu-id="7f40a-166">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="7f40a-166">\[!Important\]</span></span>  
    > <span data-ttu-id="7f40a-167">Платформа ленты инициализируется как однопотоковое подразделение (STA).</span><span class="sxs-lookup"><span data-stu-id="7f40a-167">The Ribbon framework is initialized as a single-threaded apartment (STA).</span></span>

     

    ```
    hr = pFramework->Initialize(hWndHost, pApplication);
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

3.  <span data-ttu-id="7f40a-168">Лоадуи (экземпляр, resourceName)</span><span class="sxs-lookup"><span data-stu-id="7f40a-168">LoadUI(instance, resourceName)</span></span>

    <span data-ttu-id="7f40a-169">Приложение вызывает [**иуифрамеворк:: лоадуи**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) для привязки ресурса разметки.</span><span class="sxs-lookup"><span data-stu-id="7f40a-169">The application calls [**IUIFramework::LoadUI**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-loadui) to bind the markup resource.</span></span> <span data-ttu-id="7f40a-170">Первый параметр этой функции является маркером для экземпляра приложения ленты.</span><span class="sxs-lookup"><span data-stu-id="7f40a-170">The first parameter of this function is a handle to the Ribbon application instance.</span></span> <span data-ttu-id="7f40a-171">Вторым параметром является имя ресурса двоичной разметки, который был скомпилирован ранее.</span><span class="sxs-lookup"><span data-stu-id="7f40a-171">The second parameter is the name of the binary markup resource that was compiled previously.</span></span> <span data-ttu-id="7f40a-172">Передавая двоичную разметку в платформу Ribbon, приложение сигнализирует, что должна быть структура ленты и как должны упорядочиваться элементы управления.</span><span class="sxs-lookup"><span data-stu-id="7f40a-172">By passing the binary markup to the Ribbon framework, the application signals what the Ribbon structure should be and how controls should be arranged.</span></span> <span data-ttu-id="7f40a-173">Она также предоставляет платформу с манифестом команд для предоставления (например, вставки, вырезания, поиска), которые используются платформой при выполнении обратных вызовов, связанных с командой, во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7f40a-173">It also provides the framework with a manifest of commands to expose (such as Paste, Cut, Find), which are used by the framework when it makes Command-related callbacks at run time.</span></span>

    ```
    hr = pFramework->LoadUI(GetModuleHandle(NULL), L"APPLICATION_RIBBON");
    if (FAILED(hr))
    {
      return hr;
    }
    ```

    

4.  <span data-ttu-id="7f40a-174">Обратные вызовы [**иуиаппликатион:: онкреатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand)</span><span class="sxs-lookup"><span data-stu-id="7f40a-174">[**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) callbacks</span></span>

    <span data-ttu-id="7f40a-175">После выполнения шагов 1 – 3 платформа Ribbon знает, какие команды нужно предоставить на ленте.</span><span class="sxs-lookup"><span data-stu-id="7f40a-175">After steps 1 through 3 are completed, the Ribbon framework knows which Commands to expose in the Ribbon.</span></span> <span data-ttu-id="7f40a-176">Тем не менее для полной функциональности платформы необходимо выполнить два действия: способ указать приложению, когда выполняются команды, и способ получения ресурсов команды или свойств во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="7f40a-176">However, the framework still needs two things before the Ribbon is fully functional: a way to tell the application when Commands are executed and a way to get Command resources, or properties, at run time.</span></span> <span data-ttu-id="7f40a-177">Например, если поле со списком отображается в пользовательском интерфейсе, платформа должна запросить элементы, с которыми будет заполнено поле со списком.</span><span class="sxs-lookup"><span data-stu-id="7f40a-177">For example, if a combo box is to appear in the UI, then the framework needs to ask for the items with which to populate the combo box.</span></span>

    <span data-ttu-id="7f40a-178">Эти две части функциональности обрабатываются через интерфейс [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) .</span><span class="sxs-lookup"><span data-stu-id="7f40a-178">These two pieces of functionality are handled through the [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface.</span></span> <span data-ttu-id="7f40a-179">В частности, для каждой команды, объявленной в двоичной разметке (см. шаг 3 выше), платформа вызывает [**иуиаппликатион:: онкреатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) , чтобы запросить у приложения объект **иуикоммандхандлер** для этой команды.</span><span class="sxs-lookup"><span data-stu-id="7f40a-179">Specifically, for each command declared in the binary markup (see Step 3 above), the framework calls [**IUIApplication::OnCreateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiapplication-oncreateuicommand) to ask the application for an **IUICommandHandler** object for that command</span></span>

    > [!Note]  
    > <span data-ttu-id="7f40a-180">Интерфейс [**иуикоммандхандлер**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) позволяет привязать обработчик команд к одной или нескольким командам.</span><span class="sxs-lookup"><span data-stu-id="7f40a-180">The [**IUICommandHandler**](/windows/desktop/api/uiribbon/nn-uiribbon-iuicommandhandler) interface allows a Command handler to be bound to one or more Commands.</span></span>

     

<span data-ttu-id="7f40a-181">Как минимум, приложению требуется реализовать заглушки методов [**иуиаппликатион**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) , возвращающие E \_ нотимпл, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="7f40a-181">At a minimum, the application is required to implement [**IUIApplication**](/windows/desktop/api/uiribbon/nn-uiribbon-iuiapplication) methods stubs that return E\_NOTIMPL as shown in the following example.</span></span>


```
STDMETHOD(OnViewChanged)(UINT32 viewId,
                         UI_VIEWTYPE typeID,
                         IUnknown *view,
                         UI_VIEWVERB verb,
                         INT32 uReasonCode)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnCreateUICommand)(UINT32 commandId,
                             UI_COMMANDTYPE typeID,
                             IUICommandHandler **commandHandler)
{ 
  return E_NOTIMPL; 
}

STDMETHOD(OnDestroyUICommand)(UINT32 commandId,
                              UI_COMMANDTYPE typeID,
                              IUICommandHandler *commandHandler) 
{ 
  return E_NOTIMPL; 
}
```



### <a name="link-the-markup-to-the-application"></a><span data-ttu-id="7f40a-182">Связывание разметки с приложением</span><span class="sxs-lookup"><span data-stu-id="7f40a-182">Link the Markup to the Application</span></span>

<span data-ttu-id="7f40a-183">На этом этапе файлы ресурсов разметки должны быть связаны с ведущим приложением, включив ссылку на файл определения ресурса разметки (который содержит ссылку на файл заголовка разметки) в файле ресурсов приложения.</span><span class="sxs-lookup"><span data-stu-id="7f40a-183">At this point, the markup resource files must be linked to the host application by including a reference to the markup resource-definition file (which contains a reference to the markup header file) in the application resource file.</span></span> <span data-ttu-id="7f40a-184">Например, для приложения с именем Риббонапп и файлом ресурсов с именем Риббонуи. RC требуется следующая строка в файле Риббонапп. rc.</span><span class="sxs-lookup"><span data-stu-id="7f40a-184">For example, an application called RibbonApp with a resource file called ribbonUI.rc requires the following line in the RibbonApp.rc file.</span></span>


```C++
#include "ribbonUI.rc"
```



<span data-ttu-id="7f40a-185">В зависимости от используемого компилятора и компоновщика скрипт определения ресурса может также требовать компиляции перед компиляцией приложения Ribbon.</span><span class="sxs-lookup"><span data-stu-id="7f40a-185">Depending on the compiler and linker being used, the resource-definition script may also require compiling before the Ribbon application can be compiled.</span></span> <span data-ttu-id="7f40a-186">Для этой задачи можно использовать программу командной строки [компилятора ресурсов (RC)](../menurc/using-rc-the-rc-command-line-.md) , которая поставляется с Microsoft Visual Studio и Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="7f40a-186">The [resource compiler (RC)](../menurc/using-rc-the-rc-command-line-.md) command line tool that ships with Microsoft Visual Studio and the Windows SDK can be used for this task.</span></span>

### <a name="compile-the-application"></a><span data-ttu-id="7f40a-187">Компиляция приложения</span><span class="sxs-lookup"><span data-stu-id="7f40a-187">Compile the Application</span></span>

<span data-ttu-id="7f40a-188">После компиляции приложения на ленте его можно запустить и проверить пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7f40a-188">Once the Ribbon application is compiled, it can be run and the UI tested.</span></span> <span data-ttu-id="7f40a-189">Если в пользовательском интерфейсе требуется настройка и нет изменений в связанных обработчиках команд в основном коде приложения, измените исходный файл разметки, перескомпилируйте разметку с UICC.exe и свяжите новые файлы ресурсов разметки.</span><span class="sxs-lookup"><span data-stu-id="7f40a-189">If the UI requires tweaking and there are no changes to any associated Command handlers in the core application code, revise the markup source file, recompile the markup with UICC.exe, and link the new markup resource files.</span></span> <span data-ttu-id="7f40a-190">При перезапуске приложения отображается измененный пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="7f40a-190">When the application is restarted, the modified UI is displayed.</span></span>

<span data-ttu-id="7f40a-191">Все это возможно, не затрагивая основной код приложения — значительное улучшение по сравнению со стандартными разработками и распространением приложений.</span><span class="sxs-lookup"><span data-stu-id="7f40a-191">All this is possible without touching the core application code—a significant improvement over standard application development and distribution.</span></span>

## <a name="run-time-updates-and-executions"></a><span data-ttu-id="7f40a-192">Обновления и выполнения во время выполнения</span><span class="sxs-lookup"><span data-stu-id="7f40a-192">Run Time Updates and Executions</span></span>

<span data-ttu-id="7f40a-193">Структура взаимодействия платформы Ribbon во время выполнения основана на принудительном и опрашивающем, или двустороннем вызывающем объекте Model.</span><span class="sxs-lookup"><span data-stu-id="7f40a-193">The run-time communication structure of the Ribbon framework is based on a push and pull, or two-way caller, model.</span></span>

<span data-ttu-id="7f40a-194">Эта модель позволяет платформе уведомлять приложение при выполнении команды и позволяет платформе и приложению запрашивать, обновлять и делать недействительными значения свойств и ресурсов ленты.</span><span class="sxs-lookup"><span data-stu-id="7f40a-194">This model allows the framework to inform the application when a Command is executed and allows both the framework and the application to query, update, and invalidate property values and Ribbon resources.</span></span> <span data-ttu-id="7f40a-195">Эта функция предоставляется через ряд интерфейсов и методов.</span><span class="sxs-lookup"><span data-stu-id="7f40a-195">This functionality is provided through a number of interfaces and methods.</span></span>

<span data-ttu-id="7f40a-196">Платформа извлекает обновленные сведения о свойствах из приложения ленты с помощью метода обратного вызова [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="7f40a-196">The framework pulls updated property information from the Ribbon application through the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span> <span data-ttu-id="7f40a-197">Идентификатор команды и ключ свойства, определяющие обновляемое свойство команды, передаются в метод, который затем возвращает или передает значение для этого ключа свойства в платформу.</span><span class="sxs-lookup"><span data-stu-id="7f40a-197">A Command ID and a property key, which identifies the Command property to update, are passed to the method which then returns, or pushes, a value for that property key to the framework.</span></span>

<span data-ttu-id="7f40a-198">Платформа вызывает [**иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) при выполнении команды, определяя идентификатор команды и тип выполнения ([**UI \_ ексекутионверб**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span><span class="sxs-lookup"><span data-stu-id="7f40a-198">The framework calls [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) when a Command is executed, identifying both the Command ID and the type of execution that occurred ([**UI\_EXECUTIONVERB**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_executionverb)).</span></span> <span data-ttu-id="7f40a-199">Здесь приложение указывает логику выполнения для команды.</span><span class="sxs-lookup"><span data-stu-id="7f40a-199">This is where the application specifies the execution logic for a command.</span></span>

<span data-ttu-id="7f40a-200">На следующей схеме показана связь времени выполнения для выполнения команд между платформой и приложением.</span><span class="sxs-lookup"><span data-stu-id="7f40a-200">The following diagram illustrates the run-time communication for Command execution between the framework and the application.</span></span>

![Схема, на которой показан пример взаимодействия между платформой Ribbon и ведущим приложением.](images/overviews/updatesandexecutions.png)

> [!Note]  
> <span data-ttu-id="7f40a-202">Реализация функций [**иуикоммандхандлер:: упдатепроперти**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) и [**Иуикоммандхандлер:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) не требуется для первоначального вывода ленты в приложении.</span><span class="sxs-lookup"><span data-stu-id="7f40a-202">Implementing the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) and [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) functions is not necessary to initially display a Ribbon in an application.</span></span> <span data-ttu-id="7f40a-203">Однако эти методы необходимы, чтобы обеспечить правильное функционирование приложения при выполнении команд пользователем.</span><span class="sxs-lookup"><span data-stu-id="7f40a-203">However, these methods are necessary to ensure that the application functions correctly when commands are executed by the user.</span></span>

 

## <a name="ole-support"></a><span data-ttu-id="7f40a-204">Поддержка OLE</span><span class="sxs-lookup"><span data-stu-id="7f40a-204">OLE Support</span></span>

<span data-ttu-id="7f40a-205">Приложение ленты можно настроить как OLE-сервер для поддержки внутренней OLE-активации.</span><span class="sxs-lookup"><span data-stu-id="7f40a-205">A Ribbon application can be configured as an OLE server to support out-of-place OLE activation.</span></span>

<span data-ttu-id="7f40a-206">Объекты, созданные в приложении OLE-сервера, сохраняют связь с серверным приложением при вставке (вставленном или помещенном) в клиентское приложение OLE (или контейнер).</span><span class="sxs-lookup"><span data-stu-id="7f40a-206">Objects created in an OLE server application maintain their association with the server application when inserted (either pasted or placed) into an OLE client application (or container).</span></span> <span data-ttu-id="7f40a-207">При неразмещенной OLE-активации дважды щелкните объект в клиентском приложении, чтобы открыть выделенный экземпляр серверного приложения и загрузить объект для редактирования.</span><span class="sxs-lookup"><span data-stu-id="7f40a-207">In out-of-place OLE activation, double clicking the object in the client application opens a dedicated instance of the server application and loads the object for editing.</span></span> <span data-ttu-id="7f40a-208">При закрытии серверного приложения все изменения, внесенные в объект, отражаются в клиентском приложении.</span><span class="sxs-lookup"><span data-stu-id="7f40a-208">When the server application is closed, all changes made to the object are reflected in the client application.</span></span>

> [!Note]  
> <span data-ttu-id="7f40a-209">Платформа Ribbon не поддерживает активацию OLE на месте.</span><span class="sxs-lookup"><span data-stu-id="7f40a-209">The Ribbon framework does not support in-place OLE activation.</span></span> <span data-ttu-id="7f40a-210">Объекты, созданные в OLE-сервере на основе ленты, нельзя редактировать в клиентском приложении OLE.</span><span class="sxs-lookup"><span data-stu-id="7f40a-210">Objects created in a Ribbon-based OLE server cannot be edited from within the OLE client application.</span></span> <span data-ttu-id="7f40a-211">Требуется внешний выделенный экземпляр серверного приложения.</span><span class="sxs-lookup"><span data-stu-id="7f40a-211">An external dedicated instance of the server application is required.</span></span>


## <a name="related-topics"></a><span data-ttu-id="7f40a-212">См. также</span><span class="sxs-lookup"><span data-stu-id="7f40a-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f40a-213">Объявление команд и элементов управления с разметкой ленты</span><span class="sxs-lookup"><span data-stu-id="7f40a-213">Declaring Commands and Controls with Ribbon Markup</span></span>](./windowsribbon-schema.md)
</dt> <dt>

[<span data-ttu-id="7f40a-214">Рекомендации по работе пользователя с лентой</span><span class="sxs-lookup"><span data-stu-id="7f40a-214">Ribbon User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/cc872782.aspx)
</dt> <dt>

[<span data-ttu-id="7f40a-215">Процесс разработки ленты</span><span class="sxs-lookup"><span data-stu-id="7f40a-215">Ribbon Design Process</span></span>](https://msdn.microsoft.com/library/cc872781.aspx)
</dt> </dl>

 

 




