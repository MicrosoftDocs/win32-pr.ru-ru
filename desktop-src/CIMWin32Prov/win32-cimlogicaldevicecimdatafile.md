---
description: '\_Класс WMI взаимосвязей Win32 ЦимлогикалдевицеЦимдатафиле связывает логические устройства и файлы данных, указывая файлы драйверов, используемые устройством. Этот класс используется для определения того, какие драйверы устройств использует устройство.'
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Класс Win32_CIMLogicalDeviceCIMDataFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539152"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a><span data-ttu-id="d31f2-104">\_Класс Win32 ЦимлогикалдевицеЦимдатафиле</span><span class="sxs-lookup"><span data-stu-id="d31f2-104">Win32\_CIMLogicalDeviceCIMDataFile class</span></span>

<span data-ttu-id="d31f2-105">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ ЦимлогикалдевицеЦимдатафиле** связывает логические устройства и файлы данных, указывая файлы драйверов, используемые устройством.</span><span class="sxs-lookup"><span data-stu-id="d31f2-105">The **Win32\_CIMLogicalDeviceCIMDataFile** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates logical devices and data files, indicating the driver files used by the device.</span></span> <span data-ttu-id="d31f2-106">Этот класс используется для определения того, какие драйверы устройств использует устройство.</span><span class="sxs-lookup"><span data-stu-id="d31f2-106">This class is used to discover which device drivers a device uses.</span></span>

<span data-ttu-id="d31f2-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d31f2-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="d31f2-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d31f2-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d31f2-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d31f2-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="d31f2-110">Члены</span><span class="sxs-lookup"><span data-stu-id="d31f2-110">Members</span></span>

<span data-ttu-id="d31f2-111">Класс **Win32 \_ ЦимлогикалдевицеЦимдатафиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d31f2-111">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these types of members:</span></span>

-   [<span data-ttu-id="d31f2-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d31f2-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d31f2-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="d31f2-113">Properties</span></span>

<span data-ttu-id="d31f2-114">Класс **Win32 \_ ЦимлогикалдевицеЦимдатафиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d31f2-114">The **Win32\_CIMLogicalDeviceCIMDataFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d31f2-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d31f2-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31f2-116">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="d31f2-116">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d31f2-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-118">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="d31f2-118">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="d31f2-119">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , представляющее свойства логического устройства, которое используется файлом данных.</span><span class="sxs-lookup"><span data-stu-id="d31f2-119">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is being used by the data file.</span></span>

</dd> <dt>

<span data-ttu-id="d31f2-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="d31f2-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31f2-121">Тип данных: **CIM \_ File**</span><span class="sxs-lookup"><span data-stu-id="d31f2-121">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d31f2-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-123">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ File")</span><span class="sxs-lookup"><span data-stu-id="d31f2-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_DataFile")</span></span>
</dt> </dl>

<span data-ttu-id="d31f2-124">[**CIM- \_ файл**](cim-datafile.md) , представляющий свойства файла данных, назначенного логическому устройству.</span><span class="sxs-lookup"><span data-stu-id="d31f2-124">A [**CIM\_DataFile**](cim-datafile.md) that represents the properties of the data file assigned to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="d31f2-125">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="d31f2-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31f2-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d31f2-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d31f2-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-128">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="d31f2-128">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="d31f2-129">Роль, с которой начнется файл данных, относительно связанного с ним логического устройства.</span><span class="sxs-lookup"><span data-stu-id="d31f2-129">Role that the data file plays with regard to its associated logical device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d31f2-130">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="d31f2-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d31f2-131">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="d31f2-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="d31f2-132">**Драйвер** (2)</span><span class="sxs-lookup"><span data-stu-id="d31f2-132">**Driver** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="d31f2-133">**Программное обеспечение для настройки** (3)</span><span class="sxs-lookup"><span data-stu-id="d31f2-133">**Configuration Software** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="d31f2-134">**Программное обеспечение приложения** (4)</span><span class="sxs-lookup"><span data-stu-id="d31f2-134">**Application Software** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="d31f2-135">**Инструментирование** (5)</span><span class="sxs-lookup"><span data-stu-id="d31f2-135">**Instrumentation** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="d31f2-136">**Встроенное по** (6)</span><span class="sxs-lookup"><span data-stu-id="d31f2-136">**Firmware** (6)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d31f2-137">**пурпоседескриптион**</span><span class="sxs-lookup"><span data-stu-id="d31f2-137">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d31f2-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d31f2-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d31f2-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d31f2-140">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span><span class="sxs-lookup"><span data-stu-id="d31f2-140">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")</span></span>
</dt> </dl>

<span data-ttu-id="d31f2-141">Расширяет значение свойства **цели** этого класса.</span><span class="sxs-lookup"><span data-stu-id="d31f2-141">Extends the value of the **Purpose** property of this class.</span></span>

<span data-ttu-id="d31f2-142">Пример: "драйвер гибкого диска"</span><span class="sxs-lookup"><span data-stu-id="d31f2-142">Example: "Floppy Disk Driver"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d31f2-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d31f2-143">Remarks</span></span>

<span data-ttu-id="d31f2-144">Класс **Win32 \_ ЦимлогикалдевицеЦимдатафиле** является производным от [**\_ зависимости CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="d31f2-144">The **Win32\_CIMLogicalDeviceCIMDataFile** class is derived from [**CIM\_Dependency**](cim-logicaldevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d31f2-145">Требования</span><span class="sxs-lookup"><span data-stu-id="d31f2-145">Requirements</span></span>



| <span data-ttu-id="d31f2-146">Требование</span><span class="sxs-lookup"><span data-stu-id="d31f2-146">Requirement</span></span> | <span data-ttu-id="d31f2-147">Значение</span><span class="sxs-lookup"><span data-stu-id="d31f2-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d31f2-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d31f2-148">Minimum supported client</span></span><br/> | <span data-ttu-id="d31f2-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d31f2-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d31f2-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d31f2-150">Minimum supported server</span></span><br/> | <span data-ttu-id="d31f2-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d31f2-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d31f2-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d31f2-152">Namespace</span></span><br/>                | <span data-ttu-id="d31f2-153">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d31f2-153">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d31f2-154">MOF</span><span class="sxs-lookup"><span data-stu-id="d31f2-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d31f2-155"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d31f2-155"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d31f2-156">DLL</span><span class="sxs-lookup"><span data-stu-id="d31f2-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d31f2-157"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d31f2-157"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d31f2-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d31f2-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31f2-159">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="d31f2-159">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

<span data-ttu-id="d31f2-160">[Классы операционной системы](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d31f2-160">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

