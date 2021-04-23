---
description: Категория датчика \_ \_ другая категория содержит датчики, которые поддерживают пользовательский класс в драйвере класса HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072682"
---
# <a name="sensor_category_other"></a><span data-ttu-id="06995-103">\_другая категория \_ датчика</span><span class="sxs-lookup"><span data-stu-id="06995-103">SENSOR\_CATEGORY\_OTHER</span></span>

<span data-ttu-id="06995-104">Категория датчика \_ \_ другая категория содержит датчики, которые поддерживают пользовательский класс в драйвере класса HID.</span><span class="sxs-lookup"><span data-stu-id="06995-104">The SENSOR\_CATEGORY\_OTHER category contains sensors that support the Custom class in the HID Class driver.</span></span>

<dl> <dt>

<span data-ttu-id="06995-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**Тип датчика — \_ \_ настраиваемый**</span><span class="sxs-lookup"><span data-stu-id="06995-105"><span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**SENSOR\_TYPE\_CUSTOM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="06995-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span><span class="sxs-lookup"><span data-stu-id="06995-106">{E83AF229-8640-4D18-A213-E22675EBB2C3}</span></span>
</dt> <dt>



<span data-ttu-id="06995-107">Пользовательский датчик, поддерживающий пользовательский класс в драйвере класса HID.</span><span class="sxs-lookup"><span data-stu-id="06995-107">Custom sensor that supports the Custom class in the HID Class driver.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="06995-108">**Поля данных, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="06995-108">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="06995-109">Ключи свойств, определяемые платформой для этой категории, основаны на \_ \_ пользовательском GUID типа данных датчика \_ \_ :</span><span class="sxs-lookup"><span data-stu-id="06995-109">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_CUSTOM\_GUID:</span></span>

<span data-ttu-id="06995-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span><span class="sxs-lookup"><span data-stu-id="06995-110">{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}</span></span>

<span data-ttu-id="06995-111">Эта категория включает следующие поля данных, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="06995-111">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="06995-112">Имя поля данных и идентификатор процесса</span><span class="sxs-lookup"><span data-stu-id="06995-112">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="06995-113">Описание</span><span class="sxs-lookup"><span data-stu-id="06995-113">Description</span></span>                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <span data-ttu-id="06995-114"><dt>**Датчик \_ \_ \_ Пользовательское \_ Использование типа данных**</dt> <dt> (PID = 5)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-114"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_USAGE**</dt> <dt> (PID = 5) </dt></span></span> </dl>                          | <span data-ttu-id="06995-115">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="06995-115">**VT\_UI4**</span></span><br/> <span data-ttu-id="06995-116">Использование HID, которое можно использовать для различения нескольких настраиваемых датчиков.</span><span class="sxs-lookup"><span data-stu-id="06995-116">A HID usage which can be used to distinguish multiple, custom sensors.</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <span data-ttu-id="06995-117"><dt>**Датчик \_ \_ \_ Пользовательский \_ логический \_ массив типа данных**</dt> <dt> (PID = 6)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-117"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_BOOLEAN\_ARRAY**</dt> <dt> (PID = 6) </dt></span></span> </dl> | <span data-ttu-id="06995-118">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="06995-118">**VT\_UI4**</span></span><br/> <span data-ttu-id="06995-119">Массив логических значений для заданного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-119">An array of Boolean values for a given custom sensor.</span></span><br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <span data-ttu-id="06995-120"><dt>**Датчик \_ \_Тип данных \_ Custom \_ Значение1**</dt> <dt> (PID = 7)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-120"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE1**</dt> <dt> (PID = 7) </dt></span></span> </dl>                       | <span data-ttu-id="06995-121">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="06995-121">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="06995-122">Одно из шести доступных значений для данного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-122">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <span data-ttu-id="06995-123"><dt>**Датчик \_ \_Тип данных \_ Custom \_ VALUE2**</dt> <dt> (PID = 8)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-123"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE2**</dt> <dt> (PID = 8) </dt></span></span> </dl>                       | <span data-ttu-id="06995-124">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="06995-124">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="06995-125">Одно из шести доступных значений для данного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-125">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <span data-ttu-id="06995-126"><dt>**Датчик \_ \_Тип данных \_ Custom \_ значение3**</dt> <dt> (PID = 9)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-126"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE3**</dt> <dt> (PID = 9) </dt></span></span> </dl>                       | <span data-ttu-id="06995-127">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="06995-127">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="06995-128">Одно из шести доступных значений для данного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-128">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <span data-ttu-id="06995-129"><dt>**Датчик \_ \_Тип данных \_ Custom \_ VALUE4**</dt> <dt> (PID = 10)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-129"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE4**</dt> <dt> (PID = 10) </dt></span></span> </dl>                      | <span data-ttu-id="06995-130">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="06995-130">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="06995-131">Одно из шести доступных значений для данного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-131">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <span data-ttu-id="06995-132"><dt>**Датчик \_ \_Тип данных \_ Custom \_ VALUE5**</dt> <dt> (PID = 11)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-132"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE5**</dt> <dt> (PID = 11) </dt></span></span> </dl>                      | <span data-ttu-id="06995-133">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="06995-133">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="06995-134">Одно из шести доступных значений для данного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-134">One of six available values for a given custom sensor.</span></span><br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <span data-ttu-id="06995-135"><dt>**Датчик \_ \_Тип данных \_ Custom \_ VALUE6**</dt> <dt> (PID = 12)</dt></span><span class="sxs-lookup"><span data-stu-id="06995-135"><dt>**SENSOR\_DATA\_TYPE\_CUSTOM\_VALUE6**</dt> <dt> (PID = 12) </dt></span></span> </dl>                      | <span data-ttu-id="06995-136">**VT \_ UI4 \| \| VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="06995-136">**VT\_UI4\|\|VT\_R4**</span></span><br/> <span data-ttu-id="06995-137">Одно из шести доступных значений для данного пользовательского датчика.</span><span class="sxs-lookup"><span data-stu-id="06995-137">One of six available values for a given custom sensor.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="06995-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06995-138">Remarks</span></span>

<span data-ttu-id="06995-139">Датчик, поддерживающий универсальный класс в драйвере класса HID, будет сопоставляться с одной из других определенных категорий (биометрическая, электрическая, среда и т. д.).</span><span class="sxs-lookup"><span data-stu-id="06995-139">A sensor that supports the Generic class in the HID class driver will map to one of the other defined categories (biometric, electrical, environmental, and so on).</span></span>

## <a name="requirements"></a><span data-ttu-id="06995-140">Требования</span><span class="sxs-lookup"><span data-stu-id="06995-140">Requirements</span></span>



| <span data-ttu-id="06995-141">Требование</span><span class="sxs-lookup"><span data-stu-id="06995-141">Requirement</span></span> | <span data-ttu-id="06995-142">Значение</span><span class="sxs-lookup"><span data-stu-id="06995-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="06995-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06995-143">Minimum supported client</span></span><br/> | <span data-ttu-id="06995-144">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="06995-144">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="06995-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06995-145">Minimum supported server</span></span><br/> | <span data-ttu-id="06995-146">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="06995-146">None supported</span></span><br/>                                                            |
| <span data-ttu-id="06995-147">Header</span><span class="sxs-lookup"><span data-stu-id="06995-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="06995-148"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="06995-148"><dt>Sensors.h</dt></span></span> </dl> |



 

 




