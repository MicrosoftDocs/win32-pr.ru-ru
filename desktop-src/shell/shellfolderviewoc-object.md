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
ms.openlocfilehash: 2670578417dc616d30f319887f5281fa5d0615f5
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840875"
---
# <a name="shellfolderviewoc-object"></a><span data-ttu-id="b64ed-103">Объект Шеллфолдервиевок</span><span class="sxs-lookup"><span data-stu-id="b64ed-103">ShellFolderViewOC object</span></span>

<span data-ttu-id="b64ed-104">Перенаправляет события, инициируемые указанным объектом [**шеллфолдервиев**](shellfolderview.md) , в соответствующие обработчики событий **шеллфолдервиевок** .</span><span class="sxs-lookup"><span data-stu-id="b64ed-104">Forwards the events fired by a specified [**ShellFolderView**](shellfolderview.md) object to corresponding **ShellFolderViewOC** event handlers.</span></span>

## <a name="members"></a><span data-ttu-id="b64ed-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="b64ed-105">Members</span></span>

<span data-ttu-id="b64ed-106">Объект **шеллфолдервиевок** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b64ed-106">The **ShellFolderViewOC** object has these types of members:</span></span>

-   [<span data-ttu-id="b64ed-107">События</span><span class="sxs-lookup"><span data-stu-id="b64ed-107">Events</span></span>](#events)
-   [<span data-ttu-id="b64ed-108">Методы</span><span class="sxs-lookup"><span data-stu-id="b64ed-108">Methods</span></span>](#methods)

### <a name="events"></a><span data-ttu-id="b64ed-109">События</span><span class="sxs-lookup"><span data-stu-id="b64ed-109">Events</span></span>

<span data-ttu-id="b64ed-110">Объект **шеллфолдервиевок** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="b64ed-110">The **ShellFolderViewOC** object has these events.</span></span>



| <span data-ttu-id="b64ed-111">Событие</span><span class="sxs-lookup"><span data-stu-id="b64ed-111">Event</span></span>                                                          | <span data-ttu-id="b64ed-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b64ed-112">Description</span></span>                                                                                                                     |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b64ed-113">**енумдоне**</span><span class="sxs-lookup"><span data-stu-id="b64ed-113">**EnumDone**</span></span>](shellfolderviewoc-enumdone.md)                 | <span data-ttu-id="b64ed-114">Указывает, что объект [**шеллфолдервиев**](shellfolderview.md) завершил перечисление содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="b64ed-114">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span><br/> |
| [<span data-ttu-id="b64ed-115">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="b64ed-115">**SelectionChanged**</span></span>](shellfolderviewoc-selectionchanged.md) | <span data-ttu-id="b64ed-116">Указывает, что состояние выбора одного или нескольких элементов в представлении изменилось.</span><span class="sxs-lookup"><span data-stu-id="b64ed-116">Indicates that the selection state of one or more items in the view has changed.</span></span><br/>                                     |



 

### <a name="methods"></a><span data-ttu-id="b64ed-117">Методы</span><span class="sxs-lookup"><span data-stu-id="b64ed-117">Methods</span></span>

<span data-ttu-id="b64ed-118">Объект **шеллфолдервиевок** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="b64ed-118">The **ShellFolderViewOC** object has these methods.</span></span>



| <span data-ttu-id="b64ed-119">Метод</span><span class="sxs-lookup"><span data-stu-id="b64ed-119">Method</span></span>                                                   | <span data-ttu-id="b64ed-120">Описание</span><span class="sxs-lookup"><span data-stu-id="b64ed-120">Description</span></span>                                                                                                                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b64ed-121">**сетфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="b64ed-121">**SetFolderView**</span></span>](shellfolderviewoc-setfolderview.md) | <span data-ttu-id="b64ed-122">Перенаправляет события указанного объекта [**шеллфолдервиев**](shellfolderview.md) в соответствующий обработчик событий **шеллфолдервиевок** .</span><span class="sxs-lookup"><span data-stu-id="b64ed-122">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding **ShellFolderViewOC** event handler.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b64ed-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="b64ed-123">Remarks</span></span>

<span data-ttu-id="b64ed-124">Объект [**шеллфолдервиев**](shellfolderview.md) запускает два события, [**енумдоне**](shellfolderviewoc-enumdone.md) и [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), которые обычно обрабатываются приложениями.</span><span class="sxs-lookup"><span data-stu-id="b64ed-124">The [**ShellFolderView**](shellfolderview.md) object fires two events, [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderviewoc-selectionchanged.md), that are typically handled by applications.</span></span> <span data-ttu-id="b64ed-125">Однако некоторые приложения должны выполнять обработку событий из ряда объектов **шеллфолдервиев** .</span><span class="sxs-lookup"><span data-stu-id="b64ed-125">However, some applications must handle events from a series of **ShellFolderView** objects.</span></span> <span data-ttu-id="b64ed-126">Например, в приложении может размещаться элемент управления WebBrowser, позволяющий пользователям перемещаться по ряду папок.</span><span class="sxs-lookup"><span data-stu-id="b64ed-126">For example, an application might host a WebBrowser control that allows users to navigate through a series of folders.</span></span> <span data-ttu-id="b64ed-127">Каждая папка имеет собственный объект **шеллфолдервиев** со связанными событиями.</span><span class="sxs-lookup"><span data-stu-id="b64ed-127">Each folder has its own **ShellFolderView** object with its associated events.</span></span> <span data-ttu-id="b64ed-128">Обработка этих событий может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="b64ed-128">Handling these events can be difficult.</span></span>

<span data-ttu-id="b64ed-129">Объект **шеллфолдервиевок** упрощает обработку событий для таких сценариев.</span><span class="sxs-lookup"><span data-stu-id="b64ed-129">The **ShellFolderViewOC** object simplifies event handling for such scenarios.</span></span> <span data-ttu-id="b64ed-130">Он позволяет приложениям выполнять обработку событий для всех объектов [**шеллфолдервиев**](shellfolderview.md) с помощью одной пары обработчиков событий **шеллфолдервиевок** .</span><span class="sxs-lookup"><span data-stu-id="b64ed-130">It allows applications to handle events for all [**ShellFolderView**](shellfolderview.md) objects with a single pair of **ShellFolderViewOC** event handlers.</span></span> <span data-ttu-id="b64ed-131">Каждый раз, когда пользователь переходит к новой папке, приложение передает связанный объект **шеллфолдервиев** объекту **шеллфолдервиевок** , вызывая [**сетфолдервиев**](shellfolderviewoc-setfolderview.md).</span><span class="sxs-lookup"><span data-stu-id="b64ed-131">Each time the user navigates to a new folder, the application passes the associated **ShellFolderView** object to the **ShellFolderViewOC** object by calling [**SetFolderView**](shellfolderviewoc-setfolderview.md).</span></span> <span data-ttu-id="b64ed-132">Затем при срабатывании события [**енумдоне**](shellfolderviewoc-enumdone.md) или [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) объект **шеллфолдервиевок** перенаправляет событие в собственный обработчик для обработки.</span><span class="sxs-lookup"><span data-stu-id="b64ed-132">Then, when an [**EnumDone**](shellfolderviewoc-enumdone.md) or [**SelectionChanged**](shellfolderviewoc-selectionchanged.md) event is fired, the **ShellFolderViewOC** object forwards the event to its own handler for processing.</span></span>

## <a name="requirements"></a><span data-ttu-id="b64ed-133">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="b64ed-133">Requirements</span></span>



| <span data-ttu-id="b64ed-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b64ed-134">Requirement</span></span> | <span data-ttu-id="b64ed-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b64ed-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b64ed-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b64ed-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b64ed-137">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b64ed-137">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b64ed-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b64ed-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b64ed-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b64ed-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b64ed-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b64ed-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b64ed-141"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="b64ed-141"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b64ed-142">IDL</span><span class="sxs-lookup"><span data-stu-id="b64ed-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b64ed-143"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b64ed-143"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b64ed-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b64ed-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b64ed-145"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="b64ed-145"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b64ed-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b64ed-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b64ed-147">**шеллфолдервиев**</span><span class="sxs-lookup"><span data-stu-id="b64ed-147">**ShellFolderView**</span></span>](shellfolderview.md)
</dt> </dl>

 

 




