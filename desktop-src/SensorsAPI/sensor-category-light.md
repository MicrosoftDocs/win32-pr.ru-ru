---
description: Категория " \_ Категория датчика" \_ содержит датчики, предоставляющие сведения о характеристиках освещения.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897030"
---
# <a name="sensor_category_light"></a><span data-ttu-id="b4797-103">\_Категория датчика \_ : светло</span><span class="sxs-lookup"><span data-stu-id="b4797-103">SENSOR\_CATEGORY\_LIGHT</span></span>

<span data-ttu-id="b4797-104">Категория " \_ Категория датчика" \_ содержит датчики, предоставляющие сведения о характеристиках освещения.</span><span class="sxs-lookup"><span data-stu-id="b4797-104">The SENSOR\_CATEGORY\_LIGHT category contains sensors that provide information about characteristics of light.</span></span>

<span data-ttu-id="b4797-105">**Типы датчиков, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="b4797-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="b4797-106">В эту категорию входят следующие типы датчиков, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="b4797-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="b4797-107">Тип датчика</span><span class="sxs-lookup"><span data-stu-id="b4797-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                     | <span data-ttu-id="b4797-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b4797-108">Description</span></span>                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <span data-ttu-id="b4797-109"><dt>**Датчик \_ Тип \_ окружающего \_ освещения**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span><span class="sxs-lookup"><span data-stu-id="b4797-109"><dt>**SENSOR\_TYPE\_AMBIENT\_LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt></span></span> </dl> | <span data-ttu-id="b4797-110">Датчики внешнего освещения.</span><span class="sxs-lookup"><span data-stu-id="b4797-110">Ambient light sensors.</span></span><br/> |



<span data-ttu-id="b4797-111">**Поля данных, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="b4797-111">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="b4797-112">Ключи свойств, определяемые платформой для этой категории, основываются на \_ \_ \_ идентификаторе источника данных датчика Light \_ :</span><span class="sxs-lookup"><span data-stu-id="b4797-112">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_LIGHT\_GUID:</span></span>

<span data-ttu-id="b4797-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span><span class="sxs-lookup"><span data-stu-id="b4797-113">{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}</span></span>

<span data-ttu-id="b4797-114">Эта категория включает следующие поля данных, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="b4797-114">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="b4797-115">Имя поля данных и идентификатор процесса</span><span class="sxs-lookup"><span data-stu-id="b4797-115">Data field name and PID</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="b4797-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b4797-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <span data-ttu-id="b4797-117"><dt> **\_ Тип данных \_ датчика \_ Light \_ чромаЦити**</dt> <dt>(PID = 4)</dt></span><span class="sxs-lookup"><span data-stu-id="b4797-117"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_CHROMACITY** </dt> <dt> (PID = 4) </dt></span></span> </dl>                     | <span data-ttu-id="b4797-118">**VT \_ вектор \| VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="b4797-118">**VT\_VECTOR\|VT\_UI1**</span></span><br/> <span data-ttu-id="b4797-119">Цветность в виде массива с подсчетом значений float.</span><span class="sxs-lookup"><span data-stu-id="b4797-119">Chromaticity as a counted array of float values.</span></span><br/> <span data-ttu-id="b4797-120">Данные для векторных типов всегда сериализуются как **VT \_ UI1** (массив неподписанных, 1-байтовых символов).</span><span class="sxs-lookup"><span data-stu-id="b4797-120">Data for vector types is always serialized as **VT\_UI1** (an array of unsigned, 1-byte characters).</span></span> <span data-ttu-id="b4797-121">Это поле данных фактически содержит каждое значение в виде реального значения в формате IEEE (**VT \_ R4**).</span><span class="sxs-lookup"><span data-stu-id="b4797-121">This data field actually contains each value as an IEEE 4-byte real value (**VT\_R4**).</span></span><br/> <span data-ttu-id="b4797-122">Дополнительные сведения о работе с массивами см. в разделе [Получение типов вектора](retrieving-vector-types.md).</span><span class="sxs-lookup"><span data-stu-id="b4797-122">For information about working with arrays, see [Retrieving Vector Types](retrieving-vector-types.md).</span></span><br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <span data-ttu-id="b4797-123"><dt>**Датчик \_ \_Тип данных \_ светлого \_ уровня \_ Lux**</dt> <dt> (PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="b4797-123"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_LEVEL\_LUX**</dt> <dt> (PID = 2) </dt></span></span> </dl>                            | <span data-ttu-id="b4797-124">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="b4797-124">**VT\_R4**</span></span><br/> <span data-ttu-id="b4797-125">Уровень иллуминанце в Lux.</span><span class="sxs-lookup"><span data-stu-id="b4797-125">Illuminance level, in lux.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <span data-ttu-id="b4797-126"><dt>**Датчик \_ Тип данных " \_ \_ светло- \_ температура \_ Кельвина**</dt> <dt> " (PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="b4797-126"><dt>**SENSOR\_DATA\_TYPE\_LIGHT\_TEMPERATURE\_KELVIN**</dt> <dt> (PID = 3) </dt></span></span> </dl> | <span data-ttu-id="b4797-127">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="b4797-127">**VT\_R4**</span></span><br/> <span data-ttu-id="b4797-128">Цветовая температура в градусах Кельвина.</span><span class="sxs-lookup"><span data-stu-id="b4797-128">Color temperature, in degrees Kelvin.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a><span data-ttu-id="b4797-129">Требования</span><span class="sxs-lookup"><span data-stu-id="b4797-129">Requirements</span></span>



| <span data-ttu-id="b4797-130">Требование</span><span class="sxs-lookup"><span data-stu-id="b4797-130">Requirement</span></span> | <span data-ttu-id="b4797-131">Значение</span><span class="sxs-lookup"><span data-stu-id="b4797-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b4797-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4797-132">Minimum supported client</span></span><br/> | <span data-ttu-id="b4797-133">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b4797-133">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b4797-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4797-134">Minimum supported server</span></span><br/> | <span data-ttu-id="b4797-135">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b4797-135">None supported</span></span><br/>                                                            |
| <span data-ttu-id="b4797-136">Header</span><span class="sxs-lookup"><span data-stu-id="b4797-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4797-137"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4797-137"><dt>Sensors.h</dt></span></span> </dl> |



 

 




