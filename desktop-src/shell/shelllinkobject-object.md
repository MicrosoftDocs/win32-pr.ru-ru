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
ms.openlocfilehash: 1daf1aafae4bc230014890b79d4fb0310aa30a1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986025"
---
# <a name="shelllinkobject-object"></a><span data-ttu-id="05931-104">Объект Шелллинкобжект</span><span class="sxs-lookup"><span data-stu-id="05931-104">ShellLinkObject object</span></span>

<span data-ttu-id="05931-105">Управляет связями оболочки.</span><span class="sxs-lookup"><span data-stu-id="05931-105">Manages Shell links.</span></span> <span data-ttu-id="05931-106">Этот объект делает большую часть функциональных возможностей интерфейса [**ишелллинк**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) , доступного для сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="05931-106">This object makes much of the functionality of the [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka) interface available to scripting applications.</span></span>

## <a name="members"></a><span data-ttu-id="05931-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="05931-107">Members</span></span>

<span data-ttu-id="05931-108">Объект **шелллинкобжект** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="05931-108">The **ShellLinkObject** object has these types of members:</span></span>

-   [<span data-ttu-id="05931-109">Методы</span><span class="sxs-lookup"><span data-stu-id="05931-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="05931-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="05931-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05931-111">Методы</span><span class="sxs-lookup"><span data-stu-id="05931-111">Methods</span></span>

<span data-ttu-id="05931-112">Объект **шелллинкобжект** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="05931-112">The **ShellLinkObject** object has these methods.</span></span>



| <span data-ttu-id="05931-113">Метод</span><span class="sxs-lookup"><span data-stu-id="05931-113">Method</span></span>                                                     | <span data-ttu-id="05931-114">Описание</span><span class="sxs-lookup"><span data-stu-id="05931-114">Description</span></span>                                                                                    |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05931-115">**жетиконлокатион**</span><span class="sxs-lookup"><span data-stu-id="05931-115">**GetIconLocation**</span></span>](shelllinkobject-geticonlocation.md) | <span data-ttu-id="05931-116">Возвращает расположение значка, назначенного ссылке.</span><span class="sxs-lookup"><span data-stu-id="05931-116">Gets the location of the icon assigned to the link.</span></span><br/>                                 |
| [<span data-ttu-id="05931-117">**Разрешить**</span><span class="sxs-lookup"><span data-stu-id="05931-117">**Resolve**</span></span>](shelllinkobject-resolve.md)                 | <span data-ttu-id="05931-118">Выполняет поиск целевого объекта для ссылки на оболочку, даже если целевой объект был перемещен или переименован.</span><span class="sxs-lookup"><span data-stu-id="05931-118">Looks for the target of a Shell link, even if the target has been moved or renamed.</span></span><br/> |
| [<span data-ttu-id="05931-119">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="05931-119">**Save**</span></span>](shelllinkobject-save.md)                       | <span data-ttu-id="05931-120">Сохраняет все изменения в ссылке.</span><span class="sxs-lookup"><span data-stu-id="05931-120">Saves all changes to the link.</span></span><br/>                                                      |
| [<span data-ttu-id="05931-121">**сетиконлокатион**</span><span class="sxs-lookup"><span data-stu-id="05931-121">**SetIconLocation**</span></span>](shelllinkobject-seticonlocation.md) | <span data-ttu-id="05931-122">Задает расположение значка, назначенного ссылке.</span><span class="sxs-lookup"><span data-stu-id="05931-122">Sets the location of the icon assigned to the link.</span></span><br/>                                 |



 

### <a name="properties"></a><span data-ttu-id="05931-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="05931-123">Properties</span></span>

<span data-ttu-id="05931-124">Объект **шелллинкобжект** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="05931-124">The **ShellLinkObject** object has these properties.</span></span>



| <span data-ttu-id="05931-125">Свойство</span><span class="sxs-lookup"><span data-stu-id="05931-125">Property</span></span>                                                                | <span data-ttu-id="05931-126">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="05931-126">Access type</span></span>           | <span data-ttu-id="05931-127">Описание</span><span class="sxs-lookup"><span data-stu-id="05931-127">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05931-128">**Аргументы**</span><span class="sxs-lookup"><span data-stu-id="05931-128">**Arguments**</span></span>](shelllinkobject-arguments.md)<br/>               | <span data-ttu-id="05931-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="05931-129">Read/write</span></span><br/> | <span data-ttu-id="05931-130">Содержит аргументы ссылки.</span><span class="sxs-lookup"><span data-stu-id="05931-130">Contains a link's arguments.</span></span><br/>                                                                   |
| [<span data-ttu-id="05931-131">**Описание**</span><span class="sxs-lookup"><span data-stu-id="05931-131">**Description**</span></span>](shelllinkobject-description.md)<br/>           | <span data-ttu-id="05931-132">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="05931-132">Read/write</span></span><br/> | <span data-ttu-id="05931-133">Возвращает или задает описание ссылки.</span><span class="sxs-lookup"><span data-stu-id="05931-133">Gets or sets the description of the link.</span></span><br/>                                                      |
| [<span data-ttu-id="05931-134">**Сочетание клавиш**</span><span class="sxs-lookup"><span data-stu-id="05931-134">**Hotkey**</span></span>](shelllinkobject-hotkey.md)<br/>                     | <span data-ttu-id="05931-135">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="05931-135">Read/write</span></span><br/> | <span data-ttu-id="05931-136">Возвращает или задает сочетание клавиш для ссылки.</span><span class="sxs-lookup"><span data-stu-id="05931-136">Gets or sets the keyboard shortcut for the link.</span></span><br/>                                               |
| [<span data-ttu-id="05931-137">**Путь**</span><span class="sxs-lookup"><span data-stu-id="05931-137">**Path**</span></span>](shelllinkobject-path.md)<br/>                         | <span data-ttu-id="05931-138">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="05931-138">Read/write</span></span><br/> | <span data-ttu-id="05931-139">Возвращает или задает путь к объекту ссылки.</span><span class="sxs-lookup"><span data-stu-id="05931-139">Gets or sets the path to the link object.</span></span><br/>                                                      |
| [<span data-ttu-id="05931-140">**Возвращающий showcommand**</span><span class="sxs-lookup"><span data-stu-id="05931-140">**ShowCommand**</span></span>](shelllinkobject-showcommand.md)<br/>           | <span data-ttu-id="05931-141">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="05931-141">Read/write</span></span><br/> | <span data-ttu-id="05931-142">Возвращает или задает начальное состояние отображения команды ссылки (с указанием размера, сворачивания или развертывания).</span><span class="sxs-lookup"><span data-stu-id="05931-142">Gets or sets the initial display state (sized, minimized, or maximized) of the link's command.</span></span><br/> |
| [<span data-ttu-id="05931-143">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="05931-143">**WorkingDirectory**</span></span>](shelllinkobject-workingdirectory.md)<br/> | <span data-ttu-id="05931-144">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="05931-144">Read/write</span></span><br/> | <span data-ttu-id="05931-145">Возвращает или задает рабочий каталог, указанный в ссылке.</span><span class="sxs-lookup"><span data-stu-id="05931-145">Gets or sets the working directory specified in the link.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="05931-146">Требования</span><span class="sxs-lookup"><span data-stu-id="05931-146">Requirements</span></span>



| <span data-ttu-id="05931-147">Требование</span><span class="sxs-lookup"><span data-stu-id="05931-147">Requirement</span></span> | <span data-ttu-id="05931-148">Значение</span><span class="sxs-lookup"><span data-stu-id="05931-148">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05931-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05931-149">Minimum supported client</span></span><br/> | <span data-ttu-id="05931-150">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="05931-150">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="05931-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05931-151">Minimum supported server</span></span><br/> | <span data-ttu-id="05931-152">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="05931-152">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="05931-153">Header</span><span class="sxs-lookup"><span data-stu-id="05931-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="05931-154"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="05931-154"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="05931-155">IDL</span><span class="sxs-lookup"><span data-stu-id="05931-155">IDL</span></span><br/>                      | <dl> <span data-ttu-id="05931-156"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="05931-156"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="05931-157">DLL</span><span class="sxs-lookup"><span data-stu-id="05931-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05931-158"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="05931-158"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05931-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05931-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05931-160">Ссылки оболочки</span><span class="sxs-lookup"><span data-stu-id="05931-160">Shell Links</span></span>](./links.md)
</dt> </dl>

 

 
