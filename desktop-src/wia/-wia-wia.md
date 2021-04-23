---
description: Объект WIA — это точка входа для всех функций создания скриптов для получения изображений Windows (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104145346"
---
# <a name="wia-object"></a><span data-ttu-id="1a706-103">WIA, объект</span><span class="sxs-lookup"><span data-stu-id="1a706-103">Wia object</span></span>

<span data-ttu-id="1a706-104">Объект **WIA** — это точка входа для всех функций создания скриптов для получения изображений Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="1a706-104">The **Wia** object is the entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="1a706-105">Любое приложение, использующее модель скриптов WIA, должно создавать объект [**сафевиа**](-wia-safewia.md) или **WIA** .</span><span class="sxs-lookup"><span data-stu-id="1a706-105">Any application that uses the WIA scripting model must create a [**SafeWia**](-wia-safewia.md) or **Wia** object.</span></span> <span data-ttu-id="1a706-106">Используйте этот объект для перечисления и создания устройств и получения уведомлений о событиях оборудования.</span><span class="sxs-lookup"><span data-stu-id="1a706-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

> [!Note]  
> <span data-ttu-id="1a706-107">Этот объект не является надежным для скриптов.</span><span class="sxs-lookup"><span data-stu-id="1a706-107">This object is not safe for scripting.</span></span> <span data-ttu-id="1a706-108">Версию этого объекта, которая является надежной для скриптов, см. в разделе [**сафевиа**](-wia-safewia.md).</span><span class="sxs-lookup"><span data-stu-id="1a706-108">For a version of this object that is safe for scripting, see [**SafeWia**](-wia-safewia.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="1a706-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="1a706-109">Members</span></span>

<span data-ttu-id="1a706-110">Объект **WIA** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1a706-110">The **Wia** object has these types of members:</span></span>

-   [<span data-ttu-id="1a706-111">События</span><span class="sxs-lookup"><span data-stu-id="1a706-111">Events</span></span>](#events)
-   [<span data-ttu-id="1a706-112">Методы</span><span class="sxs-lookup"><span data-stu-id="1a706-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="1a706-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a706-113">Properties</span></span>](#properties)

### <a name="events"></a><span data-ttu-id="1a706-114">События</span><span class="sxs-lookup"><span data-stu-id="1a706-114">Events</span></span>

<span data-ttu-id="1a706-115">Объект **WIA** содержит эти события.</span><span class="sxs-lookup"><span data-stu-id="1a706-115">The **Wia** object has these events.</span></span>



| <span data-ttu-id="1a706-116">Событие</span><span class="sxs-lookup"><span data-stu-id="1a706-116">Event</span></span>                                                                 | <span data-ttu-id="1a706-117">Описание</span><span class="sxs-lookup"><span data-stu-id="1a706-117">Description</span></span>                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="1a706-118">**ондевицеконнектед**</span><span class="sxs-lookup"><span data-stu-id="1a706-118">**OnDeviceConnected**</span></span>](-wia--iwiaevents-ondeviceconnected.md)       | <span data-ttu-id="1a706-119">Событие, возникающее при подключении нового аппаратного устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="1a706-119">Event that occurs when a new WIA hardware device is connected.</span></span><br/>    |
| [<span data-ttu-id="1a706-120">**ондевицедисконнектед**</span><span class="sxs-lookup"><span data-stu-id="1a706-120">**OnDeviceDisconnected**</span></span>](-wia--iwiaevents-ondevicedisconnected.md) | <span data-ttu-id="1a706-121">Событие, возникающее при отключении нового аппаратного устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="1a706-121">Event that occurs when a new WIA hardware device is disconnected.</span></span><br/> |
| [<span data-ttu-id="1a706-122">**онтрансферкомплете**</span><span class="sxs-lookup"><span data-stu-id="1a706-122">**OnTransferComplete**</span></span>](-wia--iwiaevents-ontransfercomplete.md)     | <span data-ttu-id="1a706-123">Событие, возникающее при успешном завершении обмена данными.</span><span class="sxs-lookup"><span data-stu-id="1a706-123">Event that occurs when a data transfer is completed successfully.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="1a706-124">Методы</span><span class="sxs-lookup"><span data-stu-id="1a706-124">Methods</span></span>

<span data-ttu-id="1a706-125">Объект **WIA** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="1a706-125">The **Wia** object has these methods.</span></span>



| <span data-ttu-id="1a706-126">Метод</span><span class="sxs-lookup"><span data-stu-id="1a706-126">Method</span></span>                             | <span data-ttu-id="1a706-127">Описание</span><span class="sxs-lookup"><span data-stu-id="1a706-127">Description</span></span>                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a706-128">**Создания**</span><span class="sxs-lookup"><span data-stu-id="1a706-128">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="1a706-129">Метод [**CREATE**](-wia-iwia-create.md) объекта **WIA** устанавливает соединение с указанным устройством WIA и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="1a706-129">The [**Create**](-wia-iwia-create.md) method of the **Wia** object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1a706-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a706-130">Properties</span></span>

<span data-ttu-id="1a706-131">Объект **WIA** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1a706-131">The **Wia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="1a706-132">Свойство</span><span class="sxs-lookup"><span data-stu-id="1a706-132">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1a706-133">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="1a706-133">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="1a706-134">Описание</span><span class="sxs-lookup"><span data-stu-id="1a706-134">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="1a706-135"><a href="-wia-iwia-devices.md"><strong>Устройства</strong></a></span><span class="sxs-lookup"><span data-stu-id="1a706-135"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1a706-136">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1a706-136">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="1a706-137">Коллекция объектов <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> , представляющих все устройства, установленные на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1a706-137">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="1a706-138">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1a706-138">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1a706-139">Эта коллекция основана на 0.</span><span class="sxs-lookup"><span data-stu-id="1a706-139">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="1a706-140">Требования</span><span class="sxs-lookup"><span data-stu-id="1a706-140">Requirements</span></span>



| <span data-ttu-id="1a706-141">Требование</span><span class="sxs-lookup"><span data-stu-id="1a706-141">Requirement</span></span> | <span data-ttu-id="1a706-142">Значение</span><span class="sxs-lookup"><span data-stu-id="1a706-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a706-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a706-143">Minimum supported client</span></span><br/> | <span data-ttu-id="1a706-144">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1a706-144">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1a706-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a706-145">Minimum supported server</span></span><br/> | <span data-ttu-id="1a706-146">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a706-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1a706-147">DLL</span><span class="sxs-lookup"><span data-stu-id="1a706-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a706-148"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="1a706-148"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="1a706-149">IID</span><span class="sxs-lookup"><span data-stu-id="1a706-149">IID</span></span><br/>                      | <span data-ttu-id="1a706-150">CLSID для класса \_ WIA</span><span class="sxs-lookup"><span data-stu-id="1a706-150">CLSID\_Wia</span></span><br/>                                                                                         |



 

 




