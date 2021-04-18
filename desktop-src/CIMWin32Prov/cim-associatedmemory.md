---
description: Класс CIM \_ ассоЦиатемемори связывает установленную или связанную память, например кэш-память с логическим устройством.
ms.assetid: b108d0cc-9353-4940-a5f6-34bb93330a62
ms.tgt_platform: multiple
title: Класс CIM_AssociatedMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedMemory
- CIM_AssociatedMemory.Dependent
- CIM_AssociatedMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cb1443f54ab273ef6c114b8645e5322c24785f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496482"
---
# <a name="cim_associatedmemory-class"></a><span data-ttu-id="2727a-103">\_Класс CIM ассоЦиатедмемори</span><span class="sxs-lookup"><span data-stu-id="2727a-103">CIM\_AssociatedMemory class</span></span>

<span data-ttu-id="2727a-104">Класс **CIM \_ ассоЦиатемемори** связывает установленную или связанную память, например кэш-память с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="2727a-104">The **CIM\_AssociateMemory** class associates installed or associated memory, such as cache memory with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2727a-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="2727a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2727a-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2727a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2727a-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="2727a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2727a-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2727a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2727a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2727a-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB0-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedMemory : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Memory        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="2727a-110">Члены</span><span class="sxs-lookup"><span data-stu-id="2727a-110">Members</span></span>

<span data-ttu-id="2727a-111">Класс **CIM \_ ассоЦиатедмемори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2727a-111">The **CIM\_AssociatedMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="2727a-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="2727a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2727a-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2727a-113">Properties</span></span>

<span data-ttu-id="2727a-114">Класс **CIM \_ ассоЦиатедмемори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2727a-114">The **CIM\_AssociatedMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2727a-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="2727a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2727a-116">Тип данных: **\_ память CIM**</span><span class="sxs-lookup"><span data-stu-id="2727a-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="2727a-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2727a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2727a-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="2727a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="2727a-119">[**\_ Память CIM**](cim-memory.md) , описывающая память, установленную на устройстве или связанной с ней.</span><span class="sxs-lookup"><span data-stu-id="2727a-119">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

</dd> <dt>

<span data-ttu-id="2727a-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="2727a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2727a-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="2727a-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="2727a-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2727a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2727a-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="2727a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="2727a-124">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="2727a-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2727a-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2727a-125">Remarks</span></span>

<span data-ttu-id="2727a-126">Класс **CIM \_ ассоЦиатедмемори** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="2727a-126">The **CIM\_AssociatedMemory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="2727a-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="2727a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2727a-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="2727a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2727a-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="2727a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2727a-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2727a-130">Requirements</span></span>



| <span data-ttu-id="2727a-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2727a-131">Requirement</span></span> | <span data-ttu-id="2727a-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2727a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2727a-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2727a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2727a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2727a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2727a-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2727a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2727a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2727a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2727a-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2727a-137">Namespace</span></span><br/>                | <span data-ttu-id="2727a-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2727a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2727a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2727a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2727a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2727a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2727a-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2727a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2727a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2727a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2727a-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2727a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2727a-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="2727a-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

