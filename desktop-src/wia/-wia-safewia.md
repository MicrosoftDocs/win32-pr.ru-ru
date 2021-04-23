---
description: Объект Сафевиа — это &\# 0034; безопасность для скриптов&\# 0034; точка входа для всех функций создания скриптов для получения изображений Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Объект Сафевиа
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711090"
---
# <a name="safewia-object"></a><span data-ttu-id="13f65-103">Объект Сафевиа</span><span class="sxs-lookup"><span data-stu-id="13f65-103">SafeWia object</span></span>

<span data-ttu-id="13f65-104">Объект **сафевиа** — это точка входа "безопасность для скриптов" для всех функций создания скриптов для получения изображений Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="13f65-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="13f65-105">Любое приложение, использующее модель скриптов WIA, должно создавать объект **сафевиа** или [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="13f65-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="13f65-106">Используйте этот объект для перечисления и создания устройств и получения уведомлений о событиях оборудования.</span><span class="sxs-lookup"><span data-stu-id="13f65-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="13f65-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="13f65-107">Members</span></span>

<span data-ttu-id="13f65-108">Объект **сафевиа** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="13f65-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="13f65-109">Методы</span><span class="sxs-lookup"><span data-stu-id="13f65-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="13f65-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="13f65-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="13f65-111">Методы</span><span class="sxs-lookup"><span data-stu-id="13f65-111">Methods</span></span>

<span data-ttu-id="13f65-112">Объект **сафевиа** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="13f65-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="13f65-113">Метод</span><span class="sxs-lookup"><span data-stu-id="13f65-113">Method</span></span>                             | <span data-ttu-id="13f65-114">Описание</span><span class="sxs-lookup"><span data-stu-id="13f65-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13f65-115">**Создания**</span><span class="sxs-lookup"><span data-stu-id="13f65-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="13f65-116">Метод [**CREATE**](-wia-iwia-create.md) объекта [**WIA**](-wia-wia.md) устанавливает соединение с указанным устройством WIA и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="13f65-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="13f65-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="13f65-117">Properties</span></span>

<span data-ttu-id="13f65-118">Объект **сафевиа** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="13f65-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="13f65-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="13f65-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="13f65-120">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="13f65-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="13f65-121">Описание</span><span class="sxs-lookup"><span data-stu-id="13f65-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="13f65-122"><a href="-wia-iwia-devices.md"><strong>Устройства</strong></a></span><span class="sxs-lookup"><span data-stu-id="13f65-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="13f65-123">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="13f65-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="13f65-124">Коллекция объектов <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> , представляющих все устройства, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="13f65-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="13f65-125">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="13f65-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="13f65-126">Эта коллекция основана на 0.</span><span class="sxs-lookup"><span data-stu-id="13f65-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="13f65-127">Требования</span><span class="sxs-lookup"><span data-stu-id="13f65-127">Requirements</span></span>



| <span data-ttu-id="13f65-128">Требование</span><span class="sxs-lookup"><span data-stu-id="13f65-128">Requirement</span></span> | <span data-ttu-id="13f65-129">Значение</span><span class="sxs-lookup"><span data-stu-id="13f65-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f65-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13f65-130">Minimum supported client</span></span><br/> | <span data-ttu-id="13f65-131">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="13f65-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13f65-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13f65-132">Minimum supported server</span></span><br/> | <span data-ttu-id="13f65-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13f65-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="13f65-134">DLL</span><span class="sxs-lookup"><span data-stu-id="13f65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13f65-135"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="13f65-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="13f65-136">IID</span><span class="sxs-lookup"><span data-stu-id="13f65-136">IID</span></span><br/>                      | <span data-ttu-id="13f65-137">\_САФЕВИА CLSID</span><span class="sxs-lookup"><span data-stu-id="13f65-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="13f65-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="13f65-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f65-139">**Одно**</span><span class="sxs-lookup"><span data-stu-id="13f65-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




