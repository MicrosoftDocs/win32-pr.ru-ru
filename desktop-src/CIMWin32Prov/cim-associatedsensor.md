---
description: Класс CIM \_ ассоЦиатедсенсор связывает установленный датчик с логическим устройством. Датчик измеряет критические свойства ввода и вывода и может быть добавлен вместе с устройством или установлен поблизости.
ms.assetid: 8ccaa37f-b95f-4582-a694-23bdc15b8c8b
ms.tgt_platform: multiple
title: Класс CIM_AssociatedSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedSensor
- CIM_AssociatedSensor.Dependent
- CIM_AssociatedSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50eac6b8bd933762df0da0213c420f5895b74640
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896189"
---
# <a name="cim_associatedsensor-class"></a><span data-ttu-id="d1b9f-104">\_Класс CIM ассоЦиатедсенсор</span><span class="sxs-lookup"><span data-stu-id="d1b9f-104">CIM\_AssociatedSensor class</span></span>

<span data-ttu-id="d1b9f-105">Класс **CIM \_ ассоЦиатедсенсор** связывает установленный датчик с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-105">The **CIM\_AssociatedSensor** class associates an installed sensor with a logical device.</span></span> <span data-ttu-id="d1b9f-106">Датчик измеряет критические свойства ввода и вывода и может быть добавлен вместе с устройством или установлен поблизости.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-106">The sensor measures critical input and output properties, and can be included with the device or installed nearby.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1b9f-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d1b9f-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d1b9f-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d1b9f-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="d1b9f-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1b9f-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d1b9f-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A0-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedSensor : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Sensor        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d1b9f-112">Члены</span><span class="sxs-lookup"><span data-stu-id="d1b9f-112">Members</span></span>

<span data-ttu-id="d1b9f-113">Класс **CIM \_ ассоЦиатедсенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d1b9f-113">The **CIM\_AssociatedSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="d1b9f-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1b9f-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1b9f-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="d1b9f-115">Properties</span></span>

<span data-ttu-id="d1b9f-116">Класс **CIM \_ ассоЦиатедсенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-116">The **CIM\_AssociatedSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1b9f-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="d1b9f-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b9f-118">Тип данных: **\_ датчик CIM**</span><span class="sxs-lookup"><span data-stu-id="d1b9f-118">Data type: **CIM\_Sensor**</span></span>
</dt> <dt>

<span data-ttu-id="d1b9f-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1b9f-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b9f-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="d1b9f-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="d1b9f-121">[**\_ Датчик CIM**](cim-sensor.md) , описывающий датчик.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-121">A [**CIM\_Sensor**](cim-sensor.md) that describes the sensor.</span></span>

</dd> <dt>

<span data-ttu-id="d1b9f-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="d1b9f-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1b9f-123">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="d1b9f-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="d1b9f-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d1b9f-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1b9f-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="d1b9f-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="d1b9f-126">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство, для которого данные измеряются датчиком.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device for which information is measured by the sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1b9f-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d1b9f-127">Remarks</span></span>

<span data-ttu-id="d1b9f-128">Класс **CIM \_ ассоЦиатедсенсор** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d1b9f-128">The **CIM\_AssociatedSensor** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d1b9f-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-129">WMI does not implement this class.</span></span> <span data-ttu-id="d1b9f-130">Дополнительные сведения о классах, производных от **CIM \_ ассоЦиатедсенсор**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="d1b9f-130">For more information about classes derived from **CIM\_AssociatedSensor**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="d1b9f-131">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d1b9f-132">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d1b9f-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1b9f-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d1b9f-133">Requirements</span></span>



| <span data-ttu-id="d1b9f-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d1b9f-134">Requirement</span></span> | <span data-ttu-id="d1b9f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d1b9f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1b9f-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1b9f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d1b9f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1b9f-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1b9f-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1b9f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d1b9f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1b9f-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1b9f-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1b9f-140">Namespace</span></span><br/>                | <span data-ttu-id="d1b9f-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d1b9f-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d1b9f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d1b9f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1b9f-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9f-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1b9f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d1b9f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1b9f-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1b9f-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1b9f-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1b9f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1b9f-147">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="d1b9f-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

