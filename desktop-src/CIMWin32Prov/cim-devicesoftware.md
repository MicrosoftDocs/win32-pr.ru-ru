---
description: Отношение CIM \_ девицесофтваре определяет программное обеспечение, связанное с устройством, например драйверы, конфигурацию или программное обеспечение или встроенное по.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: Класс CIM_DeviceSoftware
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 467fa670e8bb3f7d6ee967e6dd422102a2026a57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539068"
---
# <a name="cim_devicesoftware-class"></a><span data-ttu-id="690f4-103">\_Класс CIM девицесофтваре</span><span class="sxs-lookup"><span data-stu-id="690f4-103">CIM\_DeviceSoftware class</span></span>

<span data-ttu-id="690f4-104">Отношение **CIM \_ девицесофтваре** определяет программное обеспечение, связанное с устройством, например драйверы, конфигурацию или программное обеспечение или встроенное по.</span><span class="sxs-lookup"><span data-stu-id="690f4-104">The **CIM\_DeviceSoftware** relationship identifies software that is associated with a device, such as drivers, configuration or application software, or firmware.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="690f4-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="690f4-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="690f4-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="690f4-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="690f4-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="690f4-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="690f4-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="690f4-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="690f4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="690f4-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a><span data-ttu-id="690f4-110">Члены</span><span class="sxs-lookup"><span data-stu-id="690f4-110">Members</span></span>

<span data-ttu-id="690f4-111">Класс **CIM \_ девицесофтваре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="690f4-111">The **CIM\_DeviceSoftware** class has these types of members:</span></span>

-   [<span data-ttu-id="690f4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="690f4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="690f4-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="690f4-113">Properties</span></span>

<span data-ttu-id="690f4-114">Класс **CIM \_ девицесофтваре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="690f4-114">The **CIM\_DeviceSoftware** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="690f4-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="690f4-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="690f4-116">Тип данных: **CIM \_ софтварилемент**</span><span class="sxs-lookup"><span data-stu-id="690f4-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="690f4-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="690f4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="690f4-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="690f4-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="690f4-119">[**\_ Софтварилемент CIM**](cim-softwareelement.md) , описывающий программный элемент.</span><span class="sxs-lookup"><span data-stu-id="690f4-119">A [**CIM\_SoftwareElement**](cim-softwareelement.md) that describes the software element.</span></span>

</dd> <dt>

<span data-ttu-id="690f4-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="690f4-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="690f4-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="690f4-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="690f4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="690f4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="690f4-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="690f4-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="690f4-124">[**Модель CIM \_**](cim-logicaldevice.md) , описывающая логическое устройство, которое требует или использует программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="690f4-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device that requires or uses the software.</span></span>

</dd> <dt>

<span data-ttu-id="690f4-125">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="690f4-125">**Purpose**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="690f4-126">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="690f4-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="690f4-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="690f4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="690f4-128">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ девицесофтваре**.**Пурпоседескриптион**")</span><span class="sxs-lookup"><span data-stu-id="690f4-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**PurposeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="690f4-129">Роль, которую программное обеспечение принимает в отношении связанного с ним устройства.</span><span class="sxs-lookup"><span data-stu-id="690f4-129">Role that the software takes regarding its associated device.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="690f4-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="690f4-130"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-131">Неизвестно.</span><span class="sxs-lookup"><span data-stu-id="690f4-131">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="690f4-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="690f4-132"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-133">Другое</span><span class="sxs-lookup"><span data-stu-id="690f4-133">Other.</span></span>

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span data-ttu-id="690f4-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Драйвер** (2)</span><span class="sxs-lookup"><span data-stu-id="690f4-134"><span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Driver** (2)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-135">Аудиодрайвера.</span><span class="sxs-lookup"><span data-stu-id="690f4-135">Driver.</span></span>

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span data-ttu-id="690f4-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Программное обеспечение для настройки** (3)</span><span class="sxs-lookup"><span data-stu-id="690f4-136"><span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Configuration Software** (3)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-137">Программное обеспечение для настройки.</span><span class="sxs-lookup"><span data-stu-id="690f4-137">Configuration software.</span></span>

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span data-ttu-id="690f4-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Программное обеспечение приложения** (4)</span><span class="sxs-lookup"><span data-stu-id="690f4-138"><span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Application Software** (4)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-139">Программное обеспечение приложения.</span><span class="sxs-lookup"><span data-stu-id="690f4-139">Application software.</span></span>

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span data-ttu-id="690f4-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Инструментирование** (5)</span><span class="sxs-lookup"><span data-stu-id="690f4-140"><span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentation** (5)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-141">Инструментирование.</span><span class="sxs-lookup"><span data-stu-id="690f4-141">Instrumentation.</span></span>

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span data-ttu-id="690f4-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Встроенное по** (6)</span><span class="sxs-lookup"><span data-stu-id="690f4-142"><span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-143">Встроенного по.</span><span class="sxs-lookup"><span data-stu-id="690f4-143">Firmware.</span></span>

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span data-ttu-id="690f4-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span><span class="sxs-lookup"><span data-stu-id="690f4-144"><span id="BIOS"></span><span id="bios"></span>**BIOS** (7)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-145">Включен.</span><span class="sxs-lookup"><span data-stu-id="690f4-145">BIOS.</span></span>

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span data-ttu-id="690f4-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Загрузочный диск** (8)</span><span class="sxs-lookup"><span data-stu-id="690f4-146"><span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**Boot ROM** (8)</span></span>


</dt> <dd>

<span data-ttu-id="690f4-147">Загрузочный диск.</span><span class="sxs-lookup"><span data-stu-id="690f4-147">Boot ROM.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="690f4-148">**пурпоседескриптион**</span><span class="sxs-lookup"><span data-stu-id="690f4-148">**PurposeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="690f4-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="690f4-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="690f4-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="690f4-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="690f4-151">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ девицесофтваре**.**Цель**")</span><span class="sxs-lookup"><span data-stu-id="690f4-151">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_DeviceSoftware**.**Purpose**")</span></span>
</dt> </dl>

<span data-ttu-id="690f4-152">Произвольная строка, которая предоставляет дополнительные сведения для свойства **цели** , например "программное обеспечение приложения".</span><span class="sxs-lookup"><span data-stu-id="690f4-152">Free-form string that provides more information for the **Purpose** property, for example, "Application Software".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="690f4-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="690f4-153">Remarks</span></span>

<span data-ttu-id="690f4-154">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="690f4-154">WMI does not implement this class.</span></span>

<span data-ttu-id="690f4-155">Класс **CIM \_ девицесофтваре** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="690f4-155">The **CIM\_DeviceSoftware** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="690f4-156">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="690f4-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="690f4-157">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="690f4-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="690f4-158">Требования</span><span class="sxs-lookup"><span data-stu-id="690f4-158">Requirements</span></span>



| <span data-ttu-id="690f4-159">Требование</span><span class="sxs-lookup"><span data-stu-id="690f4-159">Requirement</span></span> | <span data-ttu-id="690f4-160">Значение</span><span class="sxs-lookup"><span data-stu-id="690f4-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="690f4-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="690f4-161">Minimum supported client</span></span><br/> | <span data-ttu-id="690f4-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="690f4-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="690f4-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="690f4-163">Minimum supported server</span></span><br/> | <span data-ttu-id="690f4-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="690f4-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="690f4-165">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="690f4-165">Namespace</span></span><br/>                | <span data-ttu-id="690f4-166">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="690f4-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="690f4-167">MOF</span><span class="sxs-lookup"><span data-stu-id="690f4-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="690f4-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="690f4-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="690f4-169">DLL</span><span class="sxs-lookup"><span data-stu-id="690f4-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="690f4-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="690f4-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="690f4-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="690f4-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="690f4-172">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="690f4-172">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

