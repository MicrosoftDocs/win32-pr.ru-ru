---
description: '\_ \_ Категория биометрических МЕТРИК категории датчика содержит датчики, предоставляющие сведения о живых существ.'
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144395"
---
# <a name="sensor_category_biometric"></a><span data-ttu-id="07ae4-103">\_БИОметрическая Категория датчика \_</span><span class="sxs-lookup"><span data-stu-id="07ae4-103">SENSOR\_CATEGORY\_BIOMETRIC</span></span>

<span data-ttu-id="07ae4-104">\_ \_ Категория биометрических МЕТРИК категории датчика содержит датчики, предоставляющие сведения о живых существ.</span><span class="sxs-lookup"><span data-stu-id="07ae4-104">The SENSOR\_CATEGORY\_BIOMETRIC category contains sensors that provide information about living beings.</span></span>

<span data-ttu-id="07ae4-105">**Типы датчиков, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="07ae4-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="07ae4-106">В эту категорию входят следующие типы датчиков, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="07ae4-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="07ae4-107">Тип датчика</span><span class="sxs-lookup"><span data-stu-id="07ae4-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="07ae4-108">Описание</span><span class="sxs-lookup"><span data-stu-id="07ae4-108">Description</span></span>                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <span data-ttu-id="07ae4-109"><dt>**Датчик \_ Введите \_ \_ присутствие человека**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span><span class="sxs-lookup"><span data-stu-id="07ae4-109"><dt>**SENSOR\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt></span></span> </dl>    | <span data-ttu-id="07ae4-110">Датчики, которые обнаруживают присутствие человека.</span><span class="sxs-lookup"><span data-stu-id="07ae4-110">Sensors that detect human presence.</span></span><br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <span data-ttu-id="07ae4-111"><dt>**Датчик \_ Введите \_ \_ близость человека**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span><span class="sxs-lookup"><span data-stu-id="07ae4-111"><dt>**SENSOR\_TYPE\_HUMAN\_PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt></span></span> </dl> | <span data-ttu-id="07ae4-112">Датчики, которые определяют близость людей.</span><span class="sxs-lookup"><span data-stu-id="07ae4-112">Sensors that detect human proximity.</span></span><br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <span data-ttu-id="07ae4-113"><dt>**Датчик \_ Введите \_ сенсорный**</dt> ввод <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span><span class="sxs-lookup"><span data-stu-id="07ae4-113"><dt>**SENSOR\_TYPE\_TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt></span></span> </dl>                                | <span data-ttu-id="07ae4-114">Сенсорные датчики.</span><span class="sxs-lookup"><span data-stu-id="07ae4-114">Touch sensors.</span></span><br/>                       |



<span data-ttu-id="07ae4-115">**Поля данных, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="07ae4-115">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="07ae4-116">Ключи свойств, определяемые платформой для этой категории, основываются на \_ \_ \_ идентификаторе GUID БИОметрической метрики для типа данных датчика \_ :</span><span class="sxs-lookup"><span data-stu-id="07ae4-116">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_BIOMETRIC\_GUID:</span></span>

<span data-ttu-id="07ae4-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span><span class="sxs-lookup"><span data-stu-id="07ae4-117">{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}</span></span>

<span data-ttu-id="07ae4-118">Эта категория включает следующие поля данных, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="07ae4-118">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="07ae4-119">Имя поля данных и идентификатор процесса</span><span class="sxs-lookup"><span data-stu-id="07ae4-119">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                         | <span data-ttu-id="07ae4-120">Описание</span><span class="sxs-lookup"><span data-stu-id="07ae4-120">Description</span></span>                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <span data-ttu-id="07ae4-121"><dt>**Датчик \_ \_Тип данных \_ " \_ присутствие**</dt> <dt>(PID = 2)</dt> "</span><span class="sxs-lookup"><span data-stu-id="07ae4-121"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PRESENCE**</dt> <dt>(PID = 2) </dt></span></span> </dl>                          | <span data-ttu-id="07ae4-122">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="07ae4-122">**VT\_BOOL**</span></span><br/> <span data-ttu-id="07ae4-123">**Имеет значение true** , когда человек использует компьютер.</span><span class="sxs-lookup"><span data-stu-id="07ae4-123">**TRUE** when a human is using the computer.</span></span><br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <span data-ttu-id="07ae4-124"><dt>**Датчик \_ \_Тип данных \_ \_ \_ счетчики близости к человеку**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="07ae4-124"><dt>**SENSOR\_DATA\_TYPE\_HUMAN\_PROXIMITY\_METERS**</dt> <dt>(PID = 3) </dt></span></span> </dl> | <span data-ttu-id="07ae4-125">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="07ae4-125">**VT\_R4**</span></span><br/> <span data-ttu-id="07ae4-126">Расстояние между человеком и компьютером в метрах.</span><span class="sxs-lookup"><span data-stu-id="07ae4-126">Distance between a human and the computer, in meters.</span></span><br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <span data-ttu-id="07ae4-127"><dt>**Датчик \_ \_ \_ \_ Состояние касания типа данных**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="07ae4-127"><dt>**SENSOR\_DATA\_TYPE\_TOUCH\_STATE**</dt> <dt>(PID = 4) </dt></span></span> </dl>                                   | <span data-ttu-id="07ae4-128">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="07ae4-128">**VT\_BOOL**</span></span><br/> <span data-ttu-id="07ae4-129">**Значение true** , если сенсорный датчик затрагивается; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="07ae4-129">**TRUE** when the touch sensor is being touched; otherwise, **FALSE**.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="07ae4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="07ae4-130">Requirements</span></span>



| <span data-ttu-id="07ae4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="07ae4-131">Requirement</span></span> | <span data-ttu-id="07ae4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="07ae4-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="07ae4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07ae4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="07ae4-134">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="07ae4-134">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="07ae4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07ae4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="07ae4-136">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="07ae4-136">None supported</span></span><br/>                                                            |
| <span data-ttu-id="07ae4-137">Header</span><span class="sxs-lookup"><span data-stu-id="07ae4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="07ae4-138"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="07ae4-138"><dt>Sensors.h</dt></span></span> </dl> |



 

 




