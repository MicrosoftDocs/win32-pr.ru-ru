---
title: иажентнотифисинк
description: иажентнотифисинк
ms.assetid: vs|msagent|~\paface_2xet.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb2ccfd4acf4a64c229379aeea5847fbe044b7d5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069926"
---
# <a name="iagentnotifysink"></a><span data-ttu-id="b9a60-103">иажентнотифисинк</span><span class="sxs-lookup"><span data-stu-id="b9a60-103">IAgentNotifySink</span></span>

<span data-ttu-id="b9a60-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b9a60-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="b9a60-105">Иажентнотифисинк уведомляет клиентов при возникновении определенных изменений состояния.</span><span class="sxs-lookup"><span data-stu-id="b9a60-105">IAgentNotifySink notifies clients when certain state changes occur.</span></span> <span data-ttu-id="b9a60-106">Эти функции также доступны из [иажентнотифисинкекс](iagentnotifysinkex.md).</span><span class="sxs-lookup"><span data-stu-id="b9a60-106">These functions are also available from [IAgentNotifySinkEx](iagentnotifysinkex.md).</span></span>

<span data-ttu-id="b9a60-107">**Методы в порядке таблицы Vtable**</span><span class="sxs-lookup"><span data-stu-id="b9a60-107">**Methods in Vtable Order**</span></span>



| <span data-ttu-id="b9a60-108">иажентнотифисинк</span><span class="sxs-lookup"><span data-stu-id="b9a60-108">IAgentNotifySink</span></span>                                                      | <span data-ttu-id="b9a60-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b9a60-109">Description</span></span>                                                                              |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b9a60-110">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="b9a60-110">**Command**</span></span>](command-method.md)                                     | <span data-ttu-id="b9a60-111">Происходит, когда сервер обрабатывает команду, определяемую клиентом.</span><span class="sxs-lookup"><span data-stu-id="b9a60-111">Occurs when the server processes a client-defined command.</span></span>                               |
| [<span data-ttu-id="b9a60-112">**активатеинпутстате**</span><span class="sxs-lookup"><span data-stu-id="b9a60-112">**ActivateInputState**</span></span>](iagentnotifysink--activateinputstate.md)    | <span data-ttu-id="b9a60-113">Происходит, когда символ попадает в активное значение или перестает быть активным.</span><span class="sxs-lookup"><span data-stu-id="b9a60-113">Occurs when a character becomes or ceases to be input-active.</span></span>                            |
| [<span data-ttu-id="b9a60-114">**баллунвисиблестате**</span><span class="sxs-lookup"><span data-stu-id="b9a60-114">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="b9a60-115">Происходит при изменении **видимого** состояния символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-115">Occurs when the character's **Visible** state changes.</span></span>                                   |
| [<span data-ttu-id="b9a60-116">**Событие "Щелчок"**</span><span class="sxs-lookup"><span data-stu-id="b9a60-116">**Click Event**</span></span>](click-event.md)                                    | <span data-ttu-id="b9a60-117">Происходит при щелчке символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-117">Occurs when a character is clicked.</span></span>                                                      |
| [<span data-ttu-id="b9a60-118">**Двойное событие**</span><span class="sxs-lookup"><span data-stu-id="b9a60-118">**DblClick Event**</span></span>](dblclick-event.md)                              | <span data-ttu-id="b9a60-119">Происходит при двойном щелчке символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-119">Occurs when a character is double-clicked.</span></span>                                               |
| [<span data-ttu-id="b9a60-120">**драгстарт**</span><span class="sxs-lookup"><span data-stu-id="b9a60-120">**DragStart**</span></span>](/windows/desktop/lwef/dragstart-event)                                | <span data-ttu-id="b9a60-121">Происходит, когда пользователь начинает перетаскивать символ.</span><span class="sxs-lookup"><span data-stu-id="b9a60-121">Occurs when a user starts dragging a character.</span></span>                                          |
| [<span data-ttu-id="b9a60-122">**драгкомплете**</span><span class="sxs-lookup"><span data-stu-id="b9a60-122">**DragComplete**</span></span>](https://www.bing.com/search?q=**DragComplete**)                          | <span data-ttu-id="b9a60-123">Происходит, когда пользователь останавливает перетаскивание символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-123">Occurs when a user stops dragging a character.</span></span>                                           |
| [<span data-ttu-id="b9a60-124">**RequestStart**</span><span class="sxs-lookup"><span data-stu-id="b9a60-124">**RequestStart**</span></span>](iagentnotifysink--requeststart.md)                | <span data-ttu-id="b9a60-125">Происходит, когда сервер начинает обработку объекта [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b9a60-125">Occurs when the server begins processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span>    |
| [<span data-ttu-id="b9a60-126">**рекуесткомплете**</span><span class="sxs-lookup"><span data-stu-id="b9a60-126">**RequestComplete**</span></span>](iagentnotifysink--requestcomplete.md)          | <span data-ttu-id="b9a60-127">Происходит, когда сервер завершает обработку объекта [**запроса**](/windows/desktop/lwef/the-request-object) .</span><span class="sxs-lookup"><span data-stu-id="b9a60-127">Occurs when the server completes processing a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> |
| [<span data-ttu-id="b9a60-128">**Закладка**</span><span class="sxs-lookup"><span data-stu-id="b9a60-128">**Bookmark**</span></span>](iagentnotifysink--bookmark.md)                        | <span data-ttu-id="b9a60-129">Происходит, когда сервер обрабатывает закладку.</span><span class="sxs-lookup"><span data-stu-id="b9a60-129">Occurs when the server processes a bookmark.</span></span>                                             |
| [<span data-ttu-id="b9a60-130">**Выключен**</span><span class="sxs-lookup"><span data-stu-id="b9a60-130">**Idle**</span></span>](iagentnotifysink--idle.md)                                | <span data-ttu-id="b9a60-131">Происходит, когда сервер запускает или завершает обработку бездействия.</span><span class="sxs-lookup"><span data-stu-id="b9a60-131">Occurs when the server starts or ends idle processing.</span></span>                                   |
| [<span data-ttu-id="b9a60-132">**Переместить**</span><span class="sxs-lookup"><span data-stu-id="b9a60-132">**Move**</span></span>](iagentnotifysink--move.md)                                | <span data-ttu-id="b9a60-133">Происходит при перемещении символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-133">Occurs when a character has been moved.</span></span>                                                  |
| [<span data-ttu-id="b9a60-134">**Размер**</span><span class="sxs-lookup"><span data-stu-id="b9a60-134">**Size**</span></span>](iagentnotifysink---size.md)                               | <span data-ttu-id="b9a60-135">Происходит при изменении размера символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-135">Occurs when a character has been resized.</span></span>                                                |
| [<span data-ttu-id="b9a60-136">**баллунвисиблестате**</span><span class="sxs-lookup"><span data-stu-id="b9a60-136">**BalloonVisibleState**</span></span>](iagentnotifysink---balloonvisiblestate.md) | <span data-ttu-id="b9a60-137">Происходит при изменении состояния видимости для всплывающего слова символа.</span><span class="sxs-lookup"><span data-stu-id="b9a60-137">Occurs when the visibility state of a character's word balloon changes.</span></span>                  |



 

<span data-ttu-id="b9a60-138">События Иажентнотифисинк:: Restart и Иажентнотифисинк:: Shutdown, поддерживаемые в более ранних версиях Microsoft Agent, теперь устарели.</span><span class="sxs-lookup"><span data-stu-id="b9a60-138">The IAgentNotifySink::Restart and IAgentNotifySink::Shutdown events, supported in earlier versions of Microsoft Agent, are now obsolete.</span></span> <span data-ttu-id="b9a60-139">Так как поддерживается для обратной совместимости, сервер больше не отправляет эти события.</span><span class="sxs-lookup"><span data-stu-id="b9a60-139">While supported for backward compatibility, the server no longer sends these events.</span></span>

 

 