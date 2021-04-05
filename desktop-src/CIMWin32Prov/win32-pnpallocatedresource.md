---
description: '\_Класс WMI взаимосвязей Win32 пнпаллокатедресаурце представляет связь между логическими устройствами и системными ресурсами.'
ms.assetid: e3cef457-cf88-4df5-8db8-b0495f636904
ms.tgt_platform: multiple
title: Класс Win32_PnPAllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPAllocatedResource
- Win32_PnPAllocatedResource.Antecedent
- Win32_PnPAllocatedResource.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353009016c8d4d54cdc92fb8f0ed062567dded6f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896478"
---
# <a name="win32_pnpallocatedresource-class"></a><span data-ttu-id="4c5f4-103">\_Класс Win32 пнпаллокатедресаурце</span><span class="sxs-lookup"><span data-stu-id="4c5f4-103">Win32\_PnPAllocatedResource class</span></span>

<span data-ttu-id="4c5f4-104">[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ пнпаллокатедресаурце** представляет связь между логическими устройствами и системными ресурсами.</span><span class="sxs-lookup"><span data-stu-id="4c5f4-104">The **Win32\_PnPAllocatedResource** association [WMI class](../wmisdk/retrieving-a-class.md) represents an association between logical devices and system resources.</span></span> <span data-ttu-id="4c5f4-105">Этот класс используется для обнаружения ресурсов, которые используются конкретным устройством, например запроса на прерывание (IRQ) или канала прямого доступа к памяти (DMA).</span><span class="sxs-lookup"><span data-stu-id="4c5f4-105">This class is used to discover the resources that are in-use by a specific device, such as an Interrupt ReQuest (IRQ) or a Direct Memory Access (DMA) channel.</span></span>

<span data-ttu-id="4c5f4-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="4c5f4-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="4c5f4-107">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="4c5f4-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5f4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c5f4-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("970C0998-41FE-4275-B7D9-7DABAD3FBC4D"), AMENDMENT]
class Win32_PnPAllocatedResource : CIM_AllocatedResource
{
  CIM_SystemResource REF Antecedent;
  Win32_PnPEntity    REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="4c5f4-109">Члены</span><span class="sxs-lookup"><span data-stu-id="4c5f4-109">Members</span></span>

<span data-ttu-id="4c5f4-110">Класс **Win32 \_ пнпаллокатедресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c5f4-110">The **Win32\_PnPAllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="4c5f4-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c5f4-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c5f4-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c5f4-112">Properties</span></span>

<span data-ttu-id="4c5f4-113">Класс **Win32 \_ пнпаллокатедресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4c5f4-113">The **Win32\_PnPAllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c5f4-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="4c5f4-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f4-115">Тип данных: **CIM \_ системресаурце**</span><span class="sxs-lookup"><span data-stu-id="4c5f4-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f4-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c5f4-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f4-117">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ системресаурце")</span><span class="sxs-lookup"><span data-stu-id="4c5f4-117">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="4c5f4-118">Ссылка на экземпляр [**CIM \_ системресаурце**](cim-systemresource.md) , представляющий свойства системного ресурса, доступного для логического устройства.</span><span class="sxs-lookup"><span data-stu-id="4c5f4-118">Reference to the [**CIM\_SystemResource**](cim-systemresource.md) instance that represents the properties of a system resource available to the logical device.</span></span> <span data-ttu-id="4c5f4-119">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4c5f4-119">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> <dt>

<span data-ttu-id="4c5f4-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="4c5f4-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c5f4-121">Тип данных: **Win32 \_ пнпентити**</span><span class="sxs-lookup"><span data-stu-id="4c5f4-121">Data type: **Win32\_PnPEntity**</span></span>
</dt> <dt>

<span data-ttu-id="4c5f4-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c5f4-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c5f4-123">Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("CIM \| CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="4c5f4-123">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="4c5f4-124">Ссылка на экземпляр [**Win32 \_ пнпентити**](win32-pnpentity.md) , который представляет свойства логического устройства, использующего назначенные ему ресурсы системы.</span><span class="sxs-lookup"><span data-stu-id="4c5f4-124">Reference to the [**Win32\_PnPEntity**](win32-pnpentity.md) instance that represents the properties of the logical device using the system resources assigned to it.</span></span> <span data-ttu-id="4c5f4-125">Это свойство наследуется [**от \_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="4c5f4-125">This property is inherited from [**CIM\_Dependency**](cim-dependency.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c5f4-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c5f4-126">Remarks</span></span>

<span data-ttu-id="4c5f4-127">Класс **Win32 \_ пнпаллокатедресаурце** является производным от [**CIM \_ аллокатедресаурце**](cim-allocatedresource.md).</span><span class="sxs-lookup"><span data-stu-id="4c5f4-127">The **Win32\_PnPAllocatedResource** class is derived from [**CIM\_AllocatedResource**](cim-allocatedresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4c5f4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="4c5f4-128">Requirements</span></span>



| <span data-ttu-id="4c5f4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="4c5f4-129">Requirement</span></span> | <span data-ttu-id="4c5f4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="4c5f4-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c5f4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c5f4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4c5f4-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c5f4-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c5f4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c5f4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4c5f4-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c5f4-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c5f4-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c5f4-135">Namespace</span></span><br/>                | <span data-ttu-id="4c5f4-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4c5f4-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c5f4-137">MOF</span><span class="sxs-lookup"><span data-stu-id="4c5f4-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c5f4-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c5f4-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c5f4-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4c5f4-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c5f4-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c5f4-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c5f4-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c5f4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c5f4-142">**\_АЛЛОКАТЕДРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="4c5f4-142">**CIM\_AllocatedResource**</span></span>](cim-allocatedresource.md)
</dt> <dt>

[<span data-ttu-id="4c5f4-143">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="4c5f4-143">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
