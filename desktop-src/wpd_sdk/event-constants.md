---
description: Портативные устройства Windows определяют следующие значения событий.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Константы событий (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695092"
---
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="0f005-103">Константы событий (Портабледевице. h)</span><span class="sxs-lookup"><span data-stu-id="0f005-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="0f005-104">Портативные устройства Windows определяют следующие значения событий.</span><span class="sxs-lookup"><span data-stu-id="0f005-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="0f005-105">Константа</span><span class="sxs-lookup"><span data-stu-id="0f005-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="0f005-106">Описание</span><span class="sxs-lookup"><span data-stu-id="0f005-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="0f005-107"><dt>**\_ \_ \_ обновленные возможности устройства для событий WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="0f005-108">Это событие указывает, что возможности устройства изменились.</span><span class="sxs-lookup"><span data-stu-id="0f005-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="0f005-109">Клиенты должны переделать запрос к устройству, если они внесли какие либо решения на основе возможностей устройства.</span><span class="sxs-lookup"><span data-stu-id="0f005-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="0f005-110"><dt>**\_устройство событий \_ WPD \_ удалено**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="0f005-111">Это событие отправляется при выгрузке драйвера для устройства.</span><span class="sxs-lookup"><span data-stu-id="0f005-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="0f005-112">Как правило, это результат отключения устройства.</span><span class="sxs-lookup"><span data-stu-id="0f005-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="0f005-113">Клиенты должны освободить интерфейс **ипортабледевице** и все интерфейсы [**ипортабледевицесервице**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) , указанные в **\_ \_ параметре события \_ WPD \_ \_ идентификатор устройства PnP**.</span><span class="sxs-lookup"><span data-stu-id="0f005-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="0f005-114"><dt>**\_Сброс устройства с событием WPD \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="0f005-115">Это событие указывает, что устройство будет сброшено, и все подключенные клиенты должны закрыть свои подключения к устройству.</span><span class="sxs-lookup"><span data-stu-id="0f005-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="0f005-116"><dt>**\_ \_ добавлен объект события \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="0f005-117">Это событие указывает на то, что на устройстве доступен новый объект.</span><span class="sxs-lookup"><span data-stu-id="0f005-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="0f005-118"><dt>**\_объект событий \_ WPD \_ удален**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="0f005-119">Это событие отправляется после удаления ранее существующего объекта с устройства.</span><span class="sxs-lookup"><span data-stu-id="0f005-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="0f005-120">Объект может быть объектом содержимого, например, удален файл изображения; или это может быть функциональный объект, например, новое устройство хранения было отключено от устройства.</span><span class="sxs-lookup"><span data-stu-id="0f005-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="0f005-121"><dt>**\_ \_ \_ запрошено перемещение объектов событий WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="0f005-122">Это событие отправляется, чтобы запросить приложение для передачи определенного объекта с устройства.</span><span class="sxs-lookup"><span data-stu-id="0f005-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="0f005-123">Объект обычно является объектом содержимого, например файлом изображения.</span><span class="sxs-lookup"><span data-stu-id="0f005-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="0f005-124"><dt>**\_ \_ обновлен объект события \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="0f005-125">Это событие отправляется после обновления объекта, и любой подключенный клиент должен обновить его представление этого объекта.</span><span class="sxs-lookup"><span data-stu-id="0f005-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="0f005-126"><dt>**\_ \_ метод службы событий \_ WPD \_ завершен**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="0f005-127">Это событие отправляется, когда драйвер завершил вызов метода службы.</span><span class="sxs-lookup"><span data-stu-id="0f005-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="0f005-128">Это событие должно быть отправлено даже при сбое метода.</span><span class="sxs-lookup"><span data-stu-id="0f005-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="0f005-129">Это внутреннее событие DDI для WPD, которое не будет доступно для приложений с помощью [**ипортабледевице:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) или [**Ипортабледевицесервице:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span><span class="sxs-lookup"><span data-stu-id="0f005-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="0f005-130"><dt>**\_ \_ Формат хранения событий \_ WPD**</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="0f005-131">Это событие показывает ход выполнения операции форматирования в объекте хранилища.</span><span class="sxs-lookup"><span data-stu-id="0f005-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="0f005-132">Требования</span><span class="sxs-lookup"><span data-stu-id="0f005-132">Requirements</span></span>



| <span data-ttu-id="0f005-133">Требование</span><span class="sxs-lookup"><span data-stu-id="0f005-133">Requirement</span></span> | <span data-ttu-id="0f005-134">Значение</span><span class="sxs-lookup"><span data-stu-id="0f005-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f005-135">Header</span><span class="sxs-lookup"><span data-stu-id="0f005-135">Header</span></span><br/> | <dl> <span data-ttu-id="0f005-136"><dt>Портабледевице. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f005-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f005-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f005-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f005-138">Константы</span><span class="sxs-lookup"><span data-stu-id="0f005-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




