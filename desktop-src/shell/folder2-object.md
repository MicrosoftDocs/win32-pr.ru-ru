---
description: Расширяет объект Folder для поддержки автономных папок.
title: Объект Folder2 (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985497"
---
# <a name="folder2-object"></a><span data-ttu-id="f2503-103">Объект Folder2</span><span class="sxs-lookup"><span data-stu-id="f2503-103">Folder2 object</span></span>

<span data-ttu-id="f2503-104">Расширяет объект [**Folder**](folder.md) для поддержки автономных папок.</span><span class="sxs-lookup"><span data-stu-id="f2503-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="f2503-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="f2503-105">Members</span></span>

<span data-ttu-id="f2503-106">Объект **folder2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f2503-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="f2503-107">Методы</span><span class="sxs-lookup"><span data-stu-id="f2503-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="f2503-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2503-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f2503-109">Методы</span><span class="sxs-lookup"><span data-stu-id="f2503-109">Methods</span></span>

<span data-ttu-id="f2503-110">Объект **folder2** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="f2503-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="f2503-111">Метод</span><span class="sxs-lookup"><span data-stu-id="f2503-111">Method</span></span>                                                                 | <span data-ttu-id="f2503-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f2503-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="f2503-113">**дисмисседвебвиевбаррикаде**</span><span class="sxs-lookup"><span data-stu-id="f2503-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="f2503-114">Вызывается в ответ на веб-представление баррикаде, закрытое пользователем.</span><span class="sxs-lookup"><span data-stu-id="f2503-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="f2503-115">**Полнит**</span><span class="sxs-lookup"><span data-stu-id="f2503-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="f2503-116">Синхронизирует все автономные файлы в папке.</span><span class="sxs-lookup"><span data-stu-id="f2503-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="f2503-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2503-117">Properties</span></span>

<span data-ttu-id="f2503-118">Объект **folder2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f2503-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="f2503-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="f2503-119">Property</span></span>                                                                            | <span data-ttu-id="f2503-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="f2503-120">Access type</span></span>          | <span data-ttu-id="f2503-121">Описание</span><span class="sxs-lookup"><span data-stu-id="f2503-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="f2503-122">**хаветошоввебвиевбаррикаде**</span><span class="sxs-lookup"><span data-stu-id="f2503-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="f2503-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2503-123">Read-only</span></span><br/> | <span data-ttu-id="f2503-124">В настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="f2503-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="f2503-125">**оффлинестатус**</span><span class="sxs-lookup"><span data-stu-id="f2503-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="f2503-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2503-126">Read-only</span></span><br/> | <span data-ttu-id="f2503-127">Содержит автономное состояние папки.</span><span class="sxs-lookup"><span data-stu-id="f2503-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="f2503-128">**Самообслуживания**</span><span class="sxs-lookup"><span data-stu-id="f2503-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="f2503-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="f2503-129">Read-only</span></span><br/> | <span data-ttu-id="f2503-130">Содержит объект [**FolderItem**](folderitem.md) папки.</span><span class="sxs-lookup"><span data-stu-id="f2503-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f2503-131">Требования</span><span class="sxs-lookup"><span data-stu-id="f2503-131">Requirements</span></span>



| <span data-ttu-id="f2503-132">Требование</span><span class="sxs-lookup"><span data-stu-id="f2503-132">Requirement</span></span> | <span data-ttu-id="f2503-133">Значение</span><span class="sxs-lookup"><span data-stu-id="f2503-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2503-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f2503-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f2503-135">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f2503-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f2503-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f2503-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f2503-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f2503-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f2503-138">Header</span><span class="sxs-lookup"><span data-stu-id="f2503-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2503-139"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2503-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="f2503-140">IDL</span><span class="sxs-lookup"><span data-stu-id="f2503-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f2503-141"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f2503-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="f2503-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f2503-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2503-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="f2503-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2503-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2503-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2503-145">**Папка**</span><span class="sxs-lookup"><span data-stu-id="f2503-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




