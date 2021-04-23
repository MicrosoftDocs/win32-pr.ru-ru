---
description: Класс CIM \_ статистикалинформатион является корневым классом для произвольной коллекции статистических данных или метрик, применимых к одному или нескольким управляемым системным элементам.
ms.assetid: ecc3b310-c553-416b-b4e3-705965557945
ms.tgt_platform: multiple
title: Класс CIM_StatisticalInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StatisticalInformation
- CIM_StatisticalInformation.Caption
- CIM_StatisticalInformation.Description
- CIM_StatisticalInformation.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6eda3e2463c880a58c4e23a6d09dcab99417ead
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896426"
---
# <a name="cim_statisticalinformation-class"></a><span data-ttu-id="ed630-103">\_Класс CIM статистикалинформатион</span><span class="sxs-lookup"><span data-stu-id="ed630-103">CIM\_StatisticalInformation class</span></span>

<span data-ttu-id="ed630-104">Класс **CIM \_ статистикалинформатион** является корневым классом для произвольной коллекции статистических данных или метрик, применимых к одному или нескольким управляемым системным элементам.</span><span class="sxs-lookup"><span data-stu-id="ed630-104">The **CIM\_StatisticalInformation** class is a root class for the arbitrary collection of statistical data or metrics applicable to one or more managed system elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed630-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ed630-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ed630-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ed630-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ed630-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ed630-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="ed630-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ed630-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed630-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed630-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{956597A1-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_StatisticalInformation
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="ed630-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ed630-110">Members</span></span>

<span data-ttu-id="ed630-111">Класс **CIM \_ статистикалинформатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ed630-111">The **CIM\_StatisticalInformation** class has these types of members:</span></span>

-   [<span data-ttu-id="ed630-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed630-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ed630-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ed630-113">Properties</span></span>

<span data-ttu-id="ed630-114">Класс **CIM \_ статистикалинформатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ed630-114">The **CIM\_StatisticalInformation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed630-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ed630-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed630-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed630-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed630-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed630-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed630-118">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="ed630-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="ed630-119">Краткое текстовое описание для статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="ed630-119">Short textual description for the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="ed630-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ed630-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed630-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed630-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed630-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed630-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed630-123">Текстовое описание статистики или метрики.</span><span class="sxs-lookup"><span data-stu-id="ed630-123">Textual description of the statistic or metric.</span></span>

</dd> <dt>

<span data-ttu-id="ed630-124">**Name**</span><span class="sxs-lookup"><span data-stu-id="ed630-124">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed630-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ed630-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed630-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ed630-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed630-127">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="ed630-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="ed630-128">Метка, на которой известна статистика или метрика.</span><span class="sxs-lookup"><span data-stu-id="ed630-128">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="ed630-129">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="ed630-129">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed630-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed630-130">Remarks</span></span>

<span data-ttu-id="ed630-131">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ed630-131">WMI does not implement this class.</span></span> <span data-ttu-id="ed630-132">Классы WMI, производные от **CIM \_ статистикалинформатион**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ed630-132">For WMI classes derived from **CIM\_StatisticalInformation**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="ed630-133">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ed630-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ed630-134">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ed630-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed630-135">Требования</span><span class="sxs-lookup"><span data-stu-id="ed630-135">Requirements</span></span>



| <span data-ttu-id="ed630-136">Требование</span><span class="sxs-lookup"><span data-stu-id="ed630-136">Requirement</span></span> | <span data-ttu-id="ed630-137">Значение</span><span class="sxs-lookup"><span data-stu-id="ed630-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed630-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed630-138">Minimum supported client</span></span><br/> | <span data-ttu-id="ed630-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed630-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed630-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed630-140">Minimum supported server</span></span><br/> | <span data-ttu-id="ed630-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed630-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed630-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ed630-142">Namespace</span></span><br/>                | <span data-ttu-id="ed630-143">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ed630-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed630-144">MOF</span><span class="sxs-lookup"><span data-stu-id="ed630-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed630-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed630-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed630-146">DLL</span><span class="sxs-lookup"><span data-stu-id="ed630-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed630-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed630-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

