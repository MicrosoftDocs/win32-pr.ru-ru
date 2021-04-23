---
description: Класс " \_ классы CIM" представляет ассоциацию, которая определяет сопоставление между логическим устройством и физическим компонентом, реализующим устройство.
ms.assetid: 3bddb0c8-dca5-4877-9e30-322516a8d388
ms.tgt_platform: multiple
title: Класс CIM_Realizes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Realizes
- CIM_Realizes.Dependent
- CIM_Realizes.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b37b2f5f3fe9cfce78e16530df8b94e4333e9a33
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655835"
---
# <a name="cim_realizes-class"></a><span data-ttu-id="2ae29-103">\_Класс CIM</span><span class="sxs-lookup"><span data-stu-id="2ae29-103">CIM\_Realizes class</span></span>

<span data-ttu-id="2ae29-104">Класс "классы **CIM \_** " представляет ассоциацию, которая определяет сопоставление между логическим устройством и физическим компонентом, реализующим устройство.</span><span class="sxs-lookup"><span data-stu-id="2ae29-104">The **CIM\_Realizes** class represents the association that defines the mapping between a logical device and the physical component that implements the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ae29-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae29-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2ae29-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2ae29-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2ae29-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae29-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2ae29-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2ae29-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ae29-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ae29-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B62-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Realizes : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_PhysicalElement REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2ae29-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2ae29-110">Members</span></span>

<span data-ttu-id="2ae29-111">Классы **CIM \_** имеют следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2ae29-111">The **CIM\_Realizes** class has these types of members:</span></span>

-   [<span data-ttu-id="2ae29-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2ae29-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ae29-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2ae29-113">Properties</span></span>

<span data-ttu-id="2ae29-114">Классы **CIM \_** имеют эти свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae29-114">The **CIM\_Realizes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ae29-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2ae29-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-116">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="2ae29-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2ae29-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2ae29-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-119">[**\_ Фисикалелемент CIM**](cim-physicalelement.md) , описывающий физический компонент, который реализует устройство.</span><span class="sxs-lookup"><span data-stu-id="2ae29-119">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical component that implements the device.</span></span>

</dd> <dt>

<span data-ttu-id="2ae29-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="2ae29-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ae29-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="2ae29-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2ae29-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ae29-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="2ae29-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2ae29-124">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="2ae29-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ae29-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ae29-125">Remarks</span></span>

<span data-ttu-id="2ae29-126">Класс **CIM \_** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="2ae29-126">The **CIM\_Realizes** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2ae29-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="2ae29-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2ae29-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2ae29-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2ae29-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2ae29-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ae29-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2ae29-130">Requirements</span></span>



| <span data-ttu-id="2ae29-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2ae29-131">Requirement</span></span> | <span data-ttu-id="2ae29-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2ae29-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ae29-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2ae29-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2ae29-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ae29-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ae29-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2ae29-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2ae29-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ae29-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ae29-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2ae29-137">Namespace</span></span><br/>                | <span data-ttu-id="2ae29-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2ae29-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ae29-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2ae29-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ae29-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ae29-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ae29-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2ae29-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ae29-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ae29-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ae29-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ae29-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ae29-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="2ae29-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

