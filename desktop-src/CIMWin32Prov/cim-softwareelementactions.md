---
description: '\_Ассоциация СОФТВАРИЛЕМЕНТАКТИОНС CIM определяет действия для программного элемента.'
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: Класс CIM_SoftwareElementActions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655755"
---
# <a name="cim_softwareelementactions-class"></a><span data-ttu-id="6b12b-103">\_Класс CIM софтварилементактионс</span><span class="sxs-lookup"><span data-stu-id="6b12b-103">CIM\_SoftwareElementActions class</span></span>

<span data-ttu-id="6b12b-104">Ассоциация **\_ софтварилементактионс CIM** определяет действия для программного элемента.</span><span class="sxs-lookup"><span data-stu-id="6b12b-104">The **CIM\_SoftwareElementActions** association identifies the actions for a software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6b12b-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="6b12b-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6b12b-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6b12b-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6b12b-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="6b12b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="6b12b-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="6b12b-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b12b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b12b-109">Syntax</span></span>

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a><span data-ttu-id="6b12b-110">Члены</span><span class="sxs-lookup"><span data-stu-id="6b12b-110">Members</span></span>

<span data-ttu-id="6b12b-111">Класс **CIM \_ софтварилементактионс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="6b12b-111">The **CIM\_SoftwareElementActions** class has these types of members:</span></span>

-   [<span data-ttu-id="6b12b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b12b-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6b12b-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b12b-113">Properties</span></span>

<span data-ttu-id="6b12b-114">Класс **CIM \_ софтварилементактионс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6b12b-114">The **CIM\_SoftwareElementActions** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6b12b-115">**Действие**</span><span class="sxs-lookup"><span data-stu-id="6b12b-115">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b12b-116">Тип данных: **\_ действие CIM**</span><span class="sxs-lookup"><span data-stu-id="6b12b-116">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="6b12b-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b12b-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b12b-118">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**слабая**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b12b-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b12b-119">Ссылка на экземпляр [**\_ действия CIM**](cim-action.md) .</span><span class="sxs-lookup"><span data-stu-id="6b12b-119">Reference to a [**CIM\_Action**](cim-action.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="6b12b-120">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="6b12b-120">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6b12b-121">Тип данных: **CIM \_ софтварилемент**</span><span class="sxs-lookup"><span data-stu-id="6b12b-121">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="6b12b-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="6b12b-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6b12b-123">Квалификаторы: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="6b12b-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="6b12b-124">Ссылка на экземпляр [**CIM \_ софтварилемент**](cim-softwareelement.md) .</span><span class="sxs-lookup"><span data-stu-id="6b12b-124">Reference to a [**CIM\_SoftwareElement**](cim-softwareelement.md) instance.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b12b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b12b-125">Remarks</span></span>

<span data-ttu-id="6b12b-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="6b12b-126">WMI does not implement this class.</span></span> <span data-ttu-id="6b12b-127">Классы WMI, производные от **CIM \_ софтварилементактионс**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b12b-127">For WMI classes derived from **CIM\_SoftwareElementActions**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="6b12b-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="6b12b-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6b12b-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6b12b-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b12b-130">Требования</span><span class="sxs-lookup"><span data-stu-id="6b12b-130">Requirements</span></span>



| <span data-ttu-id="6b12b-131">Требование</span><span class="sxs-lookup"><span data-stu-id="6b12b-131">Requirement</span></span> | <span data-ttu-id="6b12b-132">Значение</span><span class="sxs-lookup"><span data-stu-id="6b12b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b12b-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6b12b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6b12b-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b12b-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6b12b-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6b12b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6b12b-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b12b-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6b12b-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6b12b-137">Namespace</span></span><br/>                | <span data-ttu-id="6b12b-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="6b12b-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6b12b-139">MOF</span><span class="sxs-lookup"><span data-stu-id="6b12b-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6b12b-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6b12b-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6b12b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6b12b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b12b-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b12b-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

