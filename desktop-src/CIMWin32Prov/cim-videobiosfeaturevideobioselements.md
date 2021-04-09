---
description: Класс CIM \_ видеобиосфеатуревидеобиоселементс связывает компонент Video BIOS и его объединенные элементы Video BIOS.
ms.assetid: f1419505-213f-450e-8c96-45f547dd71da
ms.tgt_platform: multiple
title: Класс CIM_VideoBIOSFeatureVideoBIOSElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VideoBIOSFeatureVideoBIOSElements
- CIM_VideoBIOSFeatureVideoBIOSElements.PartComponent
- CIM_VideoBIOSFeatureVideoBIOSElements.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 421b6814499240b3364ac1aed622e2b7c96e7313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141422"
---
# <a name="cim_videobiosfeaturevideobioselements-class"></a><span data-ttu-id="7fd81-103">\_Класс CIM видеобиосфеатуревидеобиоселементс</span><span class="sxs-lookup"><span data-stu-id="7fd81-103">CIM\_VideoBIOSFeatureVideoBIOSElements class</span></span>

<span data-ttu-id="7fd81-104">Класс **CIM \_ видеобиосфеатуревидеобиоселементс** связывает компонент Video BIOS и его объединенные элементы Video BIOS.</span><span class="sxs-lookup"><span data-stu-id="7fd81-104">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class associates a video BIOS feature and its aggregated video BIOS elements.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7fd81-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="7fd81-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7fd81-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7fd81-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7fd81-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="7fd81-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="7fd81-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="7fd81-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd81-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7fd81-109">Syntax</span></span>

``` syntax
[UUID("{B3F86390-DB37-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_VideoBIOSFeatureVideoBIOSElements : CIM_SoftwareFeatureSoftwareElements
{
  CIM_VideoBIOSElement REF PartComponent;
  CIM_VideoBIOSFeature REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="7fd81-110">Члены</span><span class="sxs-lookup"><span data-stu-id="7fd81-110">Members</span></span>

<span data-ttu-id="7fd81-111">Класс **CIM \_ видеобиосфеатуревидеобиоселементс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7fd81-111">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these types of members:</span></span>

-   [<span data-ttu-id="7fd81-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7fd81-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7fd81-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="7fd81-113">Properties</span></span>

<span data-ttu-id="7fd81-114">Класс **CIM \_ видеобиосфеатуревидеобиоселементс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7fd81-114">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7fd81-115">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="7fd81-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd81-116">Тип данных: **CIM \_ видеобиосфеатуре**</span><span class="sxs-lookup"><span data-stu-id="7fd81-116">Data type: **CIM\_VideoBIOSFeature**</span></span>
</dt> <dt>

<span data-ttu-id="7fd81-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fd81-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd81-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="7fd81-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7fd81-119">[**\_ Видеобиосфеатуре CIM**](cim-videobiosfeature.md) , описывающий функцию Video BIOS.</span><span class="sxs-lookup"><span data-stu-id="7fd81-119">A [**CIM\_VideoBIOSFeature**](cim-videobiosfeature.md) that describes the video BIOS feature.</span></span>

</dd> <dt>

<span data-ttu-id="7fd81-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7fd81-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7fd81-121">Тип данных: **CIM \_ видеобиоселемент**</span><span class="sxs-lookup"><span data-stu-id="7fd81-121">Data type: **CIM\_VideoBIOSElement**</span></span>
</dt> <dt>

<span data-ttu-id="7fd81-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7fd81-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7fd81-123">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="7fd81-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7fd81-124">[**\_ Видеобиоселемент CIM**](cim-videobioselement.md) , описывающий элемент Video BIOS, который реализует возможности, описываемые функцией Video BIOS.</span><span class="sxs-lookup"><span data-stu-id="7fd81-124">A [**CIM\_VideoBIOSElement**](cim-videobioselement.md) that describes the video BIOS element that implements the capabilities described by video BIOS feature.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7fd81-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7fd81-125">Remarks</span></span>

<span data-ttu-id="7fd81-126">Класс **CIM \_ видеобиосфеатуревидеобиоселементс** является производным от [**CIM \_ софтварефеатуресофтварилементс**](cim-softwarefeaturesoftwareelements.md).</span><span class="sxs-lookup"><span data-stu-id="7fd81-126">The **CIM\_VideoBIOSFeatureVideoBIOSElements** class is derived from [**CIM\_SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md).</span></span>

<span data-ttu-id="7fd81-127">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="7fd81-127">WMI does not implement this class.</span></span>

<span data-ttu-id="7fd81-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="7fd81-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7fd81-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="7fd81-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fd81-130">Требования</span><span class="sxs-lookup"><span data-stu-id="7fd81-130">Requirements</span></span>



| <span data-ttu-id="7fd81-131">Требование</span><span class="sxs-lookup"><span data-stu-id="7fd81-131">Requirement</span></span> | <span data-ttu-id="7fd81-132">Значение</span><span class="sxs-lookup"><span data-stu-id="7fd81-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7fd81-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7fd81-133">Minimum supported client</span></span><br/> | <span data-ttu-id="7fd81-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7fd81-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7fd81-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7fd81-135">Minimum supported server</span></span><br/> | <span data-ttu-id="7fd81-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7fd81-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7fd81-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7fd81-137">Namespace</span></span><br/>                | <span data-ttu-id="7fd81-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7fd81-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7fd81-139">MOF</span><span class="sxs-lookup"><span data-stu-id="7fd81-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7fd81-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7fd81-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7fd81-141">DLL</span><span class="sxs-lookup"><span data-stu-id="7fd81-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7fd81-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7fd81-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fd81-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7fd81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fd81-144">**\_СОФТВАРЕФЕАТУРЕСОФТВАРИЛЕМЕНТС CIM**</span><span class="sxs-lookup"><span data-stu-id="7fd81-144">**CIM\_SoftwareFeatureSoftwareElements**</span></span>](cim-softwarefeaturesoftwareelements.md)
</dt> </dl>

 

