---
description: '\_Класс замены CIM объединяет физические элементы, которые должны быть заменены вместе.'
ms.assetid: db55ae2d-49b3-4cc9-95ee-1e757f58a427
ms.tgt_platform: multiple
title: Класс CIM_ReplacementSet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReplacementSet
- CIM_ReplacementSet.Description
- CIM_ReplacementSet.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: defc63628e494465d7a31d8adcea758e538c4c9e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141071"
---
# <a name="cim_replacementset-class"></a><span data-ttu-id="fc8af-103">\_Класс замены CIM</span><span class="sxs-lookup"><span data-stu-id="fc8af-103">CIM\_ReplacementSet class</span></span>

<span data-ttu-id="fc8af-104">Класс **\_ замены CIM** объединяет физические элементы, которые должны быть заменены вместе.</span><span class="sxs-lookup"><span data-stu-id="fc8af-104">The **CIM\_ReplacementSet** class aggregates physical elements that must be replaced together.</span></span> <span data-ttu-id="fc8af-105">Например, при замене платы памяти микросхемы памяти компонента также могут быть удалены и заменены.</span><span class="sxs-lookup"><span data-stu-id="fc8af-105">For example, when replacing a memory card, the component memory chips can also be removed and replaced.</span></span> <span data-ttu-id="fc8af-106">Или можно использовать эту связь для замены или обновления набора микросхем памяти.</span><span class="sxs-lookup"><span data-stu-id="fc8af-106">Or, this association can be used to replace or upgrade a set of memory chips.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc8af-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="fc8af-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fc8af-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fc8af-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fc8af-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="fc8af-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="fc8af-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="fc8af-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc8af-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc8af-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B6C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ReplacementSet
{
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="fc8af-112">Члены</span><span class="sxs-lookup"><span data-stu-id="fc8af-112">Members</span></span>

<span data-ttu-id="fc8af-113">Класс **\_ замены CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fc8af-113">The **CIM\_ReplacementSet** class has these types of members:</span></span>

-   [<span data-ttu-id="fc8af-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc8af-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc8af-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="fc8af-115">Properties</span></span>

<span data-ttu-id="fc8af-116">Класс **\_ замены CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="fc8af-116">The **CIM\_ReplacementSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc8af-117">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fc8af-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc8af-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc8af-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc8af-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc8af-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc8af-120">Произвольная строка, указывающая сведения, связанные с этим классом.</span><span class="sxs-lookup"><span data-stu-id="fc8af-120">Free-form string that specifies information related to this class.</span></span> <span data-ttu-id="fc8af-121">Назначение набора или сведения, связанные с заменой элементов компонента, можно добавить в это свойство.</span><span class="sxs-lookup"><span data-stu-id="fc8af-121">The purpose of the set, or information related to how the component elements are replaced, can be included in this property.</span></span>

</dd> <dt>

<span data-ttu-id="fc8af-122">**Name**</span><span class="sxs-lookup"><span data-stu-id="fc8af-122">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc8af-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fc8af-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fc8af-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fc8af-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc8af-125">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="fc8af-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="fc8af-126">Произвольная строка, которая определяет метку для этого свойства.</span><span class="sxs-lookup"><span data-stu-id="fc8af-126">Free-form string that defines a label for this property.</span></span> <span data-ttu-id="fc8af-127">Это свойство является ключом объекта.</span><span class="sxs-lookup"><span data-stu-id="fc8af-127">This property is the key for the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc8af-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fc8af-128">Remarks</span></span>

<span data-ttu-id="fc8af-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="fc8af-129">WMI does not implement this class.</span></span>

<span data-ttu-id="fc8af-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="fc8af-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fc8af-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="fc8af-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc8af-132">Требования</span><span class="sxs-lookup"><span data-stu-id="fc8af-132">Requirements</span></span>



| <span data-ttu-id="fc8af-133">Требование</span><span class="sxs-lookup"><span data-stu-id="fc8af-133">Requirement</span></span> | <span data-ttu-id="fc8af-134">Значение</span><span class="sxs-lookup"><span data-stu-id="fc8af-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8af-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fc8af-135">Minimum supported client</span></span><br/> | <span data-ttu-id="fc8af-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc8af-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc8af-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fc8af-137">Minimum supported server</span></span><br/> | <span data-ttu-id="fc8af-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc8af-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc8af-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fc8af-139">Namespace</span></span><br/>                | <span data-ttu-id="fc8af-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fc8af-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc8af-141">MOF</span><span class="sxs-lookup"><span data-stu-id="fc8af-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc8af-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc8af-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fc8af-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc8af-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc8af-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

