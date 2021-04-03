---
title: Использование COM в приложении Windows
description: В модуле 1 этой серии показано, как создать окно и отреагировать на сообщения окон, такие как WM \_ Paint и WM \_ Close. В модуле 2 представлена объектная модель компонента (COM).
ms.assetid: 6e867618-4d02-4c17-b7ea-dc7290507689
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c03f16937846c4479a70e16141f1b50bde3efc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791364"
---
# <a name="module-2-using-com-in-your-windows-based-program"></a><span data-ttu-id="aa526-104">Модуль 2.</span><span class="sxs-lookup"><span data-stu-id="aa526-104">Module 2.</span></span> <span data-ttu-id="aa526-105">Использование COM в программе Windows-Based</span><span class="sxs-lookup"><span data-stu-id="aa526-105">Using COM in Your Windows-Based Program</span></span>

<span data-ttu-id="aa526-106">В [модуле 1](your-first-windows-program.md) этой серии показано, как создать окно и отреагировать на сообщения окон, такие как [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) и [**WM \_ Close**](/windows/desktop/winmsg/wm-close).</span><span class="sxs-lookup"><span data-stu-id="aa526-106">[Module 1](your-first-windows-program.md) of this series showed how to create a window and respond to window messages such as [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) and [**WM\_CLOSE**](/windows/desktop/winmsg/wm-close).</span></span> <span data-ttu-id="aa526-107">В модуле 2 представлена объектная модель компонента (COM).</span><span class="sxs-lookup"><span data-stu-id="aa526-107">Module 2 introduces the Component Object Model (COM).</span></span>

<span data-ttu-id="aa526-108">COM — это спецификация для создания многократно используемых программных компонентов.</span><span class="sxs-lookup"><span data-stu-id="aa526-108">COM is a specification for creating reusable software components.</span></span> <span data-ttu-id="aa526-109">Многие функции, которые будут использоваться в современной программе на базе Windows, полагаются на модель COM, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="aa526-109">Many of the features that you will use in a modern Windows-based program rely on COM, such as the following:</span></span>

-   <span data-ttu-id="aa526-110">Графика (Direct2D)</span><span class="sxs-lookup"><span data-stu-id="aa526-110">Graphics (Direct2D)</span></span>
-   <span data-ttu-id="aa526-111">Текст (DirectWrite)</span><span class="sxs-lookup"><span data-stu-id="aa526-111">Text (DirectWrite)</span></span>
-   <span data-ttu-id="aa526-112">Оболочка Windows</span><span class="sxs-lookup"><span data-stu-id="aa526-112">The Windows Shell</span></span>
-   <span data-ttu-id="aa526-113">Элемент управления ленты</span><span class="sxs-lookup"><span data-stu-id="aa526-113">The Ribbon control</span></span>
-   <span data-ttu-id="aa526-114">Анимация пользовательского интерфейса</span><span class="sxs-lookup"><span data-stu-id="aa526-114">UI animation</span></span>

<span data-ttu-id="aa526-115">(Некоторые технологии в этом списке используют подмножество COM и, следовательно, не являются "чистыми" COM.)</span><span class="sxs-lookup"><span data-stu-id="aa526-115">(Some technologies on this list use a subset of COM and are therefore not "pure" COM.)</span></span>

<span data-ttu-id="aa526-116">У COM есть репутация, которую трудно изучить.</span><span class="sxs-lookup"><span data-stu-id="aa526-116">COM has a reputation for being difficult to learn.</span></span> <span data-ttu-id="aa526-117">И потому, что написание нового программного модуля для поддержки COM может быть непростой задачей.</span><span class="sxs-lookup"><span data-stu-id="aa526-117">And it is true that writing a new software module to support COM can be tricky.</span></span> <span data-ttu-id="aa526-118">Но если ваша программа является исключительно *потребителем* com, вы можете обнаружить, что модель COM проще понять, чем вы планируете.</span><span class="sxs-lookup"><span data-stu-id="aa526-118">But if your program is strictly a *consumer* of COM, you may find that COM is easier to understand than you expect.</span></span>

<span data-ttu-id="aa526-119">Этот модуль показывает, как вызывать интерфейсы API на основе COM в программе.</span><span class="sxs-lookup"><span data-stu-id="aa526-119">This module shows how to call COM-based APIs in your program.</span></span> <span data-ttu-id="aa526-120">В нем также описываются некоторые причины разработки модели COM.</span><span class="sxs-lookup"><span data-stu-id="aa526-120">It also describes some of the reasoning behind the design of COM.</span></span> <span data-ttu-id="aa526-121">Если вы понимаете, почему модель COM разработана как есть, ее можно программировать более эффективно.</span><span class="sxs-lookup"><span data-stu-id="aa526-121">If you understand why COM is designed as it is, you can program with it more effectively.</span></span> <span data-ttu-id="aa526-122">Вторая часть модуля описывает некоторые рекомендуемые методы программирования для COM.</span><span class="sxs-lookup"><span data-stu-id="aa526-122">The second part of the module describes some recommended programming practices for COM.</span></span>

<span data-ttu-id="aa526-123">COM был представлен в 1993 для поддержки связывания и внедрения объектов (OLE) 2,0.</span><span class="sxs-lookup"><span data-stu-id="aa526-123">COM was introduced in 1993 to support Object Linking and Embedding (OLE) 2.0.</span></span> <span data-ttu-id="aa526-124">Иногда люди считают, что COM и OLE одинаковы.</span><span class="sxs-lookup"><span data-stu-id="aa526-124">People sometimes think that COM and OLE are the same thing.</span></span> <span data-ttu-id="aa526-125">Это может быть еще одна причина, по которой трудно изучить Модель COM.</span><span class="sxs-lookup"><span data-stu-id="aa526-125">This may be another reason for the perception that COM is difficult to learn.</span></span> <span data-ttu-id="aa526-126">OLE 2,0 построена на основе COM, но вам не нужно знать OLE для понимания COM.</span><span class="sxs-lookup"><span data-stu-id="aa526-126">OLE 2.0 is built on COM, but you do not have to know OLE to understand COM.</span></span>

<span data-ttu-id="aa526-127">COM — это *двоичный стандарт*, а не стандартный язык: он определяет двоичный интерфейс между приложением и программным компонентом.</span><span class="sxs-lookup"><span data-stu-id="aa526-127">COM is a *binary standard*, not a language standard: It defines the binary interface between an application and a software component.</span></span> <span data-ttu-id="aa526-128">Как двоичный стандарт, модель COM не зависит от языка, хотя она сопоставляется естественным образом с определенными конструкциями C++.</span><span class="sxs-lookup"><span data-stu-id="aa526-128">As a binary standard, COM is language-neutral, although it maps naturally to certain C++ constructs.</span></span> <span data-ttu-id="aa526-129">Этот модуль будет сосредоточиться на трех основных целях COM:</span><span class="sxs-lookup"><span data-stu-id="aa526-129">This module will focus on three major goals of COM:</span></span>

-   <span data-ttu-id="aa526-130">Отделение реализации объекта от его интерфейса.</span><span class="sxs-lookup"><span data-stu-id="aa526-130">Separating the implementation of an object from its interface.</span></span>
-   <span data-ttu-id="aa526-131">Управление жизненным циклом объекта.</span><span class="sxs-lookup"><span data-stu-id="aa526-131">Managing the lifetime of an object.</span></span>
-   <span data-ttu-id="aa526-132">Обнаружение возможностей объекта во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa526-132">Discovering the capabilities of an object at run time.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="aa526-133">Содержание раздела</span><span class="sxs-lookup"><span data-stu-id="aa526-133">In this section</span></span>

-   [<span data-ttu-id="aa526-134">Что такое COM-интерфейс?</span><span class="sxs-lookup"><span data-stu-id="aa526-134">What Is a COM Interface?</span></span>](what-is-a-com-interface-.md)
-   [<span data-ttu-id="aa526-135">Инициализация библиотеки COM</span><span class="sxs-lookup"><span data-stu-id="aa526-135">Initializing the COM Library</span></span>](initializing-the-com-library.md)
-   [<span data-ttu-id="aa526-136">Коды ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="aa526-136">Error Codes in COM</span></span>](error-codes-in-com.md)
-   [<span data-ttu-id="aa526-137">Создание объекта в COM</span><span class="sxs-lookup"><span data-stu-id="aa526-137">Creating an Object in COM</span></span>](creating-an-object-in-com.md)
-   [<span data-ttu-id="aa526-138">Пример. диалоговое окно "Открыть"</span><span class="sxs-lookup"><span data-stu-id="aa526-138">Example: The Open Dialog Box</span></span>](example--the-open-dialog-box.md)
-   [<span data-ttu-id="aa526-139">Управление жизненным циклом объекта</span><span class="sxs-lookup"><span data-stu-id="aa526-139">Managing the Lifetime of an Object</span></span>](managing-the-lifetime-of-an-object.md)
-   [<span data-ttu-id="aa526-140">Запрос объекта для интерфейса</span><span class="sxs-lookup"><span data-stu-id="aa526-140">Asking an Object for an Interface</span></span>](asking-an-object-for-an-interface.md)
-   [<span data-ttu-id="aa526-141">Выделение памяти в COM</span><span class="sxs-lookup"><span data-stu-id="aa526-141">Memory Allocation in COM</span></span>](memory-allocation-in-com.md)
-   [<span data-ttu-id="aa526-142">Методики программирования COM</span><span class="sxs-lookup"><span data-stu-id="aa526-142">COM Coding Practices</span></span>](com-coding-practices.md)
-   [<span data-ttu-id="aa526-143">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="aa526-143">Error Handling in COM</span></span>](error-handling-in-com.md)

## <a name="related-topics"></a><span data-ttu-id="aa526-144">См. также</span><span class="sxs-lookup"><span data-stu-id="aa526-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa526-145">Знакомство с программой для Windows в C++</span><span class="sxs-lookup"><span data-stu-id="aa526-145">Learn to Program for Windows in C++</span></span>](learn-to-program-for-windows.md)
</dt> </dl>

 

 