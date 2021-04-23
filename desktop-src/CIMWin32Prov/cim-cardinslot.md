---
description: Класс CIM \_ кардинслот связывает адаптер адаптера с контейнером, в который он вставлен.
ms.assetid: 253fb444-2a9e-4099-a4d5-352b643d8e32
ms.tgt_platform: multiple
title: Класс CIM_CardInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardInSlot
- CIM_CardInSlot.Dependent
- CIM_CardInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 19c6e7334b8a13854241c3fd2ee41dd7010255b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896126"
---
# <a name="cim_cardinslot-class"></a><span data-ttu-id="7a829-103">\_Класс CIM кардинслот</span><span class="sxs-lookup"><span data-stu-id="7a829-103">CIM\_CardInSlot class</span></span>

<span data-ttu-id="7a829-104">Класс **CIM \_ кардинслот** связывает адаптер адаптера с контейнером, в который он вставлен.</span><span class="sxs-lookup"><span data-stu-id="7a829-104">The **CIM\_CardInSlot** class associates an adapter card with the container into which it is inserted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7a829-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7a829-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7a829-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7a829-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7a829-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7a829-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7a829-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7a829-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a829-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7a829-109">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|System Slot|004.4"), UUID("{FAF76B8A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardInSlot : CIM_PackageInSlot
{
  CIM_Card REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="7a829-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7a829-110">Members</span></span>

<span data-ttu-id="7a829-111">Класс **CIM \_ кардинслот** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7a829-111">The **CIM\_CardInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="7a829-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a829-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7a829-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a829-113">Properties</span></span>

<span data-ttu-id="7a829-114">Класс **CIM \_ кардинслот** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7a829-114">The **CIM\_CardInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7a829-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="7a829-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a829-116">Тип данных: **\_ слот CIM**</span><span class="sxs-lookup"><span data-stu-id="7a829-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="7a829-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a829-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a829-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="7a829-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="7a829-119">[**\_ Слот CIM**](cim-slot.md) , описывающий слот, в который вставлена карта.</span><span class="sxs-lookup"><span data-stu-id="7a829-119">A [**CIM\_Slot**](cim-slot.md) that describes the slot into which the card is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="7a829-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="7a829-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7a829-121">Тип данных: **\_ карта CIM**</span><span class="sxs-lookup"><span data-stu-id="7a829-121">Data type: **CIM\_Card**</span></span>
</dt> <dt>

<span data-ttu-id="7a829-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7a829-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7a829-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="7a829-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="7a829-124">[**\_ Карта CIM**](cim-card.md) , которая описывает карточку в слоте.</span><span class="sxs-lookup"><span data-stu-id="7a829-124">A [**CIM\_Card**](cim-card.md) that describes the card in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a829-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7a829-125">Remarks</span></span>

<span data-ttu-id="7a829-126">Класс **CIM \_ кардинслот** является производным от [**CIM \_ паккажеинслот**](cim-packageinslot.md).</span><span class="sxs-lookup"><span data-stu-id="7a829-126">The **CIM\_CardInSlot** class is derived from [**CIM\_PackageInSlot**](cim-packageinslot.md).</span></span>

<span data-ttu-id="7a829-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7a829-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7a829-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7a829-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7a829-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7a829-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a829-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7a829-130">Requirements</span></span>



| <span data-ttu-id="7a829-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7a829-131">Requirement</span></span> | <span data-ttu-id="7a829-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7a829-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a829-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7a829-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7a829-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a829-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a829-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7a829-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7a829-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a829-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a829-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7a829-137">Namespace</span></span><br/>                | <span data-ttu-id="7a829-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a829-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a829-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7a829-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a829-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a829-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a829-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7a829-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a829-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a829-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a829-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7a829-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a829-144">**\_ПАККАЖЕИНСЛОТ CIM**</span><span class="sxs-lookup"><span data-stu-id="7a829-144">**CIM\_PackageInSlot**</span></span>](cim-packageinslot.md)
</dt> </dl>

 

