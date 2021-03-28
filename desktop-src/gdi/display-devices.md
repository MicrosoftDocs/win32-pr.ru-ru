---
description: Перед вырисовкой система должна подготовить устройство отображения для операций рисования.
ms.assetid: a3802aa7-deec-4151-b1b1-4cd38f769864
title: Отображение устройств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6df9e5e1746f309f402b31e736c58092d134d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984989"
---
# <a name="display-devices"></a><span data-ttu-id="52b15-103">Отображение устройств</span><span class="sxs-lookup"><span data-stu-id="52b15-103">Display Devices</span></span>

<span data-ttu-id="52b15-104">Перед вырисовкой система должна подготовить устройство отображения для операций рисования.</span><span class="sxs-lookup"><span data-stu-id="52b15-104">Before painting, the system must prepare the display device for drawing operations.</span></span> <span data-ttu-id="52b15-105">Контекст устройства отображения определяет набор графических объектов и связанных с ними атрибутов, а также графические режимы, влияющие на выходные данные.</span><span class="sxs-lookup"><span data-stu-id="52b15-105">A display device context defines a set of graphic objects and their associated attributes, and the graphic modes that affect output.</span></span> <span data-ttu-id="52b15-106">Система подготавливает контекст каждого устройства отображения для вывода в окне, устанавливая графические объекты, цвета и режимы для окна, а не устройства отображения.</span><span class="sxs-lookup"><span data-stu-id="52b15-106">The system prepares each display device context for output to a window, setting the drawing objects, colors, and modes for the window instead of the display device.</span></span> <span data-ttu-id="52b15-107">Когда приложение предоставляет контекст устройства отображения с помощью вызовов функций GDI, GDI использует информацию в контексте для создания выходных данных в указанном окне без каких-либо поатак на другие окна или другие части экрана.</span><span class="sxs-lookup"><span data-stu-id="52b15-107">When the application supplies the display device context through calls to GDI functions, GDI uses the information in the context to generate output in the specified window without intruding on other windows or other parts of the screen.</span></span>

<span data-ttu-id="52b15-108">Система предоставляет пять типов контекстов устройств вывода.</span><span class="sxs-lookup"><span data-stu-id="52b15-108">The system provides five kinds of display device contexts.</span></span>



| <span data-ttu-id="52b15-109">Тип</span><span class="sxs-lookup"><span data-stu-id="52b15-109">Type</span></span>                                           | <span data-ttu-id="52b15-110">Значение</span><span class="sxs-lookup"><span data-stu-id="52b15-110">Meaning</span></span>                                                                                                                                                          |
|------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="52b15-111">разделяем</span><span class="sxs-lookup"><span data-stu-id="52b15-111">common</span></span>](common-display-device-contexts.md)   | <span data-ttu-id="52b15-112">Разрешает прорисовку в клиентской области указанного окна.</span><span class="sxs-lookup"><span data-stu-id="52b15-112">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="52b15-113">class</span><span class="sxs-lookup"><span data-stu-id="52b15-113">class</span></span>](class-display-device-contexts.md)     | <span data-ttu-id="52b15-114">Разрешает прорисовку в клиентской области указанного окна.</span><span class="sxs-lookup"><span data-stu-id="52b15-114">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="52b15-115">parent</span><span class="sxs-lookup"><span data-stu-id="52b15-115">parent</span></span>](parent-display-device-contexts.md)   | <span data-ttu-id="52b15-116">Разрешает рисование в любом месте окна.</span><span class="sxs-lookup"><span data-stu-id="52b15-116">Permits drawing anywhere in the window.</span></span> <span data-ttu-id="52b15-117">Хотя родительский контекст устройства также разрешает прорисовку в родительском окне, он не предназначен для использования таким способом.</span><span class="sxs-lookup"><span data-stu-id="52b15-117">Although the parent device context also permits drawing in the parent window, it is not intended to be used in this way.</span></span> |
| [<span data-ttu-id="52b15-118">private</span><span class="sxs-lookup"><span data-stu-id="52b15-118">private</span></span>](private-display-device-contexts.md) | <span data-ttu-id="52b15-119">Разрешает прорисовку в клиентской области указанного окна.</span><span class="sxs-lookup"><span data-stu-id="52b15-119">Permits drawing in the client area of a specified window.</span></span>                                                                                                        |
| [<span data-ttu-id="52b15-120">окно</span><span class="sxs-lookup"><span data-stu-id="52b15-120">window</span></span>](window-display-device-contexts.md)   | <span data-ttu-id="52b15-121">Разрешает рисование в любом месте окна.</span><span class="sxs-lookup"><span data-stu-id="52b15-121">Permits drawing anywhere in the window.</span></span>                                                                                                                          |



 

<span data-ttu-id="52b15-122">Система предоставляет доступ к общему, классу, родительскому или частному контексту устройства для окна на основе типа контекста дисплея, указанного в стиле класса этого окна.</span><span class="sxs-lookup"><span data-stu-id="52b15-122">The system supplies a common, class, parent, or private device context to a window based on the type of display device context specified in that window's class style.</span></span> <span data-ttu-id="52b15-123">Система предоставляет контекст устройства окна только в том случае, если приложение явно запрашивает один из них, вызывая функцию [**жетвиндовдк**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) или [**жетдцекс**](/windows/desktop/api/Winuser/nf-winuser-getdcex) .</span><span class="sxs-lookup"><span data-stu-id="52b15-123">The system supplies a window device context only when the application explicitly requests one for example, by calling the [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) or [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) function.</span></span> <span data-ttu-id="52b15-124">Во всех случаях приложение может использовать функцию [**виндовфромдк**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) , чтобы определить, какое окно в настоящее время представляет контроллер домена.</span><span class="sxs-lookup"><span data-stu-id="52b15-124">In all cases, an application can use the [**WindowFromDC**](/windows/desktop/api/Winuser/nf-winuser-windowfromdc) function to determine which window a display DC currently represents.</span></span>

<span data-ttu-id="52b15-125">В этом разделе содержатся сведения по следующим темам.</span><span class="sxs-lookup"><span data-stu-id="52b15-125">This section provides information on the following topics.</span></span>

-   [<span data-ttu-id="52b15-126">Отображение кэша контекста устройства</span><span class="sxs-lookup"><span data-stu-id="52b15-126">Display Device Context Cache</span></span>](display-device-context-cache.md)
-   [<span data-ttu-id="52b15-127">Отображать значения по умолчанию для контекста устройства</span><span class="sxs-lookup"><span data-stu-id="52b15-127">Display Device Context Defaults</span></span>](display-device-context-defaults.md)
-   [<span data-ttu-id="52b15-128">Общие контексты отображаемых устройств</span><span class="sxs-lookup"><span data-stu-id="52b15-128">Common Display Device Contexts</span></span>](common-display-device-contexts.md)
-   [<span data-ttu-id="52b15-129">Контексты частных устройств просмотра</span><span class="sxs-lookup"><span data-stu-id="52b15-129">Private Display Device Contexts</span></span>](private-display-device-contexts.md)
-   [<span data-ttu-id="52b15-130">Контексты отображаемых родительских устройств</span><span class="sxs-lookup"><span data-stu-id="52b15-130">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)
-   [<span data-ttu-id="52b15-131">Отображение контекстов устройств в классе</span><span class="sxs-lookup"><span data-stu-id="52b15-131">Class Display Device Contexts</span></span>](class-display-device-contexts.md)
-   [<span data-ttu-id="52b15-132">Контексты дисплея окна</span><span class="sxs-lookup"><span data-stu-id="52b15-132">Window Display Device Contexts</span></span>](window-display-device-contexts.md)
-   [<span data-ttu-id="52b15-133">Контексты отображаемых родительских устройств</span><span class="sxs-lookup"><span data-stu-id="52b15-133">Parent Display Device Contexts</span></span>](parent-display-device-contexts.md)

 

 



