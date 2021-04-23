---
description: Представляет объекты в представлении и предоставляет свойства и методы, используемые для получения сведений о содержимом представления.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Объект Шеллфолдервиев (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997866"
---
# <a name="shellfolderview-object"></a><span data-ttu-id="496c4-103">Объект Шеллфолдервиев</span><span class="sxs-lookup"><span data-stu-id="496c4-103">ShellFolderView object</span></span>

<span data-ttu-id="496c4-104">Представляет объекты в представлении и предоставляет свойства и методы, используемые для получения сведений о содержимом представления.</span><span class="sxs-lookup"><span data-stu-id="496c4-104">Represents the objects in a view and provides properties and methods used to obtain information about the contents of the view.</span></span>

## <a name="members"></a><span data-ttu-id="496c4-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="496c4-105">Members</span></span>

<span data-ttu-id="496c4-106">Объект **шеллфолдервиев** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="496c4-106">The **ShellFolderView** object has these types of members:</span></span>

-   [<span data-ttu-id="496c4-107">События</span><span class="sxs-lookup"><span data-stu-id="496c4-107">Events</span></span>](#events)
-   [<span data-ttu-id="496c4-108">Методы</span><span class="sxs-lookup"><span data-stu-id="496c4-108">Methods</span></span>](#methods)
-   [<span data-ttu-id="496c4-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="496c4-109">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="496c4-110">События</span><span class="sxs-lookup"><span data-stu-id="496c4-110">Events</span></span>

<span data-ttu-id="496c4-111">Объект **шеллфолдервиев** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="496c4-111">The **ShellFolderView** object has these events.</span></span>



| <span data-ttu-id="496c4-112">Событие</span><span class="sxs-lookup"><span data-stu-id="496c4-112">Event</span></span>                                                        | <span data-ttu-id="496c4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="496c4-113">Description</span></span>                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="496c4-114">**SelectionChanged**</span><span class="sxs-lookup"><span data-stu-id="496c4-114">**SelectionChanged**</span></span>](shellfolderview-selectionchanged.md) | <span data-ttu-id="496c4-115">Происходит при изменении состояния выбора любого элемента или элементов в представлении.</span><span class="sxs-lookup"><span data-stu-id="496c4-115">Occurs when the selection state of any item or items in the view has changed.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="496c4-116">Методы</span><span class="sxs-lookup"><span data-stu-id="496c4-116">Methods</span></span>

<span data-ttu-id="496c4-117">Объект **шеллфолдервиев** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="496c4-117">The **ShellFolderView** object has these methods.</span></span>



| <span data-ttu-id="496c4-118">Метод</span><span class="sxs-lookup"><span data-stu-id="496c4-118">Method</span></span>                                                 | <span data-ttu-id="496c4-119">Описание</span><span class="sxs-lookup"><span data-stu-id="496c4-119">Description</span></span>                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="496c4-120">**попупитеммену**</span><span class="sxs-lookup"><span data-stu-id="496c4-120">**PopupItemMenu**</span></span>](shellfolderview-popupitemmenu.md) | <span data-ttu-id="496c4-121">Создает контекстное меню для указанного элемента и возвращает выбранную командную строку.</span><span class="sxs-lookup"><span data-stu-id="496c4-121">Creates a shortcut menu for the specified item and returns the selected command string.</span></span><br/>                 |
| [<span data-ttu-id="496c4-122">**SelectedItems**</span><span class="sxs-lookup"><span data-stu-id="496c4-122">**SelectedItems**</span></span>](shellfolderview-selecteditems.md) | <span data-ttu-id="496c4-123">Возвращает объект [**фолдеритемс**](folderitems.md) , представляющий все выбранные элементы в представлении.</span><span class="sxs-lookup"><span data-stu-id="496c4-123">Gets a [**FolderItems**](folderitems.md) object that represents all of the selected items in the view.</span></span><br/> |
| [<span data-ttu-id="496c4-124">**SelectItem**</span><span class="sxs-lookup"><span data-stu-id="496c4-124">**SelectItem**</span></span>](shellfolderview-selectitem.md)       | <span data-ttu-id="496c4-125">Задает состояние выбора элемента в представлении.</span><span class="sxs-lookup"><span data-stu-id="496c4-125">Sets the selection state of an item in the view.</span></span><br/>                                                        |



 

### <a name="properties"></a><span data-ttu-id="496c4-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="496c4-126">Properties</span></span>

<span data-ttu-id="496c4-127">Объект **шеллфолдервиев** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="496c4-127">The **ShellFolderView** object has these properties.</span></span>



| <span data-ttu-id="496c4-128">Свойство</span><span class="sxs-lookup"><span data-stu-id="496c4-128">Property</span></span>                                                      | <span data-ttu-id="496c4-129">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="496c4-129">Access type</span></span>          | <span data-ttu-id="496c4-130">Описание</span><span class="sxs-lookup"><span data-stu-id="496c4-130">Description</span></span>                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="496c4-131">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="496c4-131">**Application**</span></span>](shellfolderview-application.md)<br/> | <span data-ttu-id="496c4-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="496c4-132">Read-only</span></span><br/> | <span data-ttu-id="496c4-133">Содержит объект приложения объекта.</span><span class="sxs-lookup"><span data-stu-id="496c4-133">Contains the object's Application object.</span></span><br/>                                                         |
| [<span data-ttu-id="496c4-134">**фокуседитем**</span><span class="sxs-lookup"><span data-stu-id="496c4-134">**FocusedItem**</span></span>](shellfolderview-focuseditem.md)<br/> | <span data-ttu-id="496c4-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="496c4-135">Read-only</span></span><br/> | <span data-ttu-id="496c4-136">Возвращает объект [**FolderItem**](folderitem.md) , представляющий элемент, имеющий фокус ввода.</span><span class="sxs-lookup"><span data-stu-id="496c4-136">Gets a [**FolderItem**](folderitem.md) object that represents the item that has the input focus.</span></span><br/> |
| [<span data-ttu-id="496c4-137">**Folder**</span><span class="sxs-lookup"><span data-stu-id="496c4-137">**Folder**</span></span>](shellfolderview-folder.md)<br/>           | <span data-ttu-id="496c4-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="496c4-138">Read-only</span></span><br/> | <span data-ttu-id="496c4-139">Возвращает объект [**Folder**](folder.md) , представляющий представление.</span><span class="sxs-lookup"><span data-stu-id="496c4-139">Gets a [**Folder**](folder.md) object that represents the view.</span></span><br/>                                  |
| [<span data-ttu-id="496c4-140">**Parent**</span><span class="sxs-lookup"><span data-stu-id="496c4-140">**Parent**</span></span>](shellfolderview-parent.md)<br/>           | <span data-ttu-id="496c4-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="496c4-141">Read-only</span></span><br/> | <span data-ttu-id="496c4-142">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="496c4-142">Not implemented.</span></span><br/>                                                                                  |
| [<span data-ttu-id="496c4-143">**Индекса**</span><span class="sxs-lookup"><span data-stu-id="496c4-143">**Script**</span></span>](shellfolderview-script.md)<br/>           | <span data-ttu-id="496c4-144">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="496c4-144">Read-only</span></span><br/> | <span data-ttu-id="496c4-145">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="496c4-145">Deprecated.</span></span><br/>                                                                                       |
| [<span data-ttu-id="496c4-146">**виевоптионс**</span><span class="sxs-lookup"><span data-stu-id="496c4-146">**ViewOptions**</span></span>](shellfolderview-viewoptions.md)<br/> | <span data-ttu-id="496c4-147">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="496c4-147">Read-only</span></span><br/> | <span data-ttu-id="496c4-148">Возвращает набор флагов, указывающих текущие параметры представления.</span><span class="sxs-lookup"><span data-stu-id="496c4-148">Gets a set of flags that indicate the current options of the view.</span></span><br/>                                |



 

## <a name="requirements"></a><span data-ttu-id="496c4-149">Требования</span><span class="sxs-lookup"><span data-stu-id="496c4-149">Requirements</span></span>



| <span data-ttu-id="496c4-150">Требование</span><span class="sxs-lookup"><span data-stu-id="496c4-150">Requirement</span></span> | <span data-ttu-id="496c4-151">Значение</span><span class="sxs-lookup"><span data-stu-id="496c4-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496c4-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="496c4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="496c4-153">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="496c4-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="496c4-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="496c4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="496c4-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="496c4-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="496c4-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="496c4-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="496c4-157"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="496c4-157"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="496c4-158">IDL</span><span class="sxs-lookup"><span data-stu-id="496c4-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="496c4-159"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="496c4-159"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="496c4-160">DLL</span><span class="sxs-lookup"><span data-stu-id="496c4-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="496c4-161"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="496c4-161"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |
| <span data-ttu-id="496c4-162">IID</span><span class="sxs-lookup"><span data-stu-id="496c4-162">IID</span></span><br/>                      | <span data-ttu-id="496c4-163">\_ШЕЛЛФОЛДЕРВИЕВ CLSID</span><span class="sxs-lookup"><span data-stu-id="496c4-163">CLSID\_ShellFolderView</span></span><br/>                                                                              |



## <a name="see-also"></a><span data-ttu-id="496c4-164">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="496c4-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496c4-165">**Флаги Шеллфолдервиевоптионс**</span><span class="sxs-lookup"><span data-stu-id="496c4-165">**ShellFolderViewOptions Flags**</span></span>](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




