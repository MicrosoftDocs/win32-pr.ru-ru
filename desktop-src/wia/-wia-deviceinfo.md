---
description: Объект DeviceInfo предоставляет доступ к свойствам аппаратного устройства для получения образа Windows (WIA).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Объект DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 928bc05da4ec97df9d52ce504ccb9dadd649e546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656607"
---
# <a name="deviceinfo-object"></a><span data-ttu-id="5a186-103">Объект DeviceInfo</span><span class="sxs-lookup"><span data-stu-id="5a186-103">DeviceInfo object</span></span>

<span data-ttu-id="5a186-104">Объект **DeviceInfo** предоставляет доступ к свойствам аппаратного устройства для получения образа Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="5a186-104">The **DeviceInfo** object provides access to the properties of a Windows Image Acquisition (WIA) hardware device.</span></span> <span data-ttu-id="5a186-105">Кроме того, метод [**CREATE**](-wia-iwiadeviceinfo-create.md) позволяет приложению или сценарию подключиться к устройству и получить объект [**элемента**](-wia-item.md) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="5a186-105">It also, through its [**Create**](-wia-iwiadeviceinfo-create.md) method, provides a way for the application or script to connect to the device and obtain an [**Item**](-wia-item.md) object that represents the device.</span></span> <span data-ttu-id="5a186-106">Используйте метод [**Devices**](-wia-iwia-devices.md) для получения коллекции объектов **DeviceInfo** .</span><span class="sxs-lookup"><span data-stu-id="5a186-106">Use the [**Devices**](-wia-iwia-devices.md) method to obtain a collection of **DeviceInfo** objects.</span></span>

## <a name="members"></a><span data-ttu-id="5a186-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="5a186-107">Members</span></span>

<span data-ttu-id="5a186-108">Объект **DeviceInfo** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5a186-108">The **DeviceInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="5a186-109">Методы</span><span class="sxs-lookup"><span data-stu-id="5a186-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="5a186-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a186-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="5a186-111">Методы</span><span class="sxs-lookup"><span data-stu-id="5a186-111">Methods</span></span>

<span data-ttu-id="5a186-112">Объект **DeviceInfo** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="5a186-112">The **DeviceInfo** object has these methods.</span></span>



| <span data-ttu-id="5a186-113">Метод</span><span class="sxs-lookup"><span data-stu-id="5a186-113">Method</span></span>                                                 | <span data-ttu-id="5a186-114">Описание</span><span class="sxs-lookup"><span data-stu-id="5a186-114">Description</span></span>                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a186-115">**Создания**</span><span class="sxs-lookup"><span data-stu-id="5a186-115">**Create**</span></span>](-wia-iwiadeviceinfo-create.md)           | <span data-ttu-id="5a186-116">Метод [**CREATE**](-wia-iwiadeviceinfo-create.md) объекта **DeviceInfo** устанавливает соединение с устройством WIA, заданным объектом **DeviceInfo** , и возвращает объект [**Item**](-wia-item.md) , представляющий устройство.</span><span class="sxs-lookup"><span data-stu-id="5a186-116">The [**Create**](-wia-iwiadeviceinfo-create.md) method of the **DeviceInfo** object makes a connection to the WIA device specified by the **DeviceInfo** object, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |
| [<span data-ttu-id="5a186-117">**жетпропбид**</span><span class="sxs-lookup"><span data-stu-id="5a186-117">**GetPropById**</span></span>](-wia-iwiadeviceinfo-getpropbyid.md) | <span data-ttu-id="5a186-118">Метод [**жетпропбид**](-wia-iwiadeviceinfo-getpropbyid.md) объекта **DeviceInfo** использует идентификатор свойства устройства для возвращения его значения.</span><span class="sxs-lookup"><span data-stu-id="5a186-118">The [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) method of the **DeviceInfo** object uses a device property's ID to return its value.</span></span><br/>                                                                                               |



 

### <a name="properties"></a><span data-ttu-id="5a186-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="5a186-119">Properties</span></span>

<span data-ttu-id="5a186-120">Объект **DeviceInfo** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5a186-120">The **DeviceInfo** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="5a186-121">Свойство</span><span class="sxs-lookup"><span data-stu-id="5a186-121">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="5a186-122">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="5a186-122">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="5a186-123">Описание</span><span class="sxs-lookup"><span data-stu-id="5a186-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="5a186-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Удостоверения</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a186-124"><a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a186-125">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-126">Получает идентификатор аппаратного устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="5a186-126">Retrieves the ID of the WIA hardware device.</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="5a186-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Производителя</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a186-127"><a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Manufacturer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a186-128">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-129">Извлекает имя производителя данного устройства.</span><span class="sxs-lookup"><span data-stu-id="5a186-129">Retrieves the name of the manufacturer of this hardware device.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="5a186-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Имя</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a186-130"><a href="-wia-iwiadeviceinfo-name.md"><strong>Name</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-131">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a186-131">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-132">Имя аппаратного устройства WIA, отображаемое в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="5a186-132">The name of the WIA hardware device as it appears in the UI.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="5a186-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Порту</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a186-133"><a href="-wia-iwiadeviceinfo-port.md"><strong>Port</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-134">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a186-134">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-135">Извлекает порт, к которому подключено аппаратное устройство WIA.</span><span class="sxs-lookup"><span data-stu-id="5a186-135">Retrieves the port to which the WIA hardware device is connected.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="5a186-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Тип</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a186-136"><a href="-wia-iwiadeviceinfo-type.md"><strong>Type</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-137">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a186-137">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-138">Возвращает тип аппаратного устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="5a186-138">Retrieves the type of WIA hardware device.</span></span> <span data-ttu-id="5a186-139">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="5a186-139">Possible values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="5a186-140">дигиталкамера</span><span class="sxs-lookup"><span data-stu-id="5a186-140">DigitalCamera</span></span></li>
<li><span data-ttu-id="5a186-141">Сканер</span><span class="sxs-lookup"><span data-stu-id="5a186-141">Scanner</span></span></li>
<li><span data-ttu-id="5a186-142">стреамингвидео</span><span class="sxs-lookup"><span data-stu-id="5a186-142">StreamingVideo</span></span></li>
<li><span data-ttu-id="5a186-143">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5a186-143">Default</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="5a186-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>уиклсид</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a186-144"><a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="5a186-145">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="5a186-146">Получает идентификатор класса пользовательского интерфейса, предоставленного изготовителем для этого аппаратного устройства WIA.</span><span class="sxs-lookup"><span data-stu-id="5a186-146">Retrieves the class id of the manufacturer-provided user interface for this WIA hardware device.</span></span> <span data-ttu-id="5a186-147">Значение представляет собой строковое представление GUID.</span><span class="sxs-lookup"><span data-stu-id="5a186-147">The value is a string representation of a GUID.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="5a186-148">Требования</span><span class="sxs-lookup"><span data-stu-id="5a186-148">Requirements</span></span>



| <span data-ttu-id="5a186-149">Требование</span><span class="sxs-lookup"><span data-stu-id="5a186-149">Requirement</span></span> | <span data-ttu-id="5a186-150">Значение</span><span class="sxs-lookup"><span data-stu-id="5a186-150">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a186-151">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a186-151">Minimum supported client</span></span><br/> | <span data-ttu-id="5a186-152">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a186-152">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a186-153">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a186-153">Minimum supported server</span></span><br/> | <span data-ttu-id="5a186-154">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a186-154">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5a186-155">DLL</span><span class="sxs-lookup"><span data-stu-id="5a186-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a186-156"><dt>Wiascr.dll (версия 4,90 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="5a186-156"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




