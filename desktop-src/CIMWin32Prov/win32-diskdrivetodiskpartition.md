---
description: '\_Класс WMI взаимосвязей Win32 дискдриветодискпартитион связывает диск и раздел, существующий на нем.'
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Класс Win32_DiskDriveToDiskPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655990"
---
# <a name="win32_diskdrivetodiskpartition-class"></a><span data-ttu-id="f177d-103">\_Класс Win32 дискдриветодискпартитион</span><span class="sxs-lookup"><span data-stu-id="f177d-103">Win32\_DiskDriveToDiskPartition class</span></span>

<span data-ttu-id="f177d-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ дискдриветодискпартитион** связывает диск и раздел, существующий на нем.</span><span class="sxs-lookup"><span data-stu-id="f177d-104">The **Win32\_DiskDriveToDiskPartition** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a disk drive and a partition existing on it.</span></span>

<span data-ttu-id="f177d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="f177d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="f177d-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f177d-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f177d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f177d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f177d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f177d-108">Members</span></span>

<span data-ttu-id="f177d-109">Класс **Win32 \_ дискдриветодискпартитион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f177d-109">The **Win32\_DiskDriveToDiskPartition** class has these types of members:</span></span>

-   [<span data-ttu-id="f177d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="f177d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f177d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="f177d-111">Properties</span></span>

<span data-ttu-id="f177d-112">Класс **Win32 \_ дискдриветодискпартитион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f177d-112">The **Win32\_DiskDriveToDiskPartition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f177d-113">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="f177d-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f177d-114">Тип данных: **Win32 \_ дискдриве**</span><span class="sxs-lookup"><span data-stu-id="f177d-114">Data type: **Win32\_DiskDrive**</span></span>
</dt> <dt>

<span data-ttu-id="f177d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f177d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f177d-116">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дискдриве")</span><span class="sxs-lookup"><span data-stu-id="f177d-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskDrive")</span></span>
</dt> </dl>

<span data-ttu-id="f177d-117">Ссылка на экземпляр, представляющий свойства диска, на котором находится секция.</span><span class="sxs-lookup"><span data-stu-id="f177d-117">Reference to the instance representing the properties of the disk drive where the partition exists.</span></span>

</dd> <dt>

<span data-ttu-id="f177d-118">**Него**</span><span class="sxs-lookup"><span data-stu-id="f177d-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f177d-119">Тип данных: **Win32 \_ дискпартитион**</span><span class="sxs-lookup"><span data-stu-id="f177d-119">Data type: **Win32\_DiskPartition**</span></span>
</dt> <dt>

<span data-ttu-id="f177d-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f177d-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f177d-121">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ дискпартитион")</span><span class="sxs-lookup"><span data-stu-id="f177d-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_DiskPartition")</span></span>
</dt> </dl>

<span data-ttu-id="f177d-122">Ссылка на экземпляр, представляющий раздел диска, расположенный на диске.</span><span class="sxs-lookup"><span data-stu-id="f177d-122">Reference to the instance representing the disk partition residing on the disk drive.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f177d-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f177d-123">Remarks</span></span>

<span data-ttu-id="f177d-124">Класс **Win32 \_ дискдриветодискпартитион** является производным от [**CIM \_ медиапресент**](cim-mediapresent.md).</span><span class="sxs-lookup"><span data-stu-id="f177d-124">The **Win32\_DiskDriveToDiskPartition** class is derived from [**CIM\_MediaPresent**](cim-mediapresent.md).</span></span>

<span data-ttu-id="f177d-125">Сведения об использовании этого класса см. в статьях [Использование PowerShell для сопоставления дисков и разделов](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) и [как можно сопоставить логические диски и физические диски?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) статьи блога.</span><span class="sxs-lookup"><span data-stu-id="f177d-125">For a discussion on how to use this class, see the [Use PowerShell to Map Disk Drives and Partitions](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) and the [How Can I Correlate Logical Drives and Physical Disks?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) blog articles.</span></span>

## <a name="examples"></a><span data-ttu-id="f177d-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="f177d-126">Examples</span></span>

<span data-ttu-id="f177d-127">Пример [использования PowerShell для сбора сведений о диске, разделе или точке подключения](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell использует **Win32 \_ дискдриветодискпартитион** для получения сведений о локальных дисках и разделах и точках подключения.</span><span class="sxs-lookup"><span data-stu-id="f177d-127">The [Use Powershell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) PowerShell sample uses **Win32\_DiskDriveToDiskPartition** to return information about local disks/partitions and mount points.</span></span>

## <a name="requirements"></a><span data-ttu-id="f177d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="f177d-128">Requirements</span></span>



| <span data-ttu-id="f177d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="f177d-129">Requirement</span></span> | <span data-ttu-id="f177d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="f177d-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f177d-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f177d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="f177d-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f177d-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f177d-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f177d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="f177d-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f177d-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f177d-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f177d-135">Namespace</span></span><br/>                | <span data-ttu-id="f177d-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f177d-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f177d-137">MOF</span><span class="sxs-lookup"><span data-stu-id="f177d-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f177d-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f177d-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f177d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="f177d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f177d-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f177d-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f177d-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f177d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f177d-142">**\_МЕДИАПРЕСЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="f177d-142">**CIM\_MediaPresent**</span></span>](cim-mediapresent.md)
</dt> <dt>

<span data-ttu-id="f177d-143">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f177d-143">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f177d-144">Задачи WMI: диски и файловые системы</span><span class="sxs-lookup"><span data-stu-id="f177d-144">WMI Tasks: Disks and File Systems</span></span>](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

