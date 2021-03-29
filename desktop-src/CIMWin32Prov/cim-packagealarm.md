---
description: '\_Ассоциация ПАККАЖЕАЛАРМ CIM представляет связь, в которой устанавливается сигнальное устройство в составе пакета. Установка указывает на проблемы с окружением пакета&\# 8212, состояние безопасности или его общую работоспособность.'
ms.assetid: 4911502a-de9c-46b4-91f6-a042c69fd052
ms.tgt_platform: multiple
title: Класс CIM_PackageAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageAlarm
- CIM_PackageAlarm.Dependent
- CIM_PackageAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 29aae3a2c1093e026356ea7a096f8b673673f67d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141082"
---
# <a name="cim_packagealarm-class"></a><span data-ttu-id="733d8-104">\_Класс CIM паккажеаларм</span><span class="sxs-lookup"><span data-stu-id="733d8-104">CIM\_PackageAlarm class</span></span>

<span data-ttu-id="733d8-105">Ассоциация [**\_ паккажеаларм CIM**](/windows/desktop/SecCrypto/extendedproperties-newenum) представляет связь, в которой устанавливается сигнальное устройство в составе пакета.</span><span class="sxs-lookup"><span data-stu-id="733d8-105">The [**CIM\_PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) association represents the relationship in which an alarm device is installed as part of a package.</span></span> <span data-ttu-id="733d8-106">Установка указывает на проблемы с состоянием безопасности среды пакета или его общей работоспособностью.</span><span class="sxs-lookup"><span data-stu-id="733d8-106">The installation indicates issues with the package's environment its security state or its overall health.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="733d8-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="733d8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="733d8-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="733d8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="733d8-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="733d8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="733d8-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="733d8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="733d8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="733d8-111">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B90-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageAlarm : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_AlarmDevice     REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="733d8-112">Члены</span><span class="sxs-lookup"><span data-stu-id="733d8-112">Members</span></span>

<span data-ttu-id="733d8-113">Класс **CIM \_ паккажеаларм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="733d8-113">The **CIM\_PackageAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="733d8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="733d8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="733d8-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="733d8-115">Properties</span></span>

<span data-ttu-id="733d8-116">Класс **CIM \_ паккажеаларм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="733d8-116">The **CIM\_PackageAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="733d8-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="733d8-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="733d8-118">Тип данных: **CIM \_ алармдевице**</span><span class="sxs-lookup"><span data-stu-id="733d8-118">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="733d8-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="733d8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="733d8-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="733d8-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="733d8-121">[**\_ Алармдевице CIM**](cim-alarmdevice.md) , описывающий сигнальное устройство для пакета.</span><span class="sxs-lookup"><span data-stu-id="733d8-121">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that describes the alarm device for the package.</span></span>

</dd> <dt>

<span data-ttu-id="733d8-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="733d8-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="733d8-123">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="733d8-123">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="733d8-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="733d8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="733d8-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="733d8-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="733d8-126">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, состояние работоспособности, безопасность, окружение и т. д.</span><span class="sxs-lookup"><span data-stu-id="733d8-126">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose health, security, environment, etc. is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="733d8-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="733d8-127">Remarks</span></span>

<span data-ttu-id="733d8-128">**Модель CIM \_ Паккажеаларм** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="733d8-128">**CIM\_PackageAlarm** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="733d8-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="733d8-129">WMI does not implement this class.</span></span>

<span data-ttu-id="733d8-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="733d8-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="733d8-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="733d8-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="733d8-132">Требования</span><span class="sxs-lookup"><span data-stu-id="733d8-132">Requirements</span></span>



| <span data-ttu-id="733d8-133">Требование</span><span class="sxs-lookup"><span data-stu-id="733d8-133">Requirement</span></span> | <span data-ttu-id="733d8-134">Значение</span><span class="sxs-lookup"><span data-stu-id="733d8-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="733d8-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="733d8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="733d8-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="733d8-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="733d8-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="733d8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="733d8-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="733d8-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="733d8-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="733d8-139">Namespace</span></span><br/>                | <span data-ttu-id="733d8-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="733d8-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="733d8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="733d8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="733d8-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="733d8-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="733d8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="733d8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="733d8-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="733d8-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="733d8-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="733d8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="733d8-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="733d8-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

