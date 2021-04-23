---
description: Следующие квалификаторы используются поставщиком WDM в MOF-файлах драйвера устройства при извлечении данных из Внодес для создания экземпляров классов драйверов WDM.
ms.assetid: 11b0af59-979f-4908-baef-c9ec564b3cfd
ms.tgt_platform: multiple
title: Квалификаторы, относящиеся к поставщику WDM
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- NA
api_location: ''
ms.openlocfilehash: be2bc4593c19555dd5a851de89a1dc2e5db00596
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692574"
---
# <a name="qualifiers-specific-to-the-wdm-provider"></a><span data-ttu-id="1d515-103">Квалификаторы, относящиеся к поставщику WDM</span><span class="sxs-lookup"><span data-stu-id="1d515-103">Qualifiers Specific to the WDM Provider</span></span>

<span data-ttu-id="1d515-104">Следующие квалификаторы используются [поставщиком WDM](/windows/desktop/WmiCoreProv/wdm-provider) в MOF-файлах драйвера устройства при извлечении данных из внодес для создания экземпляров классов драйверов WDM.</span><span class="sxs-lookup"><span data-stu-id="1d515-104">The following qualifiers are used by the [WDM Provider](/windows/desktop/WmiCoreProv/wdm-provider) in device driver MOF files when they are extracting data from WNODEs to generate instances of WDM driver classes.</span></span>

<dt>

<span data-ttu-id="1d515-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**миссингвалуе**</span><span class="sxs-lookup"><span data-stu-id="1d515-105"><span id="MissingValue"></span><span id="missingvalue"></span><span id="MISSINGVALUE"></span>**MissingValue**</span></span>
</dt> <dd>

<span data-ttu-id="1d515-106">Тип данных: **DWORD, Array, Uint8, UInt16, UInt32, sint8, sint16 или Sint32.**</span><span class="sxs-lookup"><span data-stu-id="1d515-106">Data type: **DWORD, array, uint8, uint16, uint32, sint8, sint16, or sint32.**</span></span>

<span data-ttu-id="1d515-107">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="1d515-107">Applies to: properties</span></span>

<span data-ttu-id="1d515-108">Отсутствующее значение для этого свойства должно быть представлено **значением NULL** , а не 0 (нулем).</span><span class="sxs-lookup"><span data-stu-id="1d515-108">A missing value for this property should be represented by **NULL** rather than 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="1d515-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**вмидатаид**</span><span class="sxs-lookup"><span data-stu-id="1d515-109"><span id="WMIDataId"></span><span id="wmidataid"></span><span id="WMIDATAID"></span>**WMIDataId**</span></span>
</dt> <dd>

<span data-ttu-id="1d515-110">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d515-110">Data type: **uint32**</span></span>

<span data-ttu-id="1d515-111">Область применения: свойства</span><span class="sxs-lookup"><span data-stu-id="1d515-111">Applies to: properties</span></span>

<span data-ttu-id="1d515-112">Индекс в ВНОДЕ данных для свойства.</span><span class="sxs-lookup"><span data-stu-id="1d515-112">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="1d515-113">Поставщик WDM использует этот квалификатор, чтобы определить способ форматирования данных при извлечении данных из ВНОДЕ и создании классов WMI.</span><span class="sxs-lookup"><span data-stu-id="1d515-113">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="1d515-114">Начальное значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="1d515-114">The starting value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="1d515-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**вмиекспенсе**</span><span class="sxs-lookup"><span data-stu-id="1d515-115"><span id="WMIExpense"></span><span id="wmiexpense"></span><span id="WMIEXPENSE"></span>**WMIExpense**</span></span>
</dt> <dd>

<span data-ttu-id="1d515-116">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d515-116">Data type: **uint32**</span></span>

<span data-ttu-id="1d515-117">Область применения: классы</span><span class="sxs-lookup"><span data-stu-id="1d515-117">Applies to: classes</span></span>

<span data-ttu-id="1d515-118">Указание стоимости ресурса для доступа к блоку данных.</span><span class="sxs-lookup"><span data-stu-id="1d515-118">Indication of the resource cost to access the data block.</span></span> <span data-ttu-id="1d515-119">Например, сведения о геометрии диска не требуются для получения большого количества ресурсов, так как они доступны в расширении устройства.</span><span class="sxs-lookup"><span data-stu-id="1d515-119">For example, disk geometry information does not require a lot of resources to obtain because it is available in the device extension.</span></span> <span data-ttu-id="1d515-120">Производительность чтения и записи на диск больше интенсивна, поскольку требует дополнительной работы при каждой операции чтения/записи.</span><span class="sxs-lookup"><span data-stu-id="1d515-120">Disk read/write performance is more resource-intensive because it requires extra work on each read/write operation.</span></span> <span data-ttu-id="1d515-121">Таким образом, значение квалификатора **вмиекспенсе** больше для производительности чтения и записи на диск.</span><span class="sxs-lookup"><span data-stu-id="1d515-121">Therefore, the **WMIExpense** qualifier value is larger for disk read/write performance.</span></span>

</dd> <dt>

<span data-ttu-id="1d515-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**вмимесодид**</span><span class="sxs-lookup"><span data-stu-id="1d515-122"><span id="WMIMethodId"></span><span id="wmimethodid"></span><span id="WMIMETHODID"></span>**WMIMethodId**</span></span>
</dt> <dd>

<span data-ttu-id="1d515-123">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d515-123">Data type: **uint32**</span></span>

<span data-ttu-id="1d515-124">Область применения: методы</span><span class="sxs-lookup"><span data-stu-id="1d515-124">Applies to: methods</span></span>

<span data-ttu-id="1d515-125">Индекс в ВНОДЕ данных для свойства.</span><span class="sxs-lookup"><span data-stu-id="1d515-125">Index in the WNODE of the data for the property.</span></span> <span data-ttu-id="1d515-126">Поставщик WDM использует этот квалификатор, чтобы определить способ форматирования данных при извлечении данных из ВНОДЕ и создании классов WMI.</span><span class="sxs-lookup"><span data-stu-id="1d515-126">The WDM provider uses this qualifier to determine how the data is formatted while extracting data from the WNODE and generating WMI classes.</span></span> <span data-ttu-id="1d515-127">Начальное значение равно 1.</span><span class="sxs-lookup"><span data-stu-id="1d515-127">The starting value is 1.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d515-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1d515-128">Requirements</span></span>



| <span data-ttu-id="1d515-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1d515-129">Requirement</span></span> | <span data-ttu-id="1d515-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1d515-130">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="1d515-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1d515-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1d515-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d515-132">Windows Vista</span></span><br/>       |
| <span data-ttu-id="1d515-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1d515-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1d515-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d515-134">Windows Server 2008</span></span><br/> |



 

