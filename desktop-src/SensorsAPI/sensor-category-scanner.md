---
description: '\_ \_ Категория сканер категории датчика содержит датчики, предоставляющие сведения, получаемые при сканировании.'
ms.assetid: 98a772c9-2a21-489f-ad8d-3b772b7ff892
title: SENSOR_CATEGORY_SCANNER (sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b38fdb3358ff3ce2ae96ce901972cc6842a0d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991007"
---
# <a name="sensor_category_scanner"></a><span data-ttu-id="fcaed-103">\_сканер категории \_ датчика</span><span class="sxs-lookup"><span data-stu-id="fcaed-103">SENSOR\_CATEGORY\_SCANNER</span></span>

<span data-ttu-id="fcaed-104">\_ \_ Категория сканер категории датчика содержит датчики, предоставляющие сведения, получаемые при сканировании.</span><span class="sxs-lookup"><span data-stu-id="fcaed-104">The SENSOR\_CATEGORY\_SCANNER category contains sensors that provide information that is obtained by scanning.</span></span>

<span data-ttu-id="fcaed-105">**Типы датчиков, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="fcaed-105">**Platform-Defined Sensor Types**</span></span>

<span data-ttu-id="fcaed-106">В эту категорию входят следующие типы датчиков, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="fcaed-106">This category includes the following platform-defined sensor types.</span></span>



| <span data-ttu-id="fcaed-107">Тип датчика</span><span class="sxs-lookup"><span data-stu-id="fcaed-107">Sensor type</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="fcaed-108">Описание</span><span class="sxs-lookup"><span data-stu-id="fcaed-108">Description</span></span>                                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| <span id="SENSOR_TYPE_BARCODE_SCANNER"></span><span id="sensor_type_barcode_scanner"></span><dl> <span data-ttu-id="fcaed-109"><dt>**Датчик \_ Тип \_ \_ сканера штрихкодов**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span><span class="sxs-lookup"><span data-stu-id="fcaed-109"><dt>**SENSOR\_TYPE\_BARCODE\_SCANNER**</dt> <dt>{990B3D8F-85BB-45FF-914D-998C04F372DF}</dt></span></span> </dl> | <span data-ttu-id="fcaed-110">Датчики, использующие оптическое сканирование для чтения штрихкодов.</span><span class="sxs-lookup"><span data-stu-id="fcaed-110">Sensors that use optical scanning to read bar codes.</span></span><br/> |
| <span id="SENSOR_TYPE_RFID_SCANNER"></span><span id="sensor_type_rfid_scanner"></span><dl> <span data-ttu-id="fcaed-111"><dt>**Датчик \_ Введите \_ \_ Сканер RFID**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span><span class="sxs-lookup"><span data-stu-id="fcaed-111"><dt>**SENSOR\_TYPE\_RFID\_SCANNER**</dt> <dt>{44328EF5-02DD-4E8D-AD5D-9249832B2ECA}</dt></span></span> </dl>          | <span data-ttu-id="fcaed-112">Датчики проверки кода с радиочастотой.</span><span class="sxs-lookup"><span data-stu-id="fcaed-112">Radio-frequency ID scanning sensors.</span></span><br/>                 |



<span data-ttu-id="fcaed-113">**Поля данных, определяемые платформой**</span><span class="sxs-lookup"><span data-stu-id="fcaed-113">**Platform-Defined Data Fields**</span></span>

<span data-ttu-id="fcaed-114">Ключи свойств, определяемые платформой для этой категории, основываются на \_ \_ \_ GUID сканера типа данных датчика \_ :</span><span class="sxs-lookup"><span data-stu-id="fcaed-114">Platform-defined property keys for this category are based on SENSOR\_DATA\_TYPE\_SCANNER\_GUID:</span></span>

<span data-ttu-id="fcaed-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span><span class="sxs-lookup"><span data-stu-id="fcaed-115">{D7A59A3C-3421-44AB-8D3A-9DE8AB6C4CAE}</span></span>

<span data-ttu-id="fcaed-116">Эта категория включает следующие поля данных, определяемые платформой.</span><span class="sxs-lookup"><span data-stu-id="fcaed-116">This category includes the following platform-defined data fields.</span></span>



| <span data-ttu-id="fcaed-117">Имя поля данных и идентификатор процесса</span><span class="sxs-lookup"><span data-stu-id="fcaed-117">Data field name and PID</span></span>                                                                                                                                                                                                                                                                     | <span data-ttu-id="fcaed-118">Описание</span><span class="sxs-lookup"><span data-stu-id="fcaed-118">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_RFID_TAG_40_BIT"></span><span id="sensor_data_type_rfid_tag_40_bit"></span><dl> <span data-ttu-id="fcaed-119"><dt>**Датчик \_ \_Тип данных \_ тег технологии RFID \_ \_ 40 \_ bit**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="fcaed-119"><dt>**SENSOR\_DATA\_TYPE\_RFID\_TAG\_40\_BIT**</dt> <dt>(PID = 2) </dt></span></span> </dl> | <span data-ttu-id="fcaed-120">**VT \_ UI8**</span><span class="sxs-lookup"><span data-stu-id="fcaed-120">**VT\_UI8**</span></span><br/> <span data-ttu-id="fcaed-121">40-разрядное значение тега идентификатора радиочастоты.</span><span class="sxs-lookup"><span data-stu-id="fcaed-121">40-bit radio frequency ID tag value.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="fcaed-122">Требования</span><span class="sxs-lookup"><span data-stu-id="fcaed-122">Requirements</span></span>



| <span data-ttu-id="fcaed-123">Требование</span><span class="sxs-lookup"><span data-stu-id="fcaed-123">Requirement</span></span> | <span data-ttu-id="fcaed-124">Значение</span><span class="sxs-lookup"><span data-stu-id="fcaed-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fcaed-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcaed-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fcaed-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="fcaed-126">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fcaed-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcaed-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fcaed-128">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="fcaed-128">None supported</span></span><br/>                                                            |
| <span data-ttu-id="fcaed-129">Header</span><span class="sxs-lookup"><span data-stu-id="fcaed-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="fcaed-130"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="fcaed-130"><dt>Sensors.h</dt></span></span> </dl> |



 

 




