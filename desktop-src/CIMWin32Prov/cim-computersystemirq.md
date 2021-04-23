---
description: Класс CIM \_ компутерсистемирк представляет связь между компьютерной системой и ее доступными линиями запросов на прерывание (IRQ).
ms.assetid: c2a1f231-1f8e-48b2-9afe-fa798e6a8a1d
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystemIRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemIRQ
- CIM_ComputerSystemIRQ.GroupComponent
- CIM_ComputerSystemIRQ.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 490b1f26e8d100f675a6e57a8ddf7a53770d4ea1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655943"
---
# <a name="cim_computersystemirq-class"></a><span data-ttu-id="298bf-103">\_Класс CIM компутерсистемирк</span><span class="sxs-lookup"><span data-stu-id="298bf-103">CIM\_ComputerSystemIRQ class</span></span>

<span data-ttu-id="298bf-104">Класс **CIM \_ компутерсистемирк** представляет связь между компьютерной системой и ее доступными линиями запросов на прерывание (IRQ).</span><span class="sxs-lookup"><span data-stu-id="298bf-104">The **CIM\_ComputerSystemIRQ** class represents an association between a computer system and its available interrupt request lines (IRQs).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="298bf-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="298bf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="298bf-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="298bf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="298bf-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="298bf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="298bf-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="298bf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="298bf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="298bf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC896-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemIRQ : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_IRQ            REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="298bf-110">Члены</span><span class="sxs-lookup"><span data-stu-id="298bf-110">Members</span></span>

<span data-ttu-id="298bf-111">Класс **CIM \_ компутерсистемирк** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="298bf-111">The **CIM\_ComputerSystemIRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="298bf-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="298bf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="298bf-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="298bf-113">Properties</span></span>

<span data-ttu-id="298bf-114">Класс **CIM \_ компутерсистемирк** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="298bf-114">The **CIM\_ComputerSystemIRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="298bf-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="298bf-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298bf-116">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="298bf-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="298bf-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="298bf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298bf-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="298bf-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="298bf-119">Объект [**CIM \_**](cim-computersystem.md) , описывающий компьютер, связанный с IRQ.</span><span class="sxs-lookup"><span data-stu-id="298bf-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) describing the computer associated with the IRQ.</span></span>

<span data-ttu-id="298bf-120">Это свойство наследуется от [ **CIM \_ компутерсистемресаурце**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="298bf-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="298bf-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="298bf-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298bf-122">Тип данных: **\_ IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="298bf-122">Data type: **CIM\_IRQ**</span></span>
</dt> <dt>

<span data-ttu-id="298bf-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="298bf-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="298bf-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="298bf-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="298bf-125">[**\_ IRQ CIM**](cim-irq.md) , описывающий IRQ компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="298bf-125">A [**CIM\_IRQ**](cim-irq.md) describing an IRQ of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="298bf-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="298bf-126">Remarks</span></span>

<span data-ttu-id="298bf-127">Класс **CIM \_ компутерсистемирк** является производным от [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="298bf-127">The **CIM\_ComputerSystemIRQ** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="298bf-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="298bf-128">WMI does not implement this class.</span></span>

<span data-ttu-id="298bf-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="298bf-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="298bf-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="298bf-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="298bf-131">Требования</span><span class="sxs-lookup"><span data-stu-id="298bf-131">Requirements</span></span>



| <span data-ttu-id="298bf-132">Требование</span><span class="sxs-lookup"><span data-stu-id="298bf-132">Requirement</span></span> | <span data-ttu-id="298bf-133">Значение</span><span class="sxs-lookup"><span data-stu-id="298bf-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="298bf-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="298bf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="298bf-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="298bf-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="298bf-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="298bf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="298bf-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="298bf-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="298bf-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="298bf-138">Namespace</span></span><br/>                | <span data-ttu-id="298bf-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="298bf-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="298bf-140">MOF</span><span class="sxs-lookup"><span data-stu-id="298bf-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="298bf-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="298bf-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="298bf-142">DLL</span><span class="sxs-lookup"><span data-stu-id="298bf-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="298bf-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="298bf-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="298bf-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="298bf-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298bf-145">**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="298bf-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

