---
title: Основные сведения о командах и элементах управления
description: Разделение логики из представления является философией проектирования, инспирес систему представления команд Windows Ribbon Framework \ 8212; система, основанная на шаблоне разработки, где функциональность и поведение реализуются независимо от элементов управления, предоставляющих эту функциональность.
ms.assetid: fdea0d70-c6e0-4d13-99bc-ff0c1dbff10d
keywords:
- Лента Windows, общие сведения о командах
- Лента, общие сведения о командах
- Лента Windows, общие сведения об элементах управления
- Лента, общие сведения об элементах управления
- система команд для ленты Windows
- элементы управления для ленты Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2659da608a3d3e73f3f35ac1911946a6685c74e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104555440"
---
# <a name="understanding-commands-and-controls"></a><span data-ttu-id="fd2e6-109">Основные сведения о командах и элементах управления</span><span class="sxs-lookup"><span data-stu-id="fd2e6-109">Understanding Commands and Controls</span></span>

<span data-ttu-id="fd2e6-110">Разделение логики из представления представляет собой философство проектирования, инспирес систему представления команд платформы Windows Ribbon Framework — систему, основанную на шаблоне разработки, где функциональность и поведение реализуются независимо от элементов управления, предоставляющих эти функции.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-110">The separation of logic from presentation is the design philosophy that inspires the command presentation system of the Windows Ribbon framework—a system that is based on a design pattern where functionality and behavior are implemented independently from the controls that expose this functionality.</span></span>

-   [<span data-ttu-id="fd2e6-111">Введение</span><span class="sxs-lookup"><span data-stu-id="fd2e6-111">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="fd2e6-112">Командная система ленты Windows</span><span class="sxs-lookup"><span data-stu-id="fd2e6-112">The Windows Ribbon Command System</span></span>](#the-windows-ribbon-command-system)
    -   [<span data-ttu-id="fd2e6-113">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="fd2e6-113">Controls</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="fd2e6-114">Команды</span><span class="sxs-lookup"><span data-stu-id="fd2e6-114">Commands</span></span>](#understanding-commands-and-controls)
    -   [<span data-ttu-id="fd2e6-115">Интерфейс команды в действии</span><span class="sxs-lookup"><span data-stu-id="fd2e6-115">The Command Experience In Action</span></span>](#the-command-experience-in-action)
-   [<span data-ttu-id="fd2e6-116">См. также</span><span class="sxs-lookup"><span data-stu-id="fd2e6-116">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="fd2e6-117">Введение</span><span class="sxs-lookup"><span data-stu-id="fd2e6-117">Introduction</span></span>

<span data-ttu-id="fd2e6-118">В этой статье рассматривается структура командной системы платформы Ribbon.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-118">This article discusses the design of the Ribbon framework command system.</span></span> <span data-ttu-id="fd2e6-119">В нем описываются основные понятия команд и элементов управления, а также рассматриваются принципы их совместной работы, позволяющие обеспечить широкие возможности команд с помощью новых возможностей пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-119">It describes the concepts of Commands and controls and explores how they work together to provide a rich command experience with a host of new UI capabilities.</span></span>

## <a name="the-windows-ribbon-command-system"></a><span data-ttu-id="fd2e6-120">Командная система ленты Windows</span><span class="sxs-lookup"><span data-stu-id="fd2e6-120">The Windows Ribbon Command System</span></span>

<span data-ttu-id="fd2e6-121">В платформе Ribbon команды и элементы управления являются независимыми сущностями.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-121">In the Ribbon framework, Commands and controls are independent entities.</span></span> <span data-ttu-id="fd2e6-122">Команда является абстрактной структурой без ограничений презентации, которая представляет конкретную задачу или класс функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-122">A Command is an abstract structure, without presentation constraints, that represents a specific task or class of functionality.</span></span> <span data-ttu-id="fd2e6-123">С другой стороны, элемент управления представляет собой конкретный объект, который предоставляет функциональные возможности команды через пользовательский интерфейс ленты.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-123">A control, on the other hand, is a concrete object that exposes Command functionality through the Ribbon UI.</span></span>

<span data-ttu-id="fd2e6-124">Это различие дает возможность определять команды, которые не являются сведениями о пользовательском интерфейсе и могут выполняться с целью действия без необходимости управлять способом вызова действия.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-124">This distinction provides the ability to define Commands that are free of UI details and able to execute on the intent of an action without the need to manage how the action was invoked.</span></span>

### <a name="controls"></a><span data-ttu-id="fd2e6-125">Элементы управления</span><span class="sxs-lookup"><span data-stu-id="fd2e6-125">Controls</span></span>

<span data-ttu-id="fd2e6-126">Элементы управления — это объекты пользовательского интерфейса, необходимые для представления команды.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-126">Controls are the UI objects required for Command presentation.</span></span> <span data-ttu-id="fd2e6-127">Они подготавливаются к просмотру и управляются во время выполнения платформой на основе взаимодействия с пользователем и набора встроенных свойств и поведения.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-127">They are rendered and managed at run time by the framework based on user interaction and a set of inherent properties and behaviors.</span></span>

<span data-ttu-id="fd2e6-128">Наиболее гибкая структура, управляемая платформой, известна как адаптивная, является одной из замечательных достоинств ленты.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-128">Known as adaptive layout, the framework-managed flexibility of the UI is one of the great strengths of the Ribbon.</span></span> <span data-ttu-id="fd2e6-129">Элементы управления ленты могут автоматически перенастраиваться с помощью зависимых от платформы или определенных разработчиком шаблонов макета, которые могут отвечать на различные требования ко времени выполнения, без написания кода презентации.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-129">Ribbon controls can automatically reconfigure themselves through framework-dependent or developer-defined layout templates that are able to respond to various run time requirements, all without writing a single line of presentation code.</span></span> <span data-ttu-id="fd2e6-130">Дополнительные сведения см. в разделе [Настройка ленты с помощью определений размеров и политик масштабирования](windowsribbon-templates.md).</span><span class="sxs-lookup"><span data-stu-id="fd2e6-130">For more information, see [Customizing a Ribbon Through Size Definitions and Scaling Policies](windowsribbon-templates.md).</span></span>

<span data-ttu-id="fd2e6-131">Помимо преимуществ адаптивного макета, ряд сложных элементов управления ленты предоставляют автономные решения для конкретных пространств проблемы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-131">Besides the benefits of adaptive layout, a number of complex Ribbon controls provide self-contained solutions for specific UI problem spaces.</span></span> <span data-ttu-id="fd2e6-132">Предлагая сложную модель взаимодействия, элементы управления Ribbon, такие как Фонтконтрол или ColorPicker, предоставляют возможность манипулировать данными более абстрактными терминами через контейнеры свойств для атрибутов шрифта или цвета, а не через различные подэлементы управления, перечисления и значения индекса стандартных элементов управления Windows.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-132">By offering a sophisticated interaction model, Ribbon controls, such as the FontControl or ColorPicker, provide the ability to manipulate data in more abstract terms through property bags of actual font or color attributes rather than through various sub-controls, enumerations, and index values of standard Windows controls.</span></span>

### <a name="commands"></a><span data-ttu-id="fd2e6-133">Команды</span><span class="sxs-lookup"><span data-stu-id="fd2e6-133">Commands</span></span>

<span data-ttu-id="fd2e6-134">Слабо связаны с элементами управления ленты, которые предоставляют свои функциональные возможности, реализации команд являются доменом ведущего приложения и принимают форму прослушивателей событий, обработчиков команд и различные свойства команд.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-134">Loosely coupled to the Ribbon controls that expose their functionality, Command implementations are the domain of the host application and take the form of event listeners, Command handlers, and various Command properties.</span></span>

<span data-ttu-id="fd2e6-135">Команды объявляются в разметке ленты с помощью уникального идентификатора или назначает идентификатор, созданный компилятором разметки при компиляции.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-135">Commands are declared in Ribbon markup with a unique ID, or assigned a markup compiler-generated ID at compilation.</span></span> <span data-ttu-id="fd2e6-136">Команды связаны с элементами управления с помощью имени команды, но, в отличие от элементов управления, их фактические функциональные возможности определяются в коде, где они привязаны к определенным обработчикам команд через идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-136">Commands are associated with controls through a Command name but, unlike controls, their actual functionality is defined in code where they are bound to specific Command handlers through the Command ID.</span></span>

> [!Note]  
> <span data-ttu-id="fd2e6-137">При компиляции этот идентификатор хранится в файле заголовка определения идентификатора, который предоставляет команды для соответствующих обработчиков команд в ведущем приложении ленты.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-137">At compilation, this ID is stored in an ID definition header file that exposes Commands to their corresponding Command handlers in the Ribbon host application.</span></span>

 

<span data-ttu-id="fd2e6-138">Каждая команда имеет базовый тип команды в перечислении элемента [**пользовательского интерфейса \_ COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) .</span><span class="sxs-lookup"><span data-stu-id="fd2e6-138">Each Command has an underlying Command type itemized in the [**UI\_COMMANDTYPE**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_commandtype) enumeration.</span></span>

### <a name="the-command-experience-in-action"></a><span data-ttu-id="fd2e6-139">Интерфейс команды в действии</span><span class="sxs-lookup"><span data-stu-id="fd2e6-139">The Command Experience In Action</span></span>

<span data-ttu-id="fd2e6-140">Возможности этой модели команды показаны на панели быстрого доступа к ленте (QAT).</span><span class="sxs-lookup"><span data-stu-id="fd2e6-140">The capabilities of this command model are demonstrated by the Ribbon Quick Access Toolbar (QAT).</span></span> <span data-ttu-id="fd2e6-141">QAT предоставляет конечным пользователям способ простого определения собственных сочетаний клавиш для практически любого элемента управления в ленте.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-141">The QAT provides end users with a way to easily define their own shortcuts for virtually any control in the Ribbon UI.</span></span> <span data-ttu-id="fd2e6-142">Ярлык динамически добавляется в QAT во время выполнения, когда пользователь щелкает правой кнопкой мыши элемент управления "лента" и выбирает в контекстном меню команду **Добавить в панель быстрого доступа** .</span><span class="sxs-lookup"><span data-stu-id="fd2e6-142">A shortcut is added dynamically to the QAT at run time when the user right-clicks a Ribbon control and selects **Add to Quick Access Toolbar** from the context menu.</span></span>

<span data-ttu-id="fd2e6-143">На следующем рисунке показана команда **Вставить** и **Вставить из** команд, представленных элементом управления [**SplitButton**](windowsribbon-element-splitbutton.md) , на ленте Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-143">The following picture shows the **Paste** and **Paste from** Commands, represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon of Windows 7 Paint.</span></span>

![изображение элемента splitButton на ленте Microsoft Paint.](images/overviews/paint-paste-splitbutton-ribbon.png)

<span data-ttu-id="fd2e6-145">На следующем рисунке показана та же **Вставка** и **Вставка из** команд, которые по-прежнему представлены элементом управления [**SplitButton**](windowsribbon-element-splitbutton.md) на ленте QAT Windows 7 Paint.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-145">The following picture shows the same **Paste** and **Paste from** Commands, still represented by a [**SplitButton**](windowsribbon-element-splitbutton.md) control, in the Ribbon QAT of Windows 7 Paint.</span></span>

![изображение элемента splitButton в qatе Microsoft Paint.](images/overviews/paint-paste-splitbutton-qat.png)

<span data-ttu-id="fd2e6-147">Когда элемент управления размещается в QAT, новый экземпляр элемента управления сохраняет все функциональные возможности исходного элемента управления без необходимости его поддержки для дополнительных прослушивателей событий и обработчиков команд.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-147">When a control is hosted by the QAT, the new instance of the control maintains all the functionality of the original control without the need for additional event listeners and command handlers to support it.</span></span> <span data-ttu-id="fd2e6-148">Оба элемента управления привязаны к одному обработчику команд ленты через общий идентификатор команды.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-148">Both controls are bound to the same Ribbon Command handler through a shared Command identifier.</span></span> <span data-ttu-id="fd2e6-149">Таким образом, платформа рассматривает оба элемента управления как один, независимо от того, какой из них вызывается.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-149">In this way, the framework treats both controls as one, no matter which is invoked.</span></span>

> [!Note]  
> <span data-ttu-id="fd2e6-150">Те же преимущества реализуются при внедрении команд в [**контекстпопуп**](windowsribbon-element-contextpopup.md) во время разработки.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-150">The same benefits are realized when Commands are incorporated into a [**ContextPopup**](windowsribbon-element-contextpopup.md) at design time.</span></span> <span data-ttu-id="fd2e6-151">В этом случае можно использовать обработчики команд вставки, если элемент управления [**SplitButton**](windowsribbon-element-splitbutton.md) отображается на ЛЕНТЕ, QAT или **контекстпопуп**.</span><span class="sxs-lookup"><span data-stu-id="fd2e6-151">In this case, the Paste Command handlers can be used whether the [**SplitButton**](windowsribbon-element-splitbutton.md) control appears in the Ribbon, the QAT, or the **ContextPopup**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fd2e6-152">См. также</span><span class="sxs-lookup"><span data-stu-id="fd2e6-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd2e6-153">Знакомство с платформой Windows Ribbon</span><span class="sxs-lookup"><span data-stu-id="fd2e6-153">Introducing the Windows Ribbon Framework</span></span>](windowsribbon-introduction.md)
</dt> <dt>

[<span data-ttu-id="fd2e6-154">Создание приложения для ленты</span><span class="sxs-lookup"><span data-stu-id="fd2e6-154">Creating a Ribbon Application</span></span>](windowsribbon-stepbystep.md)
</dt> <dt>

[<span data-ttu-id="fd2e6-155">Объявление команд и элементов управления с разметкой ленты</span><span class="sxs-lookup"><span data-stu-id="fd2e6-155">Declaring Commands and Controls with Ribbon Markup</span></span>](windowsribbon-schema.md)
</dt> </dl>

 

 