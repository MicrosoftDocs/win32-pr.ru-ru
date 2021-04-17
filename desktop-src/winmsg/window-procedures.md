---
description: В этом разделе обсуждаются процедуры окна. Каждое окно имеет связанную процедуру окна, которая обрабатывает все сообщения, отправленные или опубликованные во всех окнах класса.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\windowprocedures.htm
title: Процедуры окна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ae68ba9b64557a6dc70d5c83788b8337648a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703036"
---
# <a name="window-procedures"></a><span data-ttu-id="41280-104">Процедуры окна</span><span class="sxs-lookup"><span data-stu-id="41280-104">Window Procedures</span></span>

<span data-ttu-id="41280-105">Каждое окно имеет связанную процедуру окна — функцию, которая обрабатывает все сообщения, отправленные или опубликованные во всех окнах класса.</span><span class="sxs-lookup"><span data-stu-id="41280-105">Every window has an associated window procedure — a function that processes all messages sent or posted to all windows of the class.</span></span> <span data-ttu-id="41280-106">Все аспекты внешнего вида и поведения окна зависят от ответа процедуры окна на эти сообщения.</span><span class="sxs-lookup"><span data-stu-id="41280-106">All aspects of a window's appearance and behavior depend on the window procedure's response to these messages.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="41280-107">в этом разделе</span><span class="sxs-lookup"><span data-stu-id="41280-107">In This Section</span></span>



| <span data-ttu-id="41280-108">Имя</span><span class="sxs-lookup"><span data-stu-id="41280-108">Name</span></span>                                                         | <span data-ttu-id="41280-109">Описание</span><span class="sxs-lookup"><span data-stu-id="41280-109">Description</span></span>                                                                                                                                                                                                    |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41280-110">О процедурах окна</span><span class="sxs-lookup"><span data-stu-id="41280-110">About Window Procedures</span></span>](about-window-procedures.md)       | <span data-ttu-id="41280-111">Описание процедур Windows.</span><span class="sxs-lookup"><span data-stu-id="41280-111">Discusses window procedures.</span></span> <span data-ttu-id="41280-112">Каждое окно является членом определенного класса Window.</span><span class="sxs-lookup"><span data-stu-id="41280-112">Each window is a member of a particular window class.</span></span> <span data-ttu-id="41280-113">Класс Window определяет процедуру окна по умолчанию, используемую отдельным окном для обработки сообщений.</span><span class="sxs-lookup"><span data-stu-id="41280-113">The window class determines the default window procedure that an individual window uses to process its messages.</span></span><br/> |
| [<span data-ttu-id="41280-114">Использование оконных процедур</span><span class="sxs-lookup"><span data-stu-id="41280-114">Using Window Procedures</span></span>](using-window-procedures.md)       | <span data-ttu-id="41280-115">Описывает выполнение следующих задач, связанных с процедурами окон.</span><span class="sxs-lookup"><span data-stu-id="41280-115">Covers how to perform the following tasks associated with window procedures.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="41280-116">Справочник по процедурам окна</span><span class="sxs-lookup"><span data-stu-id="41280-116">Window Procedure Reference</span></span>](window-procedure-reference.md) | <span data-ttu-id="41280-117">Содержит справочник по API.</span><span class="sxs-lookup"><span data-stu-id="41280-117">Contains the API reference.</span></span><br/>                                                                                                                                                                         |



 

### <a name="functions"></a><span data-ttu-id="41280-118">Функции</span><span class="sxs-lookup"><span data-stu-id="41280-118">Functions</span></span>



| <span data-ttu-id="41280-119">Имя</span><span class="sxs-lookup"><span data-stu-id="41280-119">Name</span></span>                                     | <span data-ttu-id="41280-120">Описание</span><span class="sxs-lookup"><span data-stu-id="41280-120">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41280-121">**каллвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="41280-121">**CallWindowProc**</span></span>](/windows/win32/api/winuser/nf-winuser-callwindowproca) | <span data-ttu-id="41280-122">Передает сведения о сообщении в указанную процедуру окна.</span><span class="sxs-lookup"><span data-stu-id="41280-122">Passes message information to the specified window procedure.</span></span> <br/>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="41280-123">**дефвиндовпрок**</span><span class="sxs-lookup"><span data-stu-id="41280-123">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)   | <span data-ttu-id="41280-124">Вызывает процедуру окна по умолчанию, чтобы обеспечить обработку по умолчанию для любых сообщений окон, которые не обрабатываются приложением.</span><span class="sxs-lookup"><span data-stu-id="41280-124">Calls the default window procedure to provide default processing for any window messages that an application does not process.</span></span> <span data-ttu-id="41280-125">Эта функция гарантирует, что каждое сообщение будет обработано.</span><span class="sxs-lookup"><span data-stu-id="41280-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="41280-126">[**Дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) вызывается с теми же параметрами, которые были получены процедурой окна.</span><span class="sxs-lookup"><span data-stu-id="41280-126">[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) is called with the same parameters received by the window procedure.</span></span> <br/> |
| <span data-ttu-id="41280-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="41280-127">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))</span></span>           | <span data-ttu-id="41280-128">Определяемая приложением функция, которая обрабатывает сообщения, отправляемые в окно.</span><span class="sxs-lookup"><span data-stu-id="41280-128">An application-defined function that processes messages sent to a window.</span></span> <span data-ttu-id="41280-129">Тип **WndProc** определяет указатель на эту функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="41280-129">The **WNDPROC** type defines a pointer to this callback function.</span></span> <span data-ttu-id="41280-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) — это заполнитель для имени определяемой приложением функции.</span><span class="sxs-lookup"><span data-stu-id="41280-130">[*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) is a placeholder for the application-defined function name.</span></span> <br/>                                                            |



 

 

 
