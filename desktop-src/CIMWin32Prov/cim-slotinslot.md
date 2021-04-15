---
description: Отношение CIM \_ слотинслот представляет возможность специального адаптера расширить существующую структуру слота, чтобы обеспечить подключение несовместимых карт в кадр или на доску размещения.
ms.assetid: 688231de-49fd-415d-b2c8-ef0dd4dcaee4
ms.tgt_platform: multiple
title: Класс CIM_SlotInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SlotInSlot
- CIM_SlotInSlot.Dependent
- CIM_SlotInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0102a431393906b5ff98339569a027cbe3ef5b40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655686"
---
# <a name="cim_slotinslot-class"></a><span data-ttu-id="747c0-103">\_Класс CIM слотинслот</span><span class="sxs-lookup"><span data-stu-id="747c0-103">CIM\_SlotInSlot class</span></span>

<span data-ttu-id="747c0-104">Отношение **CIM \_ слотинслот** представляет возможность специального адаптера расширить существующую структуру слота, чтобы обеспечить подключение несовместимых карт в кадр или на доску размещения.</span><span class="sxs-lookup"><span data-stu-id="747c0-104">The **CIM\_SlotInSlot** relationship represents the ability of a special adapter to extend the existing slot structure to enable otherwise incompatible cards to be plugged into a frame or hosting board.</span></span> <span data-ttu-id="747c0-105">Слоты — это специальные типы соединителей, в которые обычно вставляются адаптеры адаптеров.</span><span class="sxs-lookup"><span data-stu-id="747c0-105">Slots are special types of connectors into which adapter cards are typically inserted.</span></span> <span data-ttu-id="747c0-106">Адаптер эффективно создает новый слот, и его можно рассматривать (концептуально) в качестве слота в слоте.</span><span class="sxs-lookup"><span data-stu-id="747c0-106">The adapter effectively creates a new slot and can be thought of (conceptually) as a slot in a slot.</span></span> <span data-ttu-id="747c0-107">Карты, которые в противном случае были бы физически или электрически несовместимы с существующими слотами, будут поддерживаться при обращении к слоту, предоставленному адаптером.</span><span class="sxs-lookup"><span data-stu-id="747c0-107">Cards that would otherwise be physically or electrically incompatible with the existing slots would be supported by interfacing to the slot provided by the adapter.</span></span> <span data-ttu-id="747c0-108">Например, сетевые платы очень дороги.</span><span class="sxs-lookup"><span data-stu-id="747c0-108">For example, networking boards are very expensive.</span></span> <span data-ttu-id="747c0-109">После того как новое оборудование станет доступным, конфигурация корпуса и платы изменится.</span><span class="sxs-lookup"><span data-stu-id="747c0-109">As new hardware becomes available, chassis and card configurations change.</span></span> <span data-ttu-id="747c0-110">Чтобы защитить инвестиции клиентов, поставщики сети будут создавать специальные адаптеры, позволяющие старым картам размещаться на новом корпусе или на плате размещения или на новых картах, чтобы они соответствовали старым картам, используя специальный адаптер, который соответствует одному или нескольким существующим слотам, и представляет новый слот, в котором карта может уместиться.</span><span class="sxs-lookup"><span data-stu-id="747c0-110">To protect the investment of their customers, networking vendors will manufacture special adapters that enable old cards to fit into new chassis or hosting boards or new cards to fit into old cards by using a special adapter that fits over one or more existing slots and presents a new slot into which the card can fit.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="747c0-111">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="747c0-111">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="747c0-112">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="747c0-112">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="747c0-113">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="747c0-113">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="747c0-114">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="747c0-114">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="747c0-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="747c0-115">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B87-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_SlotInSlot : CIM_ConnectedTo
{
  CIM_Slot REF Dependent;
  CIM_Slot REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="747c0-116">Члены</span><span class="sxs-lookup"><span data-stu-id="747c0-116">Members</span></span>

<span data-ttu-id="747c0-117">Класс **CIM \_ слотинслот** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="747c0-117">The **CIM\_SlotInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="747c0-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="747c0-118">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="747c0-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="747c0-119">Properties</span></span>

<span data-ttu-id="747c0-120">Класс **CIM \_ слотинслот** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="747c0-120">The **CIM\_SlotInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="747c0-121">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="747c0-121">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="747c0-122">Тип данных: **\_ слот CIM**</span><span class="sxs-lookup"><span data-stu-id="747c0-122">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="747c0-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="747c0-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="747c0-124">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="747c0-124">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="747c0-125">[**\_ Слот CIM**](cim-slot.md) , описывающий существующие слоты платы размещения, или кадр, который адаптируется для размещения карты, которая в противном случае не была физически и/или электрически совместима с ней.</span><span class="sxs-lookup"><span data-stu-id="747c0-125">A [**CIM\_Slot**](cim-slot.md) that describes the existing slot(s) of the hosting board, or frame that are being adapted to accommodate a card that would otherwise not be physically and/or electrically compatible with it.</span></span>

</dd> <dt>

<span data-ttu-id="747c0-126">**Него**</span><span class="sxs-lookup"><span data-stu-id="747c0-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="747c0-127">Тип данных: **\_ слот CIM**</span><span class="sxs-lookup"><span data-stu-id="747c0-127">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="747c0-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="747c0-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="747c0-129">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="747c0-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="747c0-130">[**\_ Слот CIM**](cim-slot.md) , описывающий новый слот, предоставляемый платой адаптера.</span><span class="sxs-lookup"><span data-stu-id="747c0-130">A [**CIM\_Slot**](cim-slot.md) that describes the new slot provided by the adapter board.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="747c0-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="747c0-131">Remarks</span></span>

<span data-ttu-id="747c0-132">Класс **CIM \_ слотинслот** является производным от [**CIM \_ коннектедто**](cim-connectedto.md).</span><span class="sxs-lookup"><span data-stu-id="747c0-132">The **CIM\_SlotInSlot** class is derived from [**CIM\_ConnectedTo**](cim-connectedto.md).</span></span>

<span data-ttu-id="747c0-133">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="747c0-133">WMI does not implement this class.</span></span>

<span data-ttu-id="747c0-134">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="747c0-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="747c0-135">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="747c0-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="747c0-136">Требования</span><span class="sxs-lookup"><span data-stu-id="747c0-136">Requirements</span></span>



| <span data-ttu-id="747c0-137">Требование</span><span class="sxs-lookup"><span data-stu-id="747c0-137">Requirement</span></span> | <span data-ttu-id="747c0-138">Значение</span><span class="sxs-lookup"><span data-stu-id="747c0-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="747c0-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="747c0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="747c0-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="747c0-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="747c0-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="747c0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="747c0-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="747c0-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="747c0-143">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="747c0-143">Namespace</span></span><br/>                | <span data-ttu-id="747c0-144">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="747c0-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="747c0-145">MOF</span><span class="sxs-lookup"><span data-stu-id="747c0-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="747c0-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="747c0-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="747c0-147">DLL</span><span class="sxs-lookup"><span data-stu-id="747c0-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="747c0-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="747c0-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="747c0-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="747c0-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="747c0-150">**\_КОННЕКТЕДТО CIM**</span><span class="sxs-lookup"><span data-stu-id="747c0-150">**CIM\_ConnectedTo**</span></span>](cim-connectedto.md)
</dt> </dl>

 

