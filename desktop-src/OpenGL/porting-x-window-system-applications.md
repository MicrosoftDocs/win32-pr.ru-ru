---
title: Перенос системных приложений X Window
description: Перенос системных приложений X Window
ms.assetid: 730602f3-12af-430d-a105-0efdd3fd43b4
keywords:
- OpenGL в Windows, перенос
- Перенос на OpenGL, системное окно X
- Перенос по стандарту OpenGL, система Window X
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e52a06ffa458e07a70a7c4823e0291639d878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104258512"
---
# <a name="porting-x-window-system-applications"></a><span data-ttu-id="d0743-106">Перенос системных приложений X Window</span><span class="sxs-lookup"><span data-stu-id="d0743-106">Porting X Window System Applications</span></span>

<span data-ttu-id="d0743-107">Как и Windows, система Window X является системой обработки событий, основанной на сообщениях, которая использует элементы управления окна и меню.</span><span class="sxs-lookup"><span data-stu-id="d0743-107">Like Windows, the X Window System is an event-handling, message-based system that uses window controls and menus.</span></span> <span data-ttu-id="d0743-108">Код OpenGL в приложении X Window System, скорее всего, находится в областях, которые примерно соответствуют расположению, которое будет отображаться при переносе в Windows.</span><span class="sxs-lookup"><span data-stu-id="d0743-108">The OpenGL code in your X Window System application is probably located in areas that roughly correspond to where it will appear when you port it to Windows.</span></span> <span data-ttu-id="d0743-109">Большая часть кода OpenGL не изменится, но необходимо переписать код, относящийся к системе Window X.</span><span class="sxs-lookup"><span data-stu-id="d0743-109">Most of your OpenGL code will not change, but you must rewrite any code that is specific to the X Window System.</span></span>

<span data-ttu-id="d0743-110">**Используйте следующую общую процедуру, чтобы перенести системные программы OpenGL Window X в Windows**</span><span class="sxs-lookup"><span data-stu-id="d0743-110">**Use the following general procedure to port your X Window System OpenGL programs to Windows**</span></span>

1.  <span data-ttu-id="d0743-111">Перепишите Специальный код системы X Window с помощью эквивалентного кода Windows.</span><span class="sxs-lookup"><span data-stu-id="d0743-111">Rewrite the X Window System specific code using equivalent Windows code.</span></span> <span data-ttu-id="d0743-112">Нахождение кода для создания окон и обработки событий.</span><span class="sxs-lookup"><span data-stu-id="d0743-112">Locate window-creation and event-handling code.</span></span> <span data-ttu-id="d0743-113">Окна системы X и Windows — это системы обработки событий, основанные на сообщениях, которые упрощают определение места внесения соответствующих изменений.</span><span class="sxs-lookup"><span data-stu-id="d0743-113">The X Window System and Windows are event-handling, message-based windowing systems, which makes it easier to determine where to make the appropriate changes.</span></span> <span data-ttu-id="d0743-114">(Однако, особенно для больших приложений, перезапись приложения из одной операционной системы в другую может быть сложной и сложной.)</span><span class="sxs-lookup"><span data-stu-id="d0743-114">(However, especially for large applications, rewriting an application from one operating system to another can be a complex and difficult undertaking.)</span></span>
2.  <span data-ttu-id="d0743-115">Нахождение любого кода, использующего функции ГЛКС.</span><span class="sxs-lookup"><span data-stu-id="d0743-115">Locate any code that uses GLX functions.</span></span> <span data-ttu-id="d0743-116">Это функции, которые будут преобразованы в эквивалентные функции Windows.</span><span class="sxs-lookup"><span data-stu-id="d0743-116">These are the functions you'll translate to their equivalent Windows functions.</span></span>
3.  <span data-ttu-id="d0743-117">Преобразование функций формата пикселей ГЛКС и визуальных и нарисованных функций в соответствующий формат пикселей Windows/OpenGL и функции контекста устройства.</span><span class="sxs-lookup"><span data-stu-id="d0743-117">Translate GLX pixel format functions and Visual/Drawable functions to appropriate Windows/OpenGL pixel format and device context functions.</span></span>
4.  <span data-ttu-id="d0743-118">Преобразование функций контекста отрисовки ГЛКС в функции контекста отрисовки Windows или OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d0743-118">Translate GLX rendering context functions to Windows/OpenGL rendering context functions.</span></span>
5.  <span data-ttu-id="d0743-119">Преобразование функций ГЛКС Пиксмап в эквивалентные функции Windows.</span><span class="sxs-lookup"><span data-stu-id="d0743-119">Translate GLX Pixmap functions to equivalent Windows functions.</span></span>
6.  <span data-ttu-id="d0743-120">Преобразовывать ГЛКС буфера кадров и другие функции ГЛКС в соответствующие функции Windows.</span><span class="sxs-lookup"><span data-stu-id="d0743-120">Translate GLX framebuffer and other GLX functions to the appropriate Windows functions.</span></span>

 

 




