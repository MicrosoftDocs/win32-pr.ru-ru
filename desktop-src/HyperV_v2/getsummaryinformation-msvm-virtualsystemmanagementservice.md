---
description: Возвращает сводные данные о виртуальной машине.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Метод Жетсуммаринформатион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342802"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="db923-103">Метод Жетсуммаринформатион \_ класса Виртуалсистемманажементсервице мсвм</span><span class="sxs-lookup"><span data-stu-id="db923-103">GetSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="db923-104">Возвращает сводные данные о виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="db923-104">Returns virtual machine summary information.</span></span>

## <a name="syntax"></a><span data-ttu-id="db923-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db923-105">Syntax</span></span>


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="db923-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db923-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db923-107">*SettingData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db923-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db923-108">Тип: **CIM \_ виртуалсистемсеттингдата \[ \]**</span><span class="sxs-lookup"><span data-stu-id="db923-108">Type: **CIM\_VirtualSystemSettingData\[\]**</span></span>

<span data-ttu-id="db923-109">Массив экземпляров [**\_ виртуалсистемсеттингдата CIM**](/previous-versions//cc136954(v=vs.85)) , указывающих виртуальные машины или моментальные снимки, для которых необходимо получить сведения.</span><span class="sxs-lookup"><span data-stu-id="db923-109">An array of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) instances that specify the virtual machines or snapshots for which information is to be retrieved.</span></span> <span data-ttu-id="db923-110">Если этот параметр имеет **значение NULL**, то извлекаются сведения обо всех виртуальных машинах.</span><span class="sxs-lookup"><span data-stu-id="db923-110">If this parameter is **Null**, information for all virtual machines is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="db923-111">*Рекуестединформатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="db923-111">*RequestedInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db923-112">Тип: **UInt32 \[ \]**</span><span class="sxs-lookup"><span data-stu-id="db923-112">Type: **uint32\[\]**</span></span>

<span data-ttu-id="db923-113">Массив значений перечисления, соответствующих свойствам в классе [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) , которые указывают данные для получения для виртуальных машин и моментальных снимков, указанных в массиве *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="db923-113">An array of enumeration values, which correspond to the properties in the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class, that specify the data to retrieve for the virtual machines and snapshots specified in the *SettingData* array.</span></span>

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span data-ttu-id="db923-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Имя** (0)</span><span class="sxs-lookup"><span data-stu-id="db923-114"><span id="Name"></span><span id="name"></span><span id="NAME"></span>**Name** (0)</span></span>


</dt> <dd>

<span data-ttu-id="db923-115">Это соответствует свойству **Name** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-115">This corresponds to the **Name** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span data-ttu-id="db923-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Имя элемента** (1)</span><span class="sxs-lookup"><span data-stu-id="db923-116"><span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Element Name** (1)</span></span>


</dt> <dd>

<span data-ttu-id="db923-117">Это соответствует свойству **ElementName** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-117">This corresponds to the **ElementName** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span data-ttu-id="db923-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Время создания** (2)</span><span class="sxs-lookup"><span data-stu-id="db923-118"><span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Creation Time** (2)</span></span>


</dt> <dd>

<span data-ttu-id="db923-119">Это соответствует свойству **CreationTime** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-119">This corresponds to the **CreationTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span data-ttu-id="db923-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Примечания** (3)</span><span class="sxs-lookup"><span data-stu-id="db923-120"><span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notes** (3)</span></span>


</dt> <dd>

<span data-ttu-id="db923-121">Это соответствует свойству **Notes** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-121">This corresponds to the **Notes** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span data-ttu-id="db923-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Число процессоров** (4)</span><span class="sxs-lookup"><span data-stu-id="db923-122"><span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Number of Processors** (4)</span></span>


</dt> <dd>

<span data-ttu-id="db923-123">Это соответствует свойству **NumberOfProcessors** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-123">This corresponds to the **NumberOfProcessors** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span data-ttu-id="db923-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Маленький эскиз изображения (80x60)** (5)</span><span class="sxs-lookup"><span data-stu-id="db923-124"><span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Small Thumbnail Image (80x60)** (5)</span></span>


</dt> <dd>

<span data-ttu-id="db923-125">Это соответствует свойству **сумбнаилимаже** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-125">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="db923-126">Будет получен эскиз изображения с размерами 80 60.</span><span class="sxs-lookup"><span data-stu-id="db923-126">A thumbnail image with the dimensions of 80 60 will be retrieved.</span></span>

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span data-ttu-id="db923-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Средний эскиз изображения (160x120)** (6)</span><span class="sxs-lookup"><span data-stu-id="db923-127"><span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Medium Thumbnail Image (160x120)** (6)</span></span>


</dt> <dd>

<span data-ttu-id="db923-128">Это соответствует свойству **сумбнаилимаже** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-128">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="db923-129">Будет получен эскиз изображения с размерами 160 120.</span><span class="sxs-lookup"><span data-stu-id="db923-129">A thumbnail image with the dimensions of 160 120 will be retrieved.</span></span>

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span data-ttu-id="db923-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Изображение крупного эскиза (320x240)** (7)</span><span class="sxs-lookup"><span data-stu-id="db923-130"><span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Large Thumbnail Image (320x240)** (7)</span></span>


</dt> <dd>

<span data-ttu-id="db923-131">Это соответствует свойству **сумбнаилимаже** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-131">This corresponds to the **ThumbnailImage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span> <span data-ttu-id="db923-132">Будет получен эскиз изображения с размерами 320 240.</span><span class="sxs-lookup"><span data-stu-id="db923-132">A thumbnail image with the dimensions of 320 240 will be retrieved.</span></span>

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span data-ttu-id="db923-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**Аллокатедгпу** (8)</span><span class="sxs-lookup"><span data-stu-id="db923-133"><span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)</span></span>


</dt> <dd>

<span data-ttu-id="db923-134">Это соответствует свойству **аллокатедгпу** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-134">This corresponds to the **AllocatedGPU** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span data-ttu-id="db923-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**Виртуалсвитчнамес** (9)</span><span class="sxs-lookup"><span data-stu-id="db923-135"><span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span data-ttu-id="db923-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Версия** (10)</span><span class="sxs-lookup"><span data-stu-id="db923-136"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version** (10)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="db923-137">Добавлено в Windows 10 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="db923-137">Added in Windows 10 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span data-ttu-id="db923-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Экранированная** (11)</span><span class="sxs-lookup"><span data-stu-id="db923-138"><span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Shielded** (11)</span></span>


</dt> <dd>

> [!Note]  
> <span data-ttu-id="db923-139">Добавлено в Windows 10, версии 1703 и Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="db923-139">Added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span data-ttu-id="db923-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span><span class="sxs-lookup"><span data-stu-id="db923-140"><span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)</span></span>


</dt> <dd>

<span data-ttu-id="db923-141">Это соответствует свойству **EnabledState** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-141">This corresponds to the **EnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span data-ttu-id="db923-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**Процессорлоад** (101)</span><span class="sxs-lookup"><span data-stu-id="db923-142"><span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)</span></span>


</dt> <dd>

<span data-ttu-id="db923-143">Это соответствует свойству **процессорлоад** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-143">This corresponds to the **ProcessorLoad** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span data-ttu-id="db923-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**Процессорлоадхистори** (102)</span><span class="sxs-lookup"><span data-stu-id="db923-144"><span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)</span></span>


</dt> <dd>

<span data-ttu-id="db923-145">Это соответствует свойству **процессорлоадхистори** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-145">This corresponds to the **ProcessorLoadHistory** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span data-ttu-id="db923-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span><span class="sxs-lookup"><span data-stu-id="db923-146"><span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)</span></span>


</dt> <dd>

<span data-ttu-id="db923-147">Это соответствует свойству **MemoryUsage** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-147">This corresponds to the **MemoryUsage** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span data-ttu-id="db923-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Пульс** (104)</span><span class="sxs-lookup"><span data-stu-id="db923-148"><span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Heartbeat** (104)</span></span>


</dt> <dd>

<span data-ttu-id="db923-149">Это соответствует свойству **пульса** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-149">This corresponds to the **Heartbeat** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span data-ttu-id="db923-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Время бесперебойной работы** (105)</span><span class="sxs-lookup"><span data-stu-id="db923-150"><span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Uptime** (105)</span></span>


</dt> <dd>

<span data-ttu-id="db923-151">Это соответствует свойству **время работоспособности** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-151">This corresponds to the **UpTime** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span data-ttu-id="db923-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**Гуестоператингсистем** (106)</span><span class="sxs-lookup"><span data-stu-id="db923-152"><span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)</span></span>


</dt> <dd>

<span data-ttu-id="db923-153">Это соответствует свойству **гуестоператингсистем** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-153">This corresponds to the **GuestOperatingSystem** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span data-ttu-id="db923-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Моментальные снимки** (107)</span><span class="sxs-lookup"><span data-stu-id="db923-154"><span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Snapshots** (107)</span></span>


</dt> <dd>

<span data-ttu-id="db923-155">Это соответствует свойству **моментальных снимков** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-155">This corresponds to the **Snapshots** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span data-ttu-id="db923-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**Асинчронаустаскс** (108)</span><span class="sxs-lookup"><span data-stu-id="db923-156"><span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)</span></span>


</dt> <dd>

<span data-ttu-id="db923-157">Это соответствует свойству **асинчронаустаскс** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-157">This corresponds to the **AsynchronousTasks** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span data-ttu-id="db923-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span><span class="sxs-lookup"><span data-stu-id="db923-158"><span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)</span></span>


</dt> <dd>

<span data-ttu-id="db923-159">Это соответствует свойству **HealthState** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-159">This corresponds to the **HealthState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span data-ttu-id="db923-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span><span class="sxs-lookup"><span data-stu-id="db923-160"><span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)</span></span>


</dt> <dd>

<span data-ttu-id="db923-161">Это соответствует свойству **OperationalStatus** класса [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-161">This corresponds to the **OperationalStatus** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span data-ttu-id="db923-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**Статусдескриптионс** (111)</span><span class="sxs-lookup"><span data-stu-id="db923-162"><span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)</span></span>


</dt> <dd>

<span data-ttu-id="db923-163">Это соответствует свойству **статусдескриптионс** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-163">This corresponds to the **StatusDescriptions** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span data-ttu-id="db923-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**Меморяваилабле** (112)</span><span class="sxs-lookup"><span data-stu-id="db923-164"><span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)</span></span>


</dt> <dd>

<span data-ttu-id="db923-165">Это соответствует свойству **меморяваилабле** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-165">This corresponds to the **MemoryAvailable** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span data-ttu-id="db923-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**Аваилаблемеморибуффер** (113)</span><span class="sxs-lookup"><span data-stu-id="db923-166"><span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)</span></span>


</dt> <dd>

<span data-ttu-id="db923-167">Это соответствует свойству **аваилаблемеморибуффер** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-167">This corresponds to the **AvailableMemoryBuffer** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span data-ttu-id="db923-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Режим репликации** (114)</span><span class="sxs-lookup"><span data-stu-id="db923-168"><span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Replication Mode** (114)</span></span>


</dt> <dd>

<span data-ttu-id="db923-169">Это соответствует свойству **ReplicationMode** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-169">This corresponds to the **ReplicationMode** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span data-ttu-id="db923-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Состояние репликации** (115)</span><span class="sxs-lookup"><span data-stu-id="db923-170"><span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Replication State** (115)</span></span>


</dt> <dd>

<span data-ttu-id="db923-171">Это соответствует свойству **ReplicationState** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-171">This corresponds to the **ReplicationState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span data-ttu-id="db923-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Репликация системы реплики хеалстест** (116)</span><span class="sxs-lookup"><span data-stu-id="db923-172"><span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)</span></span>


</dt> <dd>

<span data-ttu-id="db923-173">Это соответствует свойству **репликатионхеалс** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-173">This corresponds to the **ReplicationHealth** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span data-ttu-id="db923-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Работоспособность приложения** (117)</span><span class="sxs-lookup"><span data-stu-id="db923-174"><span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Application Health** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span data-ttu-id="db923-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**Репликатионстатикс** (118)</span><span class="sxs-lookup"><span data-stu-id="db923-175"><span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)</span></span>


</dt> <dd>

<span data-ttu-id="db923-176">Это соответствует свойству **ReplicationState** класса [**\_ репликатионрелатионшип мсвм**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-176">This corresponds to the **ReplicationState** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="db923-177">Это массив для всех значений состояния репликации в первичной и расширенной связях.</span><span class="sxs-lookup"><span data-stu-id="db923-177">This is array for all replication state values across primary and extended relationship.</span></span> <span data-ttu-id="db923-178">0 значение индекса всегда используется для первичной связи, а если расширенная репликация включена, она возвращается в индекс 1.</span><span class="sxs-lookup"><span data-stu-id="db923-178">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span data-ttu-id="db923-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**Репликатионхеалсекс** (119)</span><span class="sxs-lookup"><span data-stu-id="db923-179"><span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)</span></span>


</dt> <dd>

<span data-ttu-id="db923-180">Это соответствует свойству **репликатионхеалс** класса [**\_ репликатионрелатионшип мсвм**](msvm-replicationrelationship.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-180">This corresponds to the **ReplicationHealth** property of the [**Msvm\_ReplicationRelationship**](msvm-replicationrelationship.md) class.</span></span> <span data-ttu-id="db923-181">Это массив для всех значений работоспособности репликации в первичной и расширенной связях.</span><span class="sxs-lookup"><span data-stu-id="db923-181">This is array for all replication health values across primary and extended relationship.</span></span> <span data-ttu-id="db923-182">0 значение индекса всегда используется для первичной связи, а если расширенная репликация включена, она возвращается в индекс 1.</span><span class="sxs-lookup"><span data-stu-id="db923-182">0 index value is always for primary relationship, and if extended replication is enabled, it is returned in index 1.</span></span>

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span data-ttu-id="db923-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**Свапфилесинусе** (120)</span><span class="sxs-lookup"><span data-stu-id="db923-183"><span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)</span></span>


</dt> <dd>

<span data-ttu-id="db923-184">Это соответствует свойству **свапфилесинусе** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-184">This corresponds to the **SwapFilesInUse** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="db923-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Интегратионсервицесверсионстате** (121)</span><span class="sxs-lookup"><span data-stu-id="db923-185"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span data-ttu-id="db923-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span><span class="sxs-lookup"><span data-stu-id="db923-186"><span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)</span></span>


</dt> <dd>

<span data-ttu-id="db923-187">Это соответствует свойству **Name** класса [**мсвм \_ репликатионпровидер**](msvm-replicationprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-187">This corresponds to the **Name** property of the [**Msvm\_ReplicationProvider**](msvm-replicationprovider.md) class.</span></span>

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span data-ttu-id="db923-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**Мемориспансфисикалнуманодес** (123)</span><span class="sxs-lookup"><span data-stu-id="db923-188"><span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span data-ttu-id="db923-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**Интегратионсервицесверсионстате** (132)</span><span class="sxs-lookup"><span data-stu-id="db923-189"><span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="db923-190">Это соответствует свойству **интегратионсервицесверсионстате** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-190">This corresponds to the **IntegrationServicesVersionState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span data-ttu-id="db923-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**Осеренабледстате** (132)</span><span class="sxs-lookup"><span data-stu-id="db923-191"><span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)</span></span>


</dt> <dd>

<span data-ttu-id="db923-192">Это соответствует свойству **осеренабледстате** класса [**\_ SummaryInformation мсвм**](msvm-summaryinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="db923-192">This corresponds to the **OtherEnabledState** property of the [**Msvm\_SummaryInformation**](msvm-summaryinformation.md) class.</span></span>

</dd> <dt>



 <span data-ttu-id="db923-193">(133)</span><span class="sxs-lookup"><span data-stu-id="db923-193">(133)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="db923-194">*SummaryInformation* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="db923-194">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db923-195">Тип: **[ **мсвм \_ суммаринформатионбасе**](msvm-summaryinformationbase.md)\[\]**</span><span class="sxs-lookup"><span data-stu-id="db923-195">Type: **[**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**</span></span>

<span data-ttu-id="db923-196">Массив экземпляров [**мсвм \_ суммаринформатионбасе**](msvm-summaryinformationbase.md) , содержащих запрашиваемые сведения для виртуальных машин и (или) моментальных снимков, указанных в массиве *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="db923-196">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformationbase.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *SettingData* array.</span></span> <span data-ttu-id="db923-197">Этот массив будет иметь то же количество элементов, что и массив *SettingData* .</span><span class="sxs-lookup"><span data-stu-id="db923-197">This array will have the same number of elements as the *SettingData* array.</span></span> <span data-ttu-id="db923-198">Каждая из этих записей будет содержать свойство **Name** , даже если это свойство не было запрошено.</span><span class="sxs-lookup"><span data-stu-id="db923-198">Each of these entries will contain the **Name** property, even if this property was not requested.</span></span> <span data-ttu-id="db923-199">Если виртуальную машину или моментальный снимок не удается найти или он недоступен, свойство **имя** соответствующей записи сводки будет пустым.</span><span class="sxs-lookup"><span data-stu-id="db923-199">If the virtual machine or snapshot cannot be found or is unavailable, the **Name** property of the corresponding summary information entry will be empty.</span></span>

<span data-ttu-id="db923-200">Свойства, не указанные в параметре *рекуестединформатион* , будут иметь значение **null** .</span><span class="sxs-lookup"><span data-stu-id="db923-200">Properties not specified in the *RequestedInformation* parameter will have a **Null** value.</span></span>

> [!Note]  
> <span data-ttu-id="db923-201">Тип данных, обновленный из Windows 10, версия 1703 из [**мсвм \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="db923-201">Datatype updated from in Windows 10, version 1703 from [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db923-202">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="db923-202">Return value</span></span>

<span data-ttu-id="db923-203">Тип: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="db923-203">Type: **uint32**</span></span>

<span data-ttu-id="db923-204">Этот метод возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="db923-204">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="db923-205">**Завершено без ошибок** (0)</span><span class="sxs-lookup"><span data-stu-id="db923-205">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="db923-206">**Параметры метода проверены — задание запущено** (4096)</span><span class="sxs-lookup"><span data-stu-id="db923-206">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="db923-207">**Сбой** (32768)</span><span class="sxs-lookup"><span data-stu-id="db923-207">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="db923-208">**Отказано в доступе** (32769)</span><span class="sxs-lookup"><span data-stu-id="db923-208">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="db923-209">**Не поддерживается** (32770)</span><span class="sxs-lookup"><span data-stu-id="db923-209">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="db923-210">**Состояние неизвестно** (32771)</span><span class="sxs-lookup"><span data-stu-id="db923-210">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="db923-211">**Время ожидания** (32772)</span><span class="sxs-lookup"><span data-stu-id="db923-211">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="db923-212">**Недопустимый параметр** (32773)</span><span class="sxs-lookup"><span data-stu-id="db923-212">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="db923-213">**Система используется** (32774)</span><span class="sxs-lookup"><span data-stu-id="db923-213">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="db923-214">**Недопустимое состояние для этой операции** (32775)</span><span class="sxs-lookup"><span data-stu-id="db923-214">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="db923-215">**Неверный тип данных** (32776)</span><span class="sxs-lookup"><span data-stu-id="db923-215">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="db923-216">**Система недоступна** (32777)</span><span class="sxs-lookup"><span data-stu-id="db923-216">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="db923-217">**Недостаточно памяти** (32778)</span><span class="sxs-lookup"><span data-stu-id="db923-217">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="db923-218">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db923-218">Remarks</span></span>

<span data-ttu-id="db923-219">Доступ к классу [**\_ виртуалсистемманажементсервице мсвм**](msvm-virtualsystemmanagementservice.md) может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="db923-219">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="db923-220">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="db923-220">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="db923-221">Примеры</span><span class="sxs-lookup"><span data-stu-id="db923-221">Examples</span></span>

<span data-ttu-id="db923-222">В следующем примере кода C# отображаются сводные данные.</span><span class="sxs-lookup"><span data-stu-id="db923-222">The following C# sample displays summary information.</span></span> <span data-ttu-id="db923-223">Служебные программы, на которые указывают ссылки, можно найти в [общих служебных программах для примеров виртуализации (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="db923-223">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="db923-224">Для правильной работы на сервере узла виртуальной машины должен быть запущен следующий код, который должен быть запущен с правами администратора.</span><span class="sxs-lookup"><span data-stu-id="db923-224">To function correctly, the following code must be run on the virtual machine host server, and must be run with Administrator privileges.</span></span>

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a><span data-ttu-id="db923-225">Требования</span><span class="sxs-lookup"><span data-stu-id="db923-225">Requirements</span></span>



| <span data-ttu-id="db923-226">Требование</span><span class="sxs-lookup"><span data-stu-id="db923-226">Requirement</span></span> | <span data-ttu-id="db923-227">Значение</span><span class="sxs-lookup"><span data-stu-id="db923-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="db923-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db923-228">Minimum supported client</span></span><br/> | <span data-ttu-id="db923-229">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="db923-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="db923-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db923-230">Minimum supported server</span></span><br/> | <span data-ttu-id="db923-231">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="db923-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="db923-232">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="db923-232">Namespace</span></span><br/>                | <span data-ttu-id="db923-233">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="db923-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="db923-234">MOF</span><span class="sxs-lookup"><span data-stu-id="db923-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db923-235"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="db923-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="db923-236">DLL</span><span class="sxs-lookup"><span data-stu-id="db923-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db923-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="db923-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="db923-238">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db923-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db923-239">**Мсвм \_ виртуалсистемманажементсервице**</span><span class="sxs-lookup"><span data-stu-id="db923-239">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="db923-240">[**\_ВИРТУАЛСИСТЕМСЕТТИНГДАТА CIM**](/previous-versions//cc136954(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="db923-240">[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="db923-241">**Мсвм \_ SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="db923-241">**Msvm\_SummaryInformation**</span></span>](msvm-summaryinformation.md)
</dt> </dl>

 

