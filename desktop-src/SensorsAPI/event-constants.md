---
description: Платформа датчиков и расположения Windows определяет константы для событий драйвера. Манфуактуререс датчика также может определять собственные константы.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Константы событий (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663911"
---
# <a name="event-constants-sensorsh"></a><span data-ttu-id="ce1e2-104">Константы событий (sensors. h)</span><span class="sxs-lookup"><span data-stu-id="ce1e2-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="ce1e2-105">Платформа датчиков и расположения Windows определяет константы для событий драйвера.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="ce1e2-106">Манфуактуререс датчика также может определять собственные константы.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="ce1e2-107">**Типы событий датчика**</span><span class="sxs-lookup"><span data-stu-id="ce1e2-107">**Sensor Event Types**</span></span>

<span data-ttu-id="ce1e2-108">Платформа определяет следующие идентификаторы типов событий датчика.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="ce1e2-109">Тип события датчика</span><span class="sxs-lookup"><span data-stu-id="ce1e2-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="ce1e2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ce1e2-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="ce1e2-111"><dt>**Датчик \_ \_АКСЕЛЕРОМЕТР событий \_ встряхните**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="ce1e2-112">Указывает, что устройство было Шакен.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="ce1e2-113"><dt>**Датчик \_ \_Данные события \_ обновлены**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="ce1e2-114">Указывает, что новые данные доступны.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="ce1e2-115"><dt>**Датчик \_ \_Свойство события \_ изменено**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="ce1e2-116">Указывает, что значение свойства изменилось.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-116">Indicates that a property value changed.</span></span> <span data-ttu-id="ce1e2-117">Проверьте интерфейс [ипортабледевицевалуес](/previous-versions//ms740012(v=vs.85)) , передаваемый через параметр *певентдата* , в значение [**oneven**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), чтобы определить, какое свойство изменилось и его новое значение.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="ce1e2-118"><dt>**Датчик \_ \_Состояние события \_ изменено**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="ce1e2-119">Указывает изменение операционного состояния, например \_ состояние датчика \_ Инициализация до \_ состояния датчика \_ Готово.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="ce1e2-120">**Пропертикэйс события датчика**</span><span class="sxs-lookup"><span data-stu-id="ce1e2-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="ce1e2-121">Ключи свойств, определяемые платформой для событий, основаны на следующем идентификаторе GUID:</span><span class="sxs-lookup"><span data-stu-id="ce1e2-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="ce1e2-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span><span class="sxs-lookup"><span data-stu-id="ce1e2-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="ce1e2-123">Платформа датчика определяет следующие **PROPERTYKEY**, которые определяют параметры событий датчика.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="ce1e2-124">PROPERTYKEY событий датчика и PID</span><span class="sxs-lookup"><span data-stu-id="ce1e2-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="ce1e2-125">Описание</span><span class="sxs-lookup"><span data-stu-id="ce1e2-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="ce1e2-126"><dt>**Датчик \_ \_ \_ \_ ИД события параметра события**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="ce1e2-127">Указывает, что значение **идентификатора GUID** в [ипортабледевицевалуес](/previous-versions//ms740012(v=vs.85)) является идентификатором типа события, например \_ \_ обновленными данными о событии датчика \_ .</span><span class="sxs-lookup"><span data-stu-id="ce1e2-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="ce1e2-128"><dt>**Датчик \_ \_ \_ Состояние параметра события**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="ce1e2-129">Указывает, что целочисленное значение без знака в **ипортабледевицевалуес** является состоянием датчика, например, \_ состояние датчика \_ Готово.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="ce1e2-130">**Ошибка датчика Пропертикэйс**</span><span class="sxs-lookup"><span data-stu-id="ce1e2-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="ce1e2-131">Ключи свойств, определяемые платформой, для ошибок будут основываться на следующем GUID:</span><span class="sxs-lookup"><span data-stu-id="ce1e2-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="ce1e2-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span><span class="sxs-lookup"><span data-stu-id="ce1e2-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="ce1e2-133">Платформа датчика резервирует этот идентификатор GUID для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="ce1e2-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="ce1e2-134">Требования</span><span class="sxs-lookup"><span data-stu-id="ce1e2-134">Requirements</span></span>



| <span data-ttu-id="ce1e2-135">Требование</span><span class="sxs-lookup"><span data-stu-id="ce1e2-135">Requirement</span></span> | <span data-ttu-id="ce1e2-136">Значение</span><span class="sxs-lookup"><span data-stu-id="ce1e2-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce1e2-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce1e2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ce1e2-138">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ce1e2-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce1e2-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce1e2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ce1e2-140">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce1e2-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ce1e2-141">Header</span><span class="sxs-lookup"><span data-stu-id="ce1e2-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce1e2-142"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce1e2-142"><dt>Sensors.h</dt></span></span> </dl> |



 

