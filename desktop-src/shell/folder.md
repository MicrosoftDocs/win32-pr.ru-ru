---
description: Представляет папку оболочки. Этот объект содержит свойства и методы, позволяющие получить сведения о папке.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Объект Folder (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539521"
---
# <a name="folder-object"></a><span data-ttu-id="e4528-104">Объект Folder</span><span class="sxs-lookup"><span data-stu-id="e4528-104">Folder object</span></span>

<span data-ttu-id="e4528-105">Представляет папку оболочки.</span><span class="sxs-lookup"><span data-stu-id="e4528-105">Represents a Shell folder.</span></span> <span data-ttu-id="e4528-106">Этот объект содержит свойства и методы, позволяющие получить сведения о папке.</span><span class="sxs-lookup"><span data-stu-id="e4528-106">This object contains properties and methods that allow you to retrieve information about the folder.</span></span>

## <a name="members"></a><span data-ttu-id="e4528-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="e4528-107">Members</span></span>

<span data-ttu-id="e4528-108">Объект **Folder** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e4528-108">The **Folder** object has these types of members:</span></span>

-   [<span data-ttu-id="e4528-109">Методы</span><span class="sxs-lookup"><span data-stu-id="e4528-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="e4528-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="e4528-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e4528-111">Методы</span><span class="sxs-lookup"><span data-stu-id="e4528-111">Methods</span></span>

<span data-ttu-id="e4528-112">Объект **Folder** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="e4528-112">The **Folder** object has these methods.</span></span>



| <span data-ttu-id="e4528-113">Метод</span><span class="sxs-lookup"><span data-stu-id="e4528-113">Method</span></span>                                      | <span data-ttu-id="e4528-114">Описание</span><span class="sxs-lookup"><span data-stu-id="e4528-114">Description</span></span>                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4528-115">**копихере**</span><span class="sxs-lookup"><span data-stu-id="e4528-115">**CopyHere**</span></span>](folder-copyhere.md)         | <span data-ttu-id="e4528-116">Копирует элемент или элементы в папку.</span><span class="sxs-lookup"><span data-stu-id="e4528-116">Copies an item or items to a folder.</span></span><br/>                                                                            |
| [<span data-ttu-id="e4528-117">**жетдетаилсоф**</span><span class="sxs-lookup"><span data-stu-id="e4528-117">**GetDetailsOf**</span></span>](folder-getdetailsof.md) | <span data-ttu-id="e4528-118">Извлекает сведения об элементе в папке.</span><span class="sxs-lookup"><span data-stu-id="e4528-118">Retrieves details about an item in a folder.</span></span> <span data-ttu-id="e4528-119">Например, его размер, тип или время последнего изменения.</span><span class="sxs-lookup"><span data-stu-id="e4528-119">For example, its size, type, or the time of its last modification.</span></span><br/> |
| [<span data-ttu-id="e4528-120">**Элементы**</span><span class="sxs-lookup"><span data-stu-id="e4528-120">**Items**</span></span>](folder-items.md)               | <span data-ttu-id="e4528-121">Извлекает объект [**фолдеритемс**](folderitems.md) , представляющий коллекцию элементов в папке.</span><span class="sxs-lookup"><span data-stu-id="e4528-121">Retrieves a [**FolderItems**](folderitems.md) object that represents the collection of items in the folder.</span></span><br/>    |
| [<span data-ttu-id="e4528-122">**мовехере**</span><span class="sxs-lookup"><span data-stu-id="e4528-122">**MoveHere**</span></span>](folder-movehere.md)         | <span data-ttu-id="e4528-123">Перемещает элемент или элементы в эту папку.</span><span class="sxs-lookup"><span data-stu-id="e4528-123">Moves an item or items to this folder.</span></span><br/>                                                                          |
| [<span data-ttu-id="e4528-124">**NewFolder**</span><span class="sxs-lookup"><span data-stu-id="e4528-124">**NewFolder**</span></span>](folder-newfolder.md)       | <span data-ttu-id="e4528-125">Создает новую папку.</span><span class="sxs-lookup"><span data-stu-id="e4528-125">Creates a new folder.</span></span><br/>                                                                                           |
| [<span data-ttu-id="e4528-126">**ParseName**</span><span class="sxs-lookup"><span data-stu-id="e4528-126">**ParseName**</span></span>](folder-parsename.md)       | <span data-ttu-id="e4528-127">Создает и возвращает объект [**FolderItem**](folderitem.md) , представляющий указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="e4528-127">Creates and returns a [**FolderItem**](folderitem.md) object that represents a specified item.</span></span><br/>                 |



 

### <a name="properties"></a><span data-ttu-id="e4528-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="e4528-128">Properties</span></span>

<span data-ttu-id="e4528-129">Объект **Folder** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="e4528-129">The **Folder** object has these properties.</span></span>



| <span data-ttu-id="e4528-130">Свойство</span><span class="sxs-lookup"><span data-stu-id="e4528-130">Property</span></span>                                               | <span data-ttu-id="e4528-131">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e4528-131">Access type</span></span>          | <span data-ttu-id="e4528-132">Описание</span><span class="sxs-lookup"><span data-stu-id="e4528-132">Description</span></span>                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [<span data-ttu-id="e4528-133">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="e4528-133">**Application**</span></span>](folder-application.md)<br/>   | <span data-ttu-id="e4528-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4528-134">Read-only</span></span><br/> | <span data-ttu-id="e4528-135">Содержит объект приложения папки.</span><span class="sxs-lookup"><span data-stu-id="e4528-135">Contains the folder's Application object.</span></span><br/> |
| [<span data-ttu-id="e4528-136">**Parent**</span><span class="sxs-lookup"><span data-stu-id="e4528-136">**Parent**</span></span>](folder-parent.md)<br/>             | <span data-ttu-id="e4528-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4528-137">Read-only</span></span><br/> | <span data-ttu-id="e4528-138">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="e4528-138">Not implemented.</span></span><br/>                          |
| [<span data-ttu-id="e4528-139">**парентфолдер**</span><span class="sxs-lookup"><span data-stu-id="e4528-139">**ParentFolder**</span></span>](folder-parentfolder.md)<br/> | <span data-ttu-id="e4528-140">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4528-140">Read-only</span></span><br/> | <span data-ttu-id="e4528-141">Содержит объект родительской **папки** .</span><span class="sxs-lookup"><span data-stu-id="e4528-141">Contains the parent **Folder** object.</span></span><br/>    |
| [<span data-ttu-id="e4528-142">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="e4528-142">**Title**</span></span>](folder-title.md)<br/>               | <span data-ttu-id="e4528-143">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4528-143">Read-only</span></span><br/> | <span data-ttu-id="e4528-144">Содержит заголовок папки.</span><span class="sxs-lookup"><span data-stu-id="e4528-144">Contains the title of the folder.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="e4528-145">Примечания</span><span class="sxs-lookup"><span data-stu-id="e4528-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4528-146">Не все методы реализуются для всех папок.</span><span class="sxs-lookup"><span data-stu-id="e4528-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="e4528-147">Например, метод [**PARSENAME**](folder-parsename.md) не реализован для папки панели управления ( \_ элементы управления CSID).</span><span class="sxs-lookup"><span data-stu-id="e4528-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="e4528-148">При попытке вызвать нереализованный метод возникнет ошибка 0x800A01BD (Decimal 445).</span><span class="sxs-lookup"><span data-stu-id="e4528-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e4528-149">Требования</span><span class="sxs-lookup"><span data-stu-id="e4528-149">Requirements</span></span>



| <span data-ttu-id="e4528-150">Требование</span><span class="sxs-lookup"><span data-stu-id="e4528-150">Requirement</span></span> | <span data-ttu-id="e4528-151">Значение</span><span class="sxs-lookup"><span data-stu-id="e4528-151">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4528-152">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e4528-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e4528-153">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e4528-153">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                 |
| <span data-ttu-id="e4528-154">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e4528-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e4528-155">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e4528-155">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4528-156">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e4528-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4528-157"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4528-157"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4528-158">IDL</span><span class="sxs-lookup"><span data-stu-id="e4528-158">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4528-159"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4528-159"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 




