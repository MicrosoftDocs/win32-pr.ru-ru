---
description: Класс CIM \_ компутерсистемдма представляет связь между компьютерной системой и доступными каналами прямого доступа к памяти (DMA).
ms.assetid: 7d5bce4b-973f-4452-b403-a2196bd4017a
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystemDMA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemDMA
- CIM_ComputerSystemDMA.PartComponent
- CIM_ComputerSystemDMA.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23748a3b10c11878069a81cd82f7f69d0ab75792
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655944"
---
# <a name="cim_computersystemdma-class"></a><span data-ttu-id="98bfb-103">\_Класс CIM компутерсистемдма</span><span class="sxs-lookup"><span data-stu-id="98bfb-103">CIM\_ComputerSystemDMA class</span></span>

<span data-ttu-id="98bfb-104">Класс **CIM \_ компутерсистемдма** представляет связь между компьютерной системой и доступными каналами прямого доступа к памяти (DMA).</span><span class="sxs-lookup"><span data-stu-id="98bfb-104">The **CIM\_ComputerSystemDMA** class represents an association between a computer system and its available direct memory access (DMA) channels.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="98bfb-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="98bfb-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="98bfb-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="98bfb-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="98bfb-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="98bfb-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="98bfb-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="98bfb-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="98bfb-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98bfb-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{9B81340B-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemDMA : CIM_ComputerSystemResource
{
  CIM_DMA            REF PartComponent;
  CIM_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="98bfb-110">Члены</span><span class="sxs-lookup"><span data-stu-id="98bfb-110">Members</span></span>

<span data-ttu-id="98bfb-111">Класс **CIM \_ компутерсистемдма** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="98bfb-111">The **CIM\_ComputerSystemDMA** class has these types of members:</span></span>

-   [<span data-ttu-id="98bfb-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="98bfb-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98bfb-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="98bfb-113">Properties</span></span>

<span data-ttu-id="98bfb-114">Класс **CIM \_ компутерсистемдма** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="98bfb-114">The **CIM\_ComputerSystemDMA** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98bfb-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="98bfb-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98bfb-116">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="98bfb-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="98bfb-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98bfb-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98bfb-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="98bfb-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="98bfb-119">Объект [**CIM \_**](cim-computersystem.md) , описывающий компьютер, связанный с DMA.</span><span class="sxs-lookup"><span data-stu-id="98bfb-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer associated with the DMA.</span></span>

</dd> <dt>

<span data-ttu-id="98bfb-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="98bfb-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98bfb-121">Тип данных: **\_ канал передачи CIM**</span><span class="sxs-lookup"><span data-stu-id="98bfb-121">Data type: **CIM\_DMA**</span></span>
</dt> <dt>

<span data-ttu-id="98bfb-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98bfb-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98bfb-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="98bfb-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="98bfb-124">[**\_ DMA**](cim-dma.md) -канал, описывающий каналы DMA компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="98bfb-124">A [**CIM\_DMA**](cim-dma.md) that describes a DMA channel of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="98bfb-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98bfb-125">Remarks</span></span>

<span data-ttu-id="98bfb-126">Класс **CIM \_ компутерсистемдма** является производным от [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="98bfb-126">The **CIM\_ComputerSystemDMA** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="98bfb-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="98bfb-127">WMI does not implement this class.</span></span>

<span data-ttu-id="98bfb-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="98bfb-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="98bfb-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="98bfb-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="98bfb-130">Требования</span><span class="sxs-lookup"><span data-stu-id="98bfb-130">Requirements</span></span>



| <span data-ttu-id="98bfb-131">Требование</span><span class="sxs-lookup"><span data-stu-id="98bfb-131">Requirement</span></span> | <span data-ttu-id="98bfb-132">Значение</span><span class="sxs-lookup"><span data-stu-id="98bfb-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="98bfb-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98bfb-133">Minimum supported client</span></span><br/> | <span data-ttu-id="98bfb-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98bfb-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="98bfb-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98bfb-135">Minimum supported server</span></span><br/> | <span data-ttu-id="98bfb-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98bfb-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="98bfb-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="98bfb-137">Namespace</span></span><br/>                | <span data-ttu-id="98bfb-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="98bfb-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="98bfb-139">MOF</span><span class="sxs-lookup"><span data-stu-id="98bfb-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98bfb-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98bfb-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="98bfb-141">DLL</span><span class="sxs-lookup"><span data-stu-id="98bfb-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98bfb-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98bfb-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98bfb-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98bfb-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98bfb-144">**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="98bfb-144">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

