---
description: Класс CIM \_ биосфеатуребиоселементс связывает компонент BIOS и его агрегированные элементы BIOS.
ms.assetid: 84ebd6d0-af42-4e82-bad3-1f934789cbfe
ms.tgt_platform: multiple
title: Класс CIM_BIOSFeatureBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSFeatureBIOSElements
- CIM_BIOSFeatureBIOSElements.PartComponent
- CIM_BIOSFeatureBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a5a4eecea97b4d82fadcdc521d378b5b32d986b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142073"
---
# <a name="cim_biosfeaturebioselements-class"></a><span data-ttu-id="c2440-103">\_Класс CIM биосфеатуребиоселементс</span><span class="sxs-lookup"><span data-stu-id="c2440-103">CIM\_BIOSFeatureBIOSElements class</span></span>

<span data-ttu-id="c2440-104">Класс **CIM \_ биосфеатуребиоселементс** связывает компонент BIOS и его агрегированные элементы BIOS.</span><span class="sxs-lookup"><span data-stu-id="c2440-104">The **CIM\_BIOSFeatureBIOSElements** class associates a BIOS feature and its aggregated BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2440-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="c2440-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c2440-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c2440-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c2440-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="c2440-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c2440-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="c2440-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2440-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c2440-109">Syntax</span></span>

``` syntax
[UUID("{42B2EC5C-DB35-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_BIOSFeatureBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_BIOSElement REF PartComponent;
  CIM_BIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="c2440-110">Члены</span><span class="sxs-lookup"><span data-stu-id="c2440-110">Members</span></span>

<span data-ttu-id="c2440-111">Класс **CIM \_ биосфеатуребиоселементс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c2440-111">The **CIM\_BIOSFeatureBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="c2440-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2440-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c2440-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c2440-113">Properties</span></span>

<span data-ttu-id="c2440-114">Класс **CIM \_ биосфеатуребиоселементс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c2440-114">The **CIM\_BIOSFeatureBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c2440-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="c2440-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2440-116">Тип данных: **CIM \_ биосфеатуре**</span><span class="sxs-lookup"><span data-stu-id="c2440-116">Data type: **CIM\_BIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="c2440-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2440-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2440-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="c2440-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c2440-119">[**\_ Биосфеатуре CIM**](cim-biosfeature.md) , описывающий функцию BIOS.</span><span class="sxs-lookup"><span data-stu-id="c2440-119">A [**CIM\_BIOSFeature**](cim-biosfeature.md) that describes the BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="c2440-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c2440-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c2440-121">Тип данных: **CIM \_ биоселемент**</span><span class="sxs-lookup"><span data-stu-id="c2440-121">Data type: **CIM\_BIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="c2440-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c2440-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c2440-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c2440-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c2440-124">[**\_ Биоселемент CIM**](cim-bioselement.md) , описывающий элемент BIOS, который реализует возможности, описанные компонентом BIOS.</span><span class="sxs-lookup"><span data-stu-id="c2440-124">A [**CIM\_BIOSElement**](cim-bioselement.md) that describes the BIOS element that implements the capabilities described by BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2440-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c2440-125">Remarks</span></span>

<span data-ttu-id="c2440-126">Класс **CIM \_ биосфеатуребиоселементс** является производным от [**CIM \_ софтварефеатуресофтварилементс**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="c2440-126">The **CIM\_BIOSFeatureBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="c2440-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="c2440-127">WMI does not implement this class.</span></span>

<span data-ttu-id="c2440-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="c2440-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c2440-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c2440-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2440-130">Требования</span><span class="sxs-lookup"><span data-stu-id="c2440-130">Requirements</span></span>



| <span data-ttu-id="c2440-131">Требование</span><span class="sxs-lookup"><span data-stu-id="c2440-131">Requirement</span></span> | <span data-ttu-id="c2440-132">Значение</span><span class="sxs-lookup"><span data-stu-id="c2440-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2440-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c2440-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c2440-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2440-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c2440-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c2440-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c2440-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2440-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c2440-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c2440-137">Namespace</span></span><br/>                | <span data-ttu-id="c2440-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c2440-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c2440-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c2440-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c2440-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c2440-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c2440-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c2440-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2440-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2440-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2440-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c2440-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2440-144">**\_СОФТВАРЕФЕАТУРЕСОФТВАРИЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="c2440-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

