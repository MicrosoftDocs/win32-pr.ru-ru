---
description: Управляет связями оболочки. Этот объект делает большую часть функциональных возможностей интерфейса Ишелллинк, доступного для сценариев приложений.
title: Объект Шелллинкобжект (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: d3c0ccf8-0f83-42f7-9d6f-1fb293da6364
ms.openlocfilehash: 5862ae3c9b7bf1262edbc28b06f2963f2e577275
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842635"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="1f1ae-104">Объект Шелллинкобжект</span><span class="sxs-lookup"><span data-stu-id="1f1ae-104">ShellLinkObject object</span></span>

<span data-ttu-id="1f1ae-105">Управляет связями оболочки.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-105">Manages Shell links.</span></span> <span data-ttu-id="1f1ae-106">Этот объект делает большую часть функциональных возможностей интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) , доступного для сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="1f1ae-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="1f1ae-107">Members</span></span>

<span data-ttu-id="1f1ae-108">Объект **шелллинкобжект** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1f1ae-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="1f1ae-109">Методы</span><span class="sxs-lookup"><span data-stu-id="1f1ae-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="1f1ae-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f1ae-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1f1ae-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1f1ae-111">Methods</span></span>

<span data-ttu-id="1f1ae-112">Объект **шелллинкобжект** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="1f1ae-113">Метод</span><span class="sxs-lookup"><span data-stu-id="1f1ae-113">Method</span></span>                                                     | <span data-ttu-id="1f1ae-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1f1ae-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f1ae-115">**жетиконлокатион**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="1f1ae-116">Возвращает расположение значка, назначенного ссылке.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="1f1ae-117">**Проблемы**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="1f1ae-118">Выполняет поиск целевого объекта для ссылки на оболочку, даже если целевой объект был перемещен или переименован.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="1f1ae-119">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="1f1ae-120">Сохраняет все изменения в ссылке.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="1f1ae-121">**сетиконлокатион**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="1f1ae-122">Задает расположение значка, назначенного ссылке.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="1f1ae-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="1f1ae-123">Properties</span></span>

<span data-ttu-id="1f1ae-124">Объект **шелллинкобжект** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="1f1ae-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="1f1ae-125">Property</span></span>                                                                | <span data-ttu-id="1f1ae-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="1f1ae-126">Access type</span></span>           | <span data-ttu-id="1f1ae-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1f1ae-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f1ae-128">**Аргументы**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="1f1ae-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1f1ae-129">Read/write</span></span><br/> | <span data-ttu-id="1f1ae-130">Содержит аргументы ссылки.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="1f1ae-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="1f1ae-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1f1ae-132">Read/write</span></span><br/> | <span data-ttu-id="1f1ae-133">Возвращает или задает описание ссылки.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="1f1ae-134">**Сочетание клавиш**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="1f1ae-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1f1ae-135">Read/write</span></span><br/> | <span data-ttu-id="1f1ae-136">Возвращает или задает сочетание клавиш для ссылки.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="1f1ae-137">**Путь**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="1f1ae-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1f1ae-138">Read/write</span></span><br/> | <span data-ttu-id="1f1ae-139">Возвращает или задает путь к объекту ссылки.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="1f1ae-140">**Возвращающий showcommand**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="1f1ae-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1f1ae-141">Read/write</span></span><br/> | <span data-ttu-id="1f1ae-142">Возвращает или задает начальное состояние отображения команды ссылки (с указанием размера, сворачивания или развертывания).</span><span class="sxs-lookup"><span data-stu-id="1f1ae-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="1f1ae-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="1f1ae-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="1f1ae-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="1f1ae-144">Read/write</span></span><br/> | <span data-ttu-id="1f1ae-145">Возвращает или задает рабочий каталог, указанный в ссылке.</span><span class="sxs-lookup"><span data-stu-id="1f1ae-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="1f1ae-146">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="1f1ae-146">Requirements</span></span>



| <span data-ttu-id="1f1ae-147">Требование</span><span class="sxs-lookup"><span data-stu-id="1f1ae-147">Requirement</span></span> | <span data-ttu-id="1f1ae-148">Значение</span><span class="sxs-lookup"><span data-stu-id="1f1ae-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1ae-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1f1ae-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1f1ae-150">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1f1ae-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1f1ae-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1f1ae-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1f1ae-152">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f1ae-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1f1ae-153">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1f1ae-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f1ae-154"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f1ae-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="1f1ae-155">IDL</span><span class="sxs-lookup"><span data-stu-id="1f1ae-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f1ae-156"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f1ae-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="1f1ae-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1f1ae-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f1ae-158"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1f1ae-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1ae-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1f1ae-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1ae-160">Ссылки оболочки</span><span class="sxs-lookup"><span data-stu-id="1f1ae-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
