---
description: Портативные устройства Windows поддерживают следующие свойства событий.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Свойства события (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699225"
---
# <a name="event-properties"></a><span data-ttu-id="6a8db-103">Свойства события</span><span class="sxs-lookup"><span data-stu-id="6a8db-103">Event Properties</span></span>

<span data-ttu-id="6a8db-104">Портативные устройства Windows поддерживают следующие свойства событий.</span><span class="sxs-lookup"><span data-stu-id="6a8db-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6a8db-105">Свойство</span><span class="sxs-lookup"><span data-stu-id="6a8db-105">Property</span></span></th>
<th><span data-ttu-id="6a8db-106">VarType</span><span class="sxs-lookup"><span data-stu-id="6a8db-106">VarType</span></span></th>
<th><span data-ttu-id="6a8db-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6a8db-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6a8db-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="6a8db-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="6a8db-110">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="6a8db-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a8db-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="6a8db-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="6a8db-113">Логическое значение, указывающее, является ли событие широковещательным для всех клиентов. Клиенты могут получить это событие, зарегистрировав обратный вызов с помощью <strong>ипортабледевице:: Advise</strong>.</span><span class="sxs-lookup"><span data-stu-id="6a8db-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a8db-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="6a8db-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="6a8db-116">Логическое значение, указывающее, изменилась ли дочерняя иерархия объекта. Этот параметр используется для уведомления вызывающей стороны о том, что некоторые дочерние элементы для указанного объекта были добавлены или удалены.</span><span class="sxs-lookup"><span data-stu-id="6a8db-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="6a8db-117">Обычно изменение иерархии инициируется на стороне устройства.</span><span class="sxs-lookup"><span data-stu-id="6a8db-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="6a8db-118">Клиентам может потребоваться перечислить дочерние элементы этой папки для обновления своих представлений.</span><span class="sxs-lookup"><span data-stu-id="6a8db-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a8db-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="6a8db-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="6a8db-121">Значение, идентифицирующее событие.</span><span class="sxs-lookup"><span data-stu-id="6a8db-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a8db-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="6a8db-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="6a8db-124">Файл cookie передаются обратно клиенту при запросе создания объекта путем вызова метода <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>ипортабледевицеконтент:: креатеобжектвиспропертиесанддата</strong></a> . Этот параметр добавляется в качестве удобства, чтобы вызывающий объект привязать событие, добавленное к объекту, к запросу, отправленному для создания объекта.</span><span class="sxs-lookup"><span data-stu-id="6a8db-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="6a8db-125">Драйвер передает этот файл cookie обратно в качестве <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> возвращаемого значения при обработке команды <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .</span><span class="sxs-lookup"><span data-stu-id="6a8db-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a8db-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="6a8db-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="6a8db-128">Значение, уникально идентифицирующее родительский объект.</span><span class="sxs-lookup"><span data-stu-id="6a8db-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="6a8db-129">Это свойство похоже на <strong>WPD_OBJECT_PARENT_ID</strong>, но этот идентификатор не меняется между сеансами.</span><span class="sxs-lookup"><span data-stu-id="6a8db-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a8db-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="6a8db-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="6a8db-132">Значение типа, указывающее ход выполнения выполняемой в данный момент операции.</span><span class="sxs-lookup"><span data-stu-id="6a8db-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="6a8db-133">Значение этого свойства может находиться в диапазоне от 0 до 100 с 100, указывающим, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="6a8db-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a8db-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="6a8db-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="6a8db-136">Значение, указывающее текущее состояние операции, например "запущено", "запущено", "остановлено" и т. д. Возможные значения этого параметра относятся к перечислению <strong>WPD_OPERATION_STATES</strong> , определенному в портабледевице. h.</span><span class="sxs-lookup"><span data-stu-id="6a8db-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="6a8db-137">Возможны следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6a8db-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="6a8db-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="6a8db-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="6a8db-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="6a8db-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="6a8db-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="6a8db-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="6a8db-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6a8db-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="6a8db-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="6a8db-147">Значение типа, указывающее устройство, которое является источником события. Это устройство или идентификатор службы, заданные системой Plug-and-Play, и — это та же строка, которая используется в методах <strong>ипортабледевице:: Open</strong>или <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>Ипортабледевицесервице:: Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="6a8db-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6a8db-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="6a8db-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="6a8db-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="6a8db-150">Строка, используемая драйвером WPD для обнаружения операций метода службы устройства.</span><span class="sxs-lookup"><span data-stu-id="6a8db-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="6a8db-151">Приложения не должны использовать этот параметр напрямую.</span><span class="sxs-lookup"><span data-stu-id="6a8db-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="6a8db-152">Требования</span><span class="sxs-lookup"><span data-stu-id="6a8db-152">Requirements</span></span>



| <span data-ttu-id="6a8db-153">Требование</span><span class="sxs-lookup"><span data-stu-id="6a8db-153">Requirement</span></span> | <span data-ttu-id="6a8db-154">Значение</span><span class="sxs-lookup"><span data-stu-id="6a8db-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8db-155">Header</span><span class="sxs-lookup"><span data-stu-id="6a8db-155">Header</span></span><br/> | <dl> <span data-ttu-id="6a8db-156"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a8db-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a8db-157">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6a8db-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8db-158">**Свойства и атрибуты WPD**</span><span class="sxs-lookup"><span data-stu-id="6a8db-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




