---
description: Класс CIM \_ фисикалелементлокатион связывает физический элемент с \_ объектом расположения CIM для целей инвентаризации или замены.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: Класс CIM_PhysicalElementLocation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142352"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="1c998-103">\_Класс CIM фисикалелементлокатион</span><span class="sxs-lookup"><span data-stu-id="1c998-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="1c998-104">Класс **CIM \_ фисикалелементлокатион** связывает физический элемент с объектом [**\_ расположения CIM**](cim-location.md) для целей инвентаризации или замены.</span><span class="sxs-lookup"><span data-stu-id="1c998-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1c998-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="1c998-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="1c998-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="1c998-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="1c998-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="1c998-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="1c998-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="1c998-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c998-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1c998-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="1c998-110">Члены</span><span class="sxs-lookup"><span data-stu-id="1c998-110">Members</span></span>

<span data-ttu-id="1c998-111">Класс **CIM \_ фисикалелементлокатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c998-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="1c998-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c998-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1c998-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="1c998-113">Properties</span></span>

<span data-ttu-id="1c998-114">Класс **CIM \_ фисикалелементлокатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1c998-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1c998-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="1c998-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c998-116">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="1c998-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="1c998-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c998-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1c998-118">Ссылка на физический элемент, расположение которого указано.</span><span class="sxs-lookup"><span data-stu-id="1c998-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="1c998-119">**фисикаллокатион**</span><span class="sxs-lookup"><span data-stu-id="1c998-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1c998-120">Тип данных: **\_ Расположение CIM**</span><span class="sxs-lookup"><span data-stu-id="1c998-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="1c998-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="1c998-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1c998-122">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="1c998-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="1c998-123">Ссылка на расположение физического элемента.</span><span class="sxs-lookup"><span data-stu-id="1c998-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1c998-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c998-124">Remarks</span></span>

<span data-ttu-id="1c998-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="1c998-125">WMI does not implement this class.</span></span>

<span data-ttu-id="1c998-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="1c998-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="1c998-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1c998-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c998-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1c998-128">Requirements</span></span>



| <span data-ttu-id="1c998-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1c998-129">Requirement</span></span> | <span data-ttu-id="1c998-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1c998-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c998-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c998-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1c998-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c998-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c998-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c998-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1c998-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c998-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c998-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1c998-135">Namespace</span></span><br/>                | <span data-ttu-id="1c998-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1c998-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1c998-137">MOF</span><span class="sxs-lookup"><span data-stu-id="1c998-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c998-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c998-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c998-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1c998-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c998-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c998-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

