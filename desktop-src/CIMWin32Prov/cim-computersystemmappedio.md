---
description: Класс CIM \_ компутерсистеммаппедио представляет ассоциацию между компьютером и его доступными портами ввода-вывода, размещенными в памяти.
ms.assetid: 5df9db36-67ad-4a94-a7db-150b58977af1
ms.tgt_platform: multiple
title: Класс CIM_ComputerSystemMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystemMappedIO
- CIM_ComputerSystemMappedIO.GroupComponent
- CIM_ComputerSystemMappedIO.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ce7d00950038c7d94f97f9a6938b9190846f6ff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141935"
---
# <a name="cim_computersystemmappedio-class"></a><span data-ttu-id="1c95b-103">\_Класс CIM компутерсистеммаппедио</span><span class="sxs-lookup"><span data-stu-id="1c95b-103">CIM\_ComputerSystemMappedIO class</span></span>

<span data-ttu-id="1c95b-104">Класс **CIM \_ компутерсистеммаппедио** представляет ассоциацию между компьютером и его доступными портами ввода-вывода, размещенными в памяти.</span><span class="sxs-lookup"><span data-stu-id="1c95b-104">The **CIM\_ComputerSystemMappedIO** class represents an association between a computer system and its available memory-mapped I/O ports.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c95b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="1c95b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1c95b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1c95b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1c95b-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1c95b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="1c95b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1c95b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c95b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c95b-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2EFC897-E3D3-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ComputerSystemMappedIO : CIM_ComputerSystemResource
{
  CIM_ComputerSystem REF GroupComponent;
  CIM_MemoryMappedIO REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="1c95b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1c95b-110">Members</span></span>

<span data-ttu-id="1c95b-111">Класс **CIM \_ компутерсистеммаппедио** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c95b-111">The **CIM\_ComputerSystemMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="1c95b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c95b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c95b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c95b-113">Properties</span></span>

<span data-ttu-id="1c95b-114">Класс **CIM \_ компутерсистеммаппедио** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c95b-114">The **CIM\_ComputerSystemMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c95b-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="1c95b-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c95b-116">Тип данных: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="1c95b-116">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="1c95b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c95b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c95b-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span><span class="sxs-lookup"><span data-stu-id="1c95b-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (GroupComponent)</span></span>
</dt> </dl>

<span data-ttu-id="1c95b-119">Система [**CIM \_**](cim-computersystem.md) , описывающая компьютерную систему, сопоставленную с портом ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="1c95b-119">A [**CIM\_ComputerSystem**](cim-computersystem.md) that describes the computer system mapped to the I/O port.</span></span>

<span data-ttu-id="1c95b-120">Это свойство наследуется от [ **CIM \_ компутерсистемресаурце**](cim-computersystemresource.md)</span><span class="sxs-lookup"><span data-stu-id="1c95b-120">This property is inherited from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md)</span></span>

</dd> <dt>

<span data-ttu-id="1c95b-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="1c95b-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c95b-122">Тип данных: **CIM \_ меморимаппедио**</span><span class="sxs-lookup"><span data-stu-id="1c95b-122">Data type: **CIM\_MemoryMappedIO**</span></span>
</dt> <dt>

<span data-ttu-id="1c95b-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c95b-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c95b-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**слабый**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="1c95b-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="1c95b-125">[**\_ Меморимаппедио CIM**](cim-memorymappedio.md) , описывающий назначенный памятью порт ввода-вывода компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="1c95b-125">A [**CIM\_MemoryMappedIO**](cim-memorymappedio.md) that describes a memory mapped I/O port of the computer system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c95b-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c95b-126">Remarks</span></span>

<span data-ttu-id="1c95b-127">Класс **CIM \_ компутерсистеммаппедио** является производным от [**CIM \_ компутерсистемресаурце**](cim-computersystemresource.md).</span><span class="sxs-lookup"><span data-stu-id="1c95b-127">The **CIM\_ComputerSystemMappedIO** class is derived from [**CIM\_ComputerSystemResource**](cim-computersystemresource.md).</span></span>

<span data-ttu-id="1c95b-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1c95b-128">WMI does not implement this class.</span></span>

<span data-ttu-id="1c95b-129">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="1c95b-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1c95b-130">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1c95b-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c95b-131">Требования</span><span class="sxs-lookup"><span data-stu-id="1c95b-131">Requirements</span></span>



| <span data-ttu-id="1c95b-132">Требование</span><span class="sxs-lookup"><span data-stu-id="1c95b-132">Requirement</span></span> | <span data-ttu-id="1c95b-133">Значение</span><span class="sxs-lookup"><span data-stu-id="1c95b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c95b-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c95b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1c95b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c95b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c95b-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c95b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1c95b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c95b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c95b-138">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c95b-138">Namespace</span></span><br/>                | <span data-ttu-id="1c95b-139">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c95b-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c95b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1c95b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c95b-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c95b-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c95b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="1c95b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c95b-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c95b-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c95b-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c95b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c95b-145">**\_КОМПУТЕРСИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="1c95b-145">**CIM\_ComputerSystemResource**</span></span>](cim-computersystemresource.md)
</dt> </dl>

 

