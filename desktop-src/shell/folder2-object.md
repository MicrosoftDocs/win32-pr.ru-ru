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
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842065"
---
# <a name="folder2-object"></a><span data-ttu-id="40f00-103">Объект Folder2</span><span class="sxs-lookup"><span data-stu-id="40f00-103">Folder2 object</span></span>

<span data-ttu-id="40f00-104">Расширяет объект [**Folder**](folder.md) для поддержки автономных папок.</span><span class="sxs-lookup"><span data-stu-id="40f00-104">Extends the [**Folder**](folder.md) object to support offline folders.</span></span>

## <a name="members"></a><span data-ttu-id="40f00-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="40f00-105">Members</span></span>

<span data-ttu-id="40f00-106">Объект **folder2** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="40f00-106">The **Folder2** object has these types of members:</span></span>

-   [<span data-ttu-id="40f00-107">Методы</span><span class="sxs-lookup"><span data-stu-id="40f00-107">Methods</span></span>](#methods)
-   [<span data-ttu-id="40f00-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="40f00-108">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="40f00-109">Методы</span><span class="sxs-lookup"><span data-stu-id="40f00-109">Methods</span></span>

<span data-ttu-id="40f00-110">Объект **folder2** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="40f00-110">The **Folder2** object has these methods.</span></span>



| <span data-ttu-id="40f00-111">Метод</span><span class="sxs-lookup"><span data-stu-id="40f00-111">Method</span></span>                                                                 | <span data-ttu-id="40f00-112">Описание</span><span class="sxs-lookup"><span data-stu-id="40f00-112">Description</span></span>                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="40f00-113">**дисмисседвебвиевбаррикаде**</span><span class="sxs-lookup"><span data-stu-id="40f00-113">**DismissedWebViewBarricade**</span></span>](folder2-dismissedwebviewbarricade.md) | <span data-ttu-id="40f00-114">Вызывается в ответ на веб-представление баррикаде, закрытое пользователем.</span><span class="sxs-lookup"><span data-stu-id="40f00-114">Called in response to the web view barricade being dismissed by the user.</span></span><br/> |
| [<span data-ttu-id="40f00-115">**Synchronize**</span><span class="sxs-lookup"><span data-stu-id="40f00-115">**Synchronize**</span></span>](folder2-synchronize.md)                             | <span data-ttu-id="40f00-116">Синхронизирует все автономные файлы в папке.</span><span class="sxs-lookup"><span data-stu-id="40f00-116">Synchronizes all offline files in the folder.</span></span><br/>                             |



 

### <a name="properties"></a><span data-ttu-id="40f00-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="40f00-117">Properties</span></span>

<span data-ttu-id="40f00-118">Объект **folder2** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="40f00-118">The **Folder2** object has these properties.</span></span>



| <span data-ttu-id="40f00-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="40f00-119">Property</span></span>                                                                            | <span data-ttu-id="40f00-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="40f00-120">Access type</span></span>          | <span data-ttu-id="40f00-121">Описание</span><span class="sxs-lookup"><span data-stu-id="40f00-121">Description</span></span>                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="40f00-122">**хаветошоввебвиевбаррикаде**</span><span class="sxs-lookup"><span data-stu-id="40f00-122">**HaveToShowWebViewBarricade**</span></span>](folder2-havetoshowwebviewbarricade.md)<br/> | <span data-ttu-id="40f00-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f00-123">Read-only</span></span><br/> | <span data-ttu-id="40f00-124">В настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="40f00-124">Not currently supported.</span></span><br/>                                       |
| [<span data-ttu-id="40f00-125">**оффлинестатус**</span><span class="sxs-lookup"><span data-stu-id="40f00-125">**OfflineStatus**</span></span>](folder2-offlinestatus.md)<br/>                           | <span data-ttu-id="40f00-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f00-126">Read-only</span></span><br/> | <span data-ttu-id="40f00-127">Содержит автономное состояние папки.</span><span class="sxs-lookup"><span data-stu-id="40f00-127">Contains the offline status of the folder.</span></span><br/>                     |
| [<span data-ttu-id="40f00-128">**Самообслуживания**</span><span class="sxs-lookup"><span data-stu-id="40f00-128">**Self**</span></span>](folder2-self.md)<br/>                                             | <span data-ttu-id="40f00-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="40f00-129">Read-only</span></span><br/> | <span data-ttu-id="40f00-130">Содержит объект [**FolderItem**](folderitem.md) папки.</span><span class="sxs-lookup"><span data-stu-id="40f00-130">Contains the folder's [**FolderItem**](folderitem.md) object.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="40f00-131">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="40f00-131">Requirements</span></span>



| <span data-ttu-id="40f00-132">Требование</span><span class="sxs-lookup"><span data-stu-id="40f00-132">Requirement</span></span> | <span data-ttu-id="40f00-133">Значение</span><span class="sxs-lookup"><span data-stu-id="40f00-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f00-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40f00-134">Minimum supported client</span></span><br/> | <span data-ttu-id="40f00-135">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="40f00-135">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40f00-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40f00-136">Minimum supported server</span></span><br/> | <span data-ttu-id="40f00-137">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="40f00-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="40f00-138">Заголовок</span><span class="sxs-lookup"><span data-stu-id="40f00-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f00-139"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="40f00-139"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="40f00-140">IDL</span><span class="sxs-lookup"><span data-stu-id="40f00-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="40f00-141"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="40f00-141"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="40f00-142">DLL</span><span class="sxs-lookup"><span data-stu-id="40f00-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f00-143"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="40f00-143"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40f00-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40f00-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f00-145">**Папка**</span><span class="sxs-lookup"><span data-stu-id="40f00-145">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




