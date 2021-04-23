---
description: '\_Ассоциация ПАККАЖЕТЕМПСЕНСОР CIM представляет связь, в которой датчик температуры часто устанавливается в пакете, например в шасси или стойке, для мониторинга среды пакета.'
ms.assetid: 79f2c4d1-5e1a-4c5f-9ef4-0c8bc3926a13
ms.tgt_platform: multiple
title: Класс CIM_PackageTempSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageTempSensor
- CIM_PackageTempSensor.Dependent
- CIM_PackageTempSensor.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28c3fa3ba569a2bf3101d62734bb9e4d5372fcf0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141677"
---
# <a name="cim_packagetempsensor-class"></a><span data-ttu-id="8d2c3-103">\_Класс CIM паккажетемпсенсор</span><span class="sxs-lookup"><span data-stu-id="8d2c3-103">CIM\_PackageTempSensor class</span></span>

<span data-ttu-id="8d2c3-104">Ассоциация **\_ паккажетемпсенсор CIM** представляет связь, в которой датчик температуры часто устанавливается в пакете, например в шасси или стойке, для мониторинга среды пакета.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-104">The **CIM\_PackageTempSensor** association represents the relationship in which a temperature sensor is often installed in a package, such as a chassis or a rack, to monitor the package's environment.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d2c3-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8d2c3-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8d2c3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8d2c3-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8d2c3-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d2c3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8d2c3-109">Syntax</span></span>

``` syntax
[Abstract, Aggregation, UUID("{FAF76B8F-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageTempSensor : CIM_Dependency
{
  CIM_PhysicalPackage   REF Dependent;
  CIM_TemperatureSensor REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="8d2c3-110">Члены</span><span class="sxs-lookup"><span data-stu-id="8d2c3-110">Members</span></span>

<span data-ttu-id="8d2c3-111">Класс **CIM \_ паккажетемпсенсор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8d2c3-111">The **CIM\_PackageTempSensor** class has these types of members:</span></span>

-   [<span data-ttu-id="8d2c3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d2c3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8d2c3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="8d2c3-113">Properties</span></span>

<span data-ttu-id="8d2c3-114">Класс **CIM \_ паккажетемпсенсор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-114">The **CIM\_PackageTempSensor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8d2c3-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d2c3-116">Тип данных: **CIM \_ датчик температуры**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-116">Data type: **CIM\_TemperatureSensor**</span></span>
</dt> <dt>

<span data-ttu-id="8d2c3-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d2c3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d2c3-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="8d2c3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="8d2c3-119">[**\_ Датчик температуры CIM**](cim-temperaturesensor.md) , описывающий датчик температуры для пакета.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-119">A [**CIM\_TemperatureSensor**](cim-temperaturesensor.md) describing the temperature sensor for the package.</span></span>

</dd> <dt>

<span data-ttu-id="8d2c3-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8d2c3-121">Тип данных: **CIM \_ фисикалпаккаже**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="8d2c3-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8d2c3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8d2c3-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="8d2c3-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="8d2c3-124">[**\_ Фисикалпаккаже CIM**](cim-physicalpackage.md) , описывающий физический пакет, окружение которого отслеживается.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the physical package whose environment is monitored.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8d2c3-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8d2c3-125">Remarks</span></span>

<span data-ttu-id="8d2c3-126">**Модель CIM \_ Паккажетемпсенсор** является производным [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="8d2c3-126">**CIM\_PackageTempSensor** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="8d2c3-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-127">WMI does not implement this class.</span></span>

<span data-ttu-id="8d2c3-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8d2c3-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="8d2c3-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d2c3-130">Требования</span><span class="sxs-lookup"><span data-stu-id="8d2c3-130">Requirements</span></span>



| <span data-ttu-id="8d2c3-131">Требование</span><span class="sxs-lookup"><span data-stu-id="8d2c3-131">Requirement</span></span> | <span data-ttu-id="8d2c3-132">Значение</span><span class="sxs-lookup"><span data-stu-id="8d2c3-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d2c3-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8d2c3-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8d2c3-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8d2c3-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8d2c3-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8d2c3-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8d2c3-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8d2c3-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8d2c3-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8d2c3-137">Namespace</span></span><br/>                | <span data-ttu-id="8d2c3-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8d2c3-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8d2c3-139">MOF</span><span class="sxs-lookup"><span data-stu-id="8d2c3-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8d2c3-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8d2c3-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8d2c3-141">DLL</span><span class="sxs-lookup"><span data-stu-id="8d2c3-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d2c3-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d2c3-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d2c3-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8d2c3-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d2c3-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="8d2c3-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

