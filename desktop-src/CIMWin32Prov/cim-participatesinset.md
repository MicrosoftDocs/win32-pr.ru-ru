---
description: Класс CIM \_ партиЦипатесинсет определяет физические элементы, которые должны быть заменены вместе.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: Класс CIM_ParticipatesInSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896161"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="ffbec-103">\_Класс CIM партиЦипатесинсет</span><span class="sxs-lookup"><span data-stu-id="ffbec-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="ffbec-104">Класс **CIM \_ партиЦипатесинсет** определяет физические элементы, которые должны быть заменены вместе.</span><span class="sxs-lookup"><span data-stu-id="ffbec-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffbec-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ffbec-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ffbec-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ffbec-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ffbec-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ffbec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ffbec-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ffbec-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbec-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ffbec-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="ffbec-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ffbec-110">Members</span></span>

<span data-ttu-id="ffbec-111">Класс **CIM \_ партиЦипатесинсет** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ffbec-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="ffbec-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffbec-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffbec-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffbec-113">Properties</span></span>

<span data-ttu-id="ffbec-114">Класс **CIM \_ партиЦипатесинсет** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ffbec-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffbec-115">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ffbec-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffbec-116">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="ffbec-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="ffbec-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffbec-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffbec-118">Ссылка на физический элемент, который должен быть заменен другими элементами в качестве набора.</span><span class="sxs-lookup"><span data-stu-id="ffbec-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="ffbec-119">**Set**</span><span class="sxs-lookup"><span data-stu-id="ffbec-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffbec-120">Тип данных: **\_ Замена CIM**</span><span class="sxs-lookup"><span data-stu-id="ffbec-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="ffbec-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ffbec-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ffbec-122">Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ffbec-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ffbec-123">Ссылка на замещающий набор элементов.</span><span class="sxs-lookup"><span data-stu-id="ffbec-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffbec-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffbec-124">Remarks</span></span>

<span data-ttu-id="ffbec-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ffbec-125">WMI does not implement this class.</span></span>

<span data-ttu-id="ffbec-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ffbec-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ffbec-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ffbec-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbec-128">Требования</span><span class="sxs-lookup"><span data-stu-id="ffbec-128">Requirements</span></span>



| <span data-ttu-id="ffbec-129">Требование</span><span class="sxs-lookup"><span data-stu-id="ffbec-129">Requirement</span></span> | <span data-ttu-id="ffbec-130">Значение</span><span class="sxs-lookup"><span data-stu-id="ffbec-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbec-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ffbec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbec-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffbec-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ffbec-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ffbec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbec-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffbec-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ffbec-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ffbec-135">Namespace</span></span><br/>                | <span data-ttu-id="ffbec-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ffbec-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ffbec-137">MOF</span><span class="sxs-lookup"><span data-stu-id="ffbec-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffbec-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffbec-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffbec-139">DLL</span><span class="sxs-lookup"><span data-stu-id="ffbec-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffbec-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffbec-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

