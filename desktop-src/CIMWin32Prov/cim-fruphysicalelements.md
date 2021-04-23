---
description: Класс CIM \_ фруфисикалелементс представляет физические элементы, составляющие заменяемый элемент поля (FRU).
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: Класс CIM_FRUPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990591"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="fb9cd-103">\_Класс CIM фруфисикалелементс</span><span class="sxs-lookup"><span data-stu-id="fb9cd-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="fb9cd-104">Класс **CIM \_ фруфисикалелементс** представляет физические элементы, составляющие заменяемый элемент поля (FRU).</span><span class="sxs-lookup"><span data-stu-id="fb9cd-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb9cd-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fb9cd-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fb9cd-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fb9cd-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fb9cd-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb9cd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb9cd-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="fb9cd-110">Члены</span><span class="sxs-lookup"><span data-stu-id="fb9cd-110">Members</span></span>

<span data-ttu-id="fb9cd-111">Класс **CIM \_ фруфисикалелементс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fb9cd-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="fb9cd-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb9cd-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb9cd-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb9cd-113">Properties</span></span>

<span data-ttu-id="fb9cd-114">Класс **CIM \_ фруфисикалелементс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb9cd-115">**Компонент**</span><span class="sxs-lookup"><span data-stu-id="fb9cd-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb9cd-116">Тип данных: **CIM \_ фисикалелемент**</span><span class="sxs-lookup"><span data-stu-id="fb9cd-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="fb9cd-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fb9cd-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fb9cd-118">Ссылка на физический элемент, который является частью FRU.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="fb9cd-119">**ЭКСПЛУАТАЦИИ**</span><span class="sxs-lookup"><span data-stu-id="fb9cd-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb9cd-120">Тип данных: **CIM \_ FRU**</span><span class="sxs-lookup"><span data-stu-id="fb9cd-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="fb9cd-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fb9cd-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb9cd-122">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="fb9cd-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="fb9cd-123">Ссылка на FRU.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fb9cd-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb9cd-124">Remarks</span></span>

<span data-ttu-id="fb9cd-125">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-125">WMI does not implement this class.</span></span>

<span data-ttu-id="fb9cd-126">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fb9cd-127">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fb9cd-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb9cd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="fb9cd-128">Requirements</span></span>



| <span data-ttu-id="fb9cd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="fb9cd-129">Requirement</span></span> | <span data-ttu-id="fb9cd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="fb9cd-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9cd-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb9cd-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fb9cd-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fb9cd-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fb9cd-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb9cd-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fb9cd-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fb9cd-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fb9cd-135">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fb9cd-135">Namespace</span></span><br/>                | <span data-ttu-id="fb9cd-136">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fb9cd-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fb9cd-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fb9cd-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb9cd-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb9cd-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb9cd-139">DLL</span><span class="sxs-lookup"><span data-stu-id="fb9cd-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb9cd-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb9cd-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

