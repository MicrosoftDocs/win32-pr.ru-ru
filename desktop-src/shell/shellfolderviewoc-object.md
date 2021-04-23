---
description: Перенаправляет события, инициируемые указанным объектом Шеллфолдервиев, в соответствующие обработчики событий Шеллфолдервиевок.
title: Объект Шеллфолдервиевок (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b50f549c-a79d-4411-a18e-a181b4b924e3
ms.openlocfilehash: b9a2b76f48731bf4c7b515779122503fa2cb02f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999269"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="fb748-103">Объект Шеллфолдервиевок</span><span class="sxs-lookup"><span data-stu-id="fb748-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="fb748-104">Перенаправляет события, инициируемые указанным объектом [**шеллфолдервиев**](shellfolderview.md) , в соответствующие обработчики событий **шеллфолдервиевок** .</span><span class="sxs-lookup"><span data-stu-id="fb748-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="fb748-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="fb748-105">Members</span></span>

<span data-ttu-id="fb748-106">Объект **шеллфолдервиевок** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fb748-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="fb748-107">События</span><span class="sxs-lookup"><span data-stu-id="fb748-107">Events</span></span>](#events)
-   [<span data-ttu-id="fb748-108">Методы</span><span class="sxs-lookup"><span data-stu-id="fb748-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="fb748-109">События</span><span class="sxs-lookup"><span data-stu-id="fb748-109">Events</span></span>

<span data-ttu-id="fb748-110">Объект **шеллфолдервиевок** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="fb748-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="fb748-111">Событие</span><span class="sxs-lookup"><span data-stu-id="fb748-111">Event</span></span>                                                          | <span data-ttu-id="fb748-112">Описание</span><span class="sxs-lookup"><span data-stu-id="fb748-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb748-113">**енумдоне**</span><span class="sxs-lookup"><span data-stu-id="fb748-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="fb748-114">Указывает, что объект [**шеллфолдервиев**](shellfolderview.md) завершил перечисление содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="fb748-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="fb748-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="fb748-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="fb748-116">Указывает, что состояние выбора одного или нескольких элементов в представлении изменилось.</span><span class="sxs-lookup"><span data-stu-id="fb748-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="fb748-117">Методы</span><span class="sxs-lookup"><span data-stu-id="fb748-117">Methods</span></span>

<span data-ttu-id="fb748-118">Объект **шеллфолдервиевок** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="fb748-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="fb748-119">Метод</span><span class="sxs-lookup"><span data-stu-id="fb748-119">Method</span></span>                                                   | <span data-ttu-id="fb748-120">Описание</span><span class="sxs-lookup"><span data-stu-id="fb748-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb748-121">**сетфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="fb748-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="fb748-122">Перенаправляет события указанного объекта [**шеллфолдервиев**](shellfolderview.md) в соответствующий обработчик событий **шеллфолдервиевок** .</span><span class="sxs-lookup"><span data-stu-id="fb748-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fb748-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="fb748-123">Remarks</span></span>

<span data-ttu-id="fb748-124">Объект [**шеллфолдервиев**](shellfolderview.md) запускает два события, [**енумдоне**](shellfolderviewoc-enumdone.md) и [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), которые обычно обрабатываются приложениями.</span><span class="sxs-lookup"><span data-stu-id="fb748-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="fb748-125">Однако некоторые приложения должны выполнять обработку событий из ряда объектов **шеллфолдервиев** .</span><span class="sxs-lookup"><span data-stu-id="fb748-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="fb748-126">Например, в приложении может размещаться элемент управления WebBrowser, позволяющий пользователям перемещаться по ряду папок.</span><span class="sxs-lookup"><span data-stu-id="fb748-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="fb748-127">Каждая папка имеет собственный объект **шеллфолдервиев** со связанными событиями.</span><span class="sxs-lookup"><span data-stu-id="fb748-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="fb748-128">Обработка этих событий может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="fb748-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="fb748-129">Объект **шеллфолдервиевок** упрощает обработку событий для таких сценариев.</span><span class="sxs-lookup"><span data-stu-id="fb748-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="fb748-130">Он позволяет приложениям выполнять обработку событий для всех объектов [**шеллфолдервиев**](shellfolderview.md) с помощью одной пары обработчиков событий **шеллфолдервиевок** .</span><span class="sxs-lookup"><span data-stu-id="fb748-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="fb748-131">Каждый раз, когда пользователь переходит к новой папке, приложение передает связанный объект **шеллфолдервиев** объекту **шеллфолдервиевок** , вызывая [**сетфолдервиев**](shellfolderviewoc-setfolderview.md).</span><span class="sxs-lookup"><span data-stu-id="fb748-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="fb748-132">Затем при срабатывании события [**енумдоне**](shellfolderviewoc-enumdone.md) или [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) объект **шеллфолдервиевок** перенаправляет событие в собственный обработчик для обработки.</span><span class="sxs-lookup"><span data-stu-id="fb748-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb748-133">Требования</span><span class="sxs-lookup"><span data-stu-id="fb748-133">Requirements</span></span>



| <span data-ttu-id="fb748-134">Требование</span><span class="sxs-lookup"><span data-stu-id="fb748-134">Requirement</span></span> | <span data-ttu-id="fb748-135">Значение</span><span class="sxs-lookup"><span data-stu-id="fb748-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb748-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb748-136">Minimum supported client</span></span><br/> | <span data-ttu-id="fb748-137">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fb748-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fb748-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb748-138">Minimum supported server</span></span><br/> | <span data-ttu-id="fb748-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fb748-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fb748-140">Header</span><span class="sxs-lookup"><span data-stu-id="fb748-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="fb748-141"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb748-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="fb748-142">IDL</span><span class="sxs-lookup"><span data-stu-id="fb748-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="fb748-143"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="fb748-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="fb748-144">DLL</span><span class="sxs-lookup"><span data-stu-id="fb748-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb748-145"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="fb748-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb748-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb748-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb748-147">**шеллфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="fb748-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




