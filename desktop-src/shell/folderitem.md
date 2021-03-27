---
description: Представляет элемент в папке оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения об элементе.
title: Объект FolderItem (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496773"
---
# <a name="folderitem-object"></a><span data-ttu-id="ffd05-104">Объект FolderItem</span><span class="sxs-lookup"><span data-stu-id="ffd05-104">FolderItem object</span></span>

<span data-ttu-id="ffd05-105">Представляет элемент в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="ffd05-105">Represents an item in a Shell folder.</span></span> <span data-ttu-id="ffd05-106">Этот объект содержит свойства и методы, позволяющие получить сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="ffd05-106">This object contains properties and methods that allow you to retrieve information about the item.</span></span>

## <a name="members"></a><span data-ttu-id="ffd05-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="ffd05-107">Members</span></span>

<span data-ttu-id="ffd05-108">Объект **FolderItem** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ffd05-108">The **FolderItem** object has these types of members:</span></span>

-   [<span data-ttu-id="ffd05-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ffd05-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="ffd05-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffd05-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ffd05-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ffd05-111">Methods</span></span>

<span data-ttu-id="ffd05-112">Объект **FolderItem** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="ffd05-112">The **FolderItem** object has these methods.</span></span>



| <span data-ttu-id="ffd05-113">Метод</span><span class="sxs-lookup"><span data-stu-id="ffd05-113">Method</span></span>                                      | <span data-ttu-id="ffd05-114">Описание</span><span class="sxs-lookup"><span data-stu-id="ffd05-114">Description</span></span>                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffd05-115">**инвокеверб**</span><span class="sxs-lookup"><span data-stu-id="ffd05-115">**InvokeVerb**</span></span>](folderitem-invokeverb.md) | <span data-ttu-id="ffd05-116">Выполняет команду для элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-116">Executes a verb on the item.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="ffd05-117">**Команды**</span><span class="sxs-lookup"><span data-stu-id="ffd05-117">**Verbs**</span></span>](folderitem-verbs.md)           | <span data-ttu-id="ffd05-118">Извлекает объект [**фолдеритемвербс**](folderitemverbs.md) элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-118">Retrieves the item's [**FolderItemVerbs**](folderitemverbs.md) object.</span></span> <span data-ttu-id="ffd05-119">Этот объект представляет собой коллекцию команд, которые могут быть выполнены для элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-119">This object is the collection of verbs that can be executed on the item.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ffd05-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffd05-120">Properties</span></span>

<span data-ttu-id="ffd05-121">Объект **FolderItem** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ffd05-121">The **FolderItem** object has these properties.</span></span>



| <span data-ttu-id="ffd05-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="ffd05-122">Property</span></span>                                                   | <span data-ttu-id="ffd05-123">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="ffd05-123">Access type</span></span>           | <span data-ttu-id="ffd05-124">Описание</span><span class="sxs-lookup"><span data-stu-id="ffd05-124">Description</span></span>                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffd05-125">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="ffd05-125">**Application**</span></span>](folderitem-application.md)<br/>   | <span data-ttu-id="ffd05-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-126">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-127">Содержит объект [**приложения**](folderitem-application.md) для элемента папки.</span><span class="sxs-lookup"><span data-stu-id="ffd05-127">Contains the [**Application**](folderitem-application.md) object of the folder item.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="ffd05-128">**GetFolder**</span><span class="sxs-lookup"><span data-stu-id="ffd05-128">**GetFolder**</span></span>](folderitem-getfolder.md)<br/>       | <span data-ttu-id="ffd05-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-129">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-130">Содержит объект [**папки**](folder.md) элемента, если элемент является папкой.</span><span class="sxs-lookup"><span data-stu-id="ffd05-130">Contains the item's [**Folder**](folder.md) object, if the item is a folder.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="ffd05-131">**Соединение**</span><span class="sxs-lookup"><span data-stu-id="ffd05-131">**GetLink**</span></span>](folderitem-getlink.md)<br/>           | <span data-ttu-id="ffd05-132">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-132">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-133">Содержит объект [**шелллинкобжект**](shelllinkobject-object.md) элемента, если элемент является ярлыком.</span><span class="sxs-lookup"><span data-stu-id="ffd05-133">Contains the item's [**ShellLinkObject**](shelllinkobject-object.md) object, if the item is a shortcut.</span></span><br/>                                                                                                |
| [<span data-ttu-id="ffd05-134">**Является Browsable**</span><span class="sxs-lookup"><span data-stu-id="ffd05-134">**IsBrowsable**</span></span>](folderitem-isbrowsable.md)<br/>   | <span data-ttu-id="ffd05-135">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-135">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-136">Указывает, может ли элемент размещаться в кадре браузера или проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="ffd05-136">Indicates if the item can be hosted inside a browser or Windows Explorer frame.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="ffd05-137">**Файловая система**</span><span class="sxs-lookup"><span data-stu-id="ffd05-137">**IsFileSystem**</span></span>](folderitem-isfilesystem.md)<br/> | <span data-ttu-id="ffd05-138">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-138">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-139">Указывает, является ли элемент частью файловой системы.</span><span class="sxs-lookup"><span data-stu-id="ffd05-139">Indicates if the item is part of the file system.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="ffd05-140">**IsFolder**</span><span class="sxs-lookup"><span data-stu-id="ffd05-140">**IsFolder**</span></span>](folderitem-isfolder.md)<br/>         | <span data-ttu-id="ffd05-141">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-141">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-142">Указывает, является ли элемент папкой.</span><span class="sxs-lookup"><span data-stu-id="ffd05-142">Indicates if the item is a folder.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="ffd05-143">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="ffd05-143">**IsLink**</span></span>](folderitem-islink.md)<br/>             | <span data-ttu-id="ffd05-144">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-144">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-145">Указывает, является ли элемент ярлыком.</span><span class="sxs-lookup"><span data-stu-id="ffd05-145">Indicates whether the item is a shortcut.</span></span><br/>                                                                                                                                                               |
| [<span data-ttu-id="ffd05-146">**ModifyDate**</span><span class="sxs-lookup"><span data-stu-id="ffd05-146">**ModifyDate**</span></span>](folderitem-modifydate.md)<br/>     | <span data-ttu-id="ffd05-147">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ffd05-147">Read/write</span></span><br/> | <span data-ttu-id="ffd05-148">Задает или возвращает дату и время последнего изменения файла.</span><span class="sxs-lookup"><span data-stu-id="ffd05-148">Sets or gets the date and time that a file was last modified.</span></span> <span data-ttu-id="ffd05-149">[**ModifyDate**](folderitem-modifydate.md) можно использовать для получения даты и времени последнего изменения папки, но не может установить ее.</span><span class="sxs-lookup"><span data-stu-id="ffd05-149">[**ModifyDate**](folderitem-modifydate.md) can be used to retrieve the date and time that a folder was last modified, but cannot set it.</span></span><br/> |
| [<span data-ttu-id="ffd05-150">**Имя**</span><span class="sxs-lookup"><span data-stu-id="ffd05-150">**Name**</span></span>](folderitem-name.md)<br/>                 | <span data-ttu-id="ffd05-151">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="ffd05-151">Read/write</span></span><br/> | <span data-ttu-id="ffd05-152">Возвращает или задает имя элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-152">Sets or gets the item's name.</span></span><br/>                                                                                                                                                                           |
| [<span data-ttu-id="ffd05-153">**Parent**</span><span class="sxs-lookup"><span data-stu-id="ffd05-153">**Parent**</span></span>](folderitem-parent.md)<br/>             | <span data-ttu-id="ffd05-154">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-154">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-155">Возвращает объект, представляющий родительский элемент для элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-155">Gets an object that represents the parent of the item.</span></span><br/>                                                                                                                                                  |
| [<span data-ttu-id="ffd05-156">**Путь**</span><span class="sxs-lookup"><span data-stu-id="ffd05-156">**Path**</span></span>](folderitem-path.md)<br/>                 | <span data-ttu-id="ffd05-157">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-157">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-158">Содержит полный путь и имя элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-158">Contains the item's full path and name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="ffd05-159">**Изменять**</span><span class="sxs-lookup"><span data-stu-id="ffd05-159">**Size**</span></span>](folderitem-size.md)<br/>                 | <span data-ttu-id="ffd05-160">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-160">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-161">Содержит размер элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-161">Contains the item's size.</span></span><br/>                                                                                                                                                                               |
| [<span data-ttu-id="ffd05-162">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ffd05-162">**Type**</span></span>](folderitem-type.md)<br/>                 | <span data-ttu-id="ffd05-163">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffd05-163">Read-only</span></span><br/>  | <span data-ttu-id="ffd05-164">Содержит строковое представление типа элемента.</span><span class="sxs-lookup"><span data-stu-id="ffd05-164">Contains a string representation of the item's type.</span></span><br/>                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="ffd05-165">Требования</span><span class="sxs-lookup"><span data-stu-id="ffd05-165">Requirements</span></span>



| <span data-ttu-id="ffd05-166">Требование</span><span class="sxs-lookup"><span data-stu-id="ffd05-166">Requirement</span></span> | <span data-ttu-id="ffd05-167">Значение</span><span class="sxs-lookup"><span data-stu-id="ffd05-167">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd05-168">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffd05-168">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd05-169">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="ffd05-169">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ffd05-170">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffd05-170">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd05-171">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ffd05-171">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ffd05-172">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ffd05-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd05-173"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd05-173"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="ffd05-174">IDL</span><span class="sxs-lookup"><span data-stu-id="ffd05-174">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ffd05-175"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ffd05-175"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="ffd05-176">DLL</span><span class="sxs-lookup"><span data-stu-id="ffd05-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffd05-177"><dt>Shell32.dll (версия 4,71 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="ffd05-177"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




