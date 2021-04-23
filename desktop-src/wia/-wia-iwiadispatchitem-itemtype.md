---
description: Тип этого элемента. Только для чтения.
ms.assetid: 6c613a08-41aa-4242-80c0-75e1981a676f
title: Свойство Item. ItemType
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.ItemType
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 9b70f7a1698ecdb4de023786f21a6ef9d55f681d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719512"
---
# <a name="itemitemtype-property"></a><span data-ttu-id="db147-104">Свойство Item. ItemType</span><span class="sxs-lookup"><span data-stu-id="db147-104">Item.ItemType property</span></span>

<span data-ttu-id="db147-105">Тип этого элемента.</span><span class="sxs-lookup"><span data-stu-id="db147-105">The type of this item.</span></span> <span data-ttu-id="db147-106">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="db147-106">Read-only.</span></span>

<span data-ttu-id="db147-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="db147-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="db147-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db147-108">Syntax</span></span>


```JScript
propVal = Item.ItemType
```



## <a name="property-value"></a><span data-ttu-id="db147-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="db147-109">Property value</span></span>

<span data-ttu-id="db147-110">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="db147-110">The following values are possible:</span></span>



| <span data-ttu-id="db147-111">Значение</span><span class="sxs-lookup"><span data-stu-id="db147-111">Value</span></span>  | <span data-ttu-id="db147-112">Описание</span><span class="sxs-lookup"><span data-stu-id="db147-112">Description</span></span>                                     |
|--------|-------------------------------------------------|
| <span data-ttu-id="db147-113">device</span><span class="sxs-lookup"><span data-stu-id="db147-113">device</span></span> | <span data-ttu-id="db147-114">Элемент является аппаратным устройством WIA.</span><span class="sxs-lookup"><span data-stu-id="db147-114">The item is a WIA hardware device.</span></span>              |
| <span data-ttu-id="db147-115">folder</span><span class="sxs-lookup"><span data-stu-id="db147-115">folder</span></span> | <span data-ttu-id="db147-116">Элемент — это папка, содержащая другие элементы.</span><span class="sxs-lookup"><span data-stu-id="db147-116">The item is a folder that contains other items.</span></span> |
| <span data-ttu-id="db147-117">файл</span><span class="sxs-lookup"><span data-stu-id="db147-117">file</span></span>   | <span data-ttu-id="db147-118">Элемент является изображением или звуковым файлом.</span><span class="sxs-lookup"><span data-stu-id="db147-118">The item is an image or audio file.</span></span>             |
| <span data-ttu-id="db147-119">звук</span><span class="sxs-lookup"><span data-stu-id="db147-119">audio</span></span>  | <span data-ttu-id="db147-120">Элемент является аудиоклипом.</span><span class="sxs-lookup"><span data-stu-id="db147-120">The item is an audio clip.</span></span>                      |
| <span data-ttu-id="db147-121">Изображение</span><span class="sxs-lookup"><span data-stu-id="db147-121">image</span></span>  | <span data-ttu-id="db147-122">Элемент является изображением.</span><span class="sxs-lookup"><span data-stu-id="db147-122">The item is an image.</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="db147-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db147-123">Remarks</span></span>

<span data-ttu-id="db147-124">Элемент может иметь более одного типа.</span><span class="sxs-lookup"><span data-stu-id="db147-124">An item can have more than one type.</span></span> <span data-ttu-id="db147-125">Например, все изображения имеют типы "Image" и "File".</span><span class="sxs-lookup"><span data-stu-id="db147-125">For example, every image is of both "image" and "file" types.</span></span> <span data-ttu-id="db147-126">**ItemType** возвращает строку, включающую все допустимые типы элемента, разделенные точкой с запятой.</span><span class="sxs-lookup"><span data-stu-id="db147-126">**ItemType** returns a string that includes all valid types for the item, separated by semicolons.</span></span> <span data-ttu-id="db147-127">Например, "Image; File".</span><span class="sxs-lookup"><span data-stu-id="db147-127">For example, "image;file".</span></span> <span data-ttu-id="db147-128">В этой строке нет пробелов, и в конце отсутствует точка с запятой.</span><span class="sxs-lookup"><span data-stu-id="db147-128">There are no spaces in this string, and there is not a semicolon at the end.</span></span>

## <a name="requirements"></a><span data-ttu-id="db147-129">Требования</span><span class="sxs-lookup"><span data-stu-id="db147-129">Requirements</span></span>



| <span data-ttu-id="db147-130">Требование</span><span class="sxs-lookup"><span data-stu-id="db147-130">Requirement</span></span> | <span data-ttu-id="db147-131">Значение</span><span class="sxs-lookup"><span data-stu-id="db147-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db147-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db147-132">Minimum supported client</span></span><br/> | <span data-ttu-id="db147-133">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="db147-133">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="db147-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db147-134">Minimum supported server</span></span><br/> | <span data-ttu-id="db147-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="db147-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="db147-136">DLL</span><span class="sxs-lookup"><span data-stu-id="db147-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db147-137"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="db147-137"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




