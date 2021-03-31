---
description: '\_Ассоциация АКТСАССПАРЕ CIM указывает, какие элементы могут быть запасными или заменить другие агрегированные элементы. Запасной элемент может действовать в &\# 0034;&0034; в режиме «горячего ожидания» \# , как указано для каждого элемента.'
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: Класс CIM_ActsAsSpare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 975c6317a78789938ea9d34e062d84fe3435498a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990672"
---
# <a name="cim_actsasspare-class"></a><span data-ttu-id="b48bf-104">\_Класс CIM актсасспаре</span><span class="sxs-lookup"><span data-stu-id="b48bf-104">CIM\_ActsAsSpare class</span></span>

<span data-ttu-id="b48bf-105">Ассоциация **\_ актсасспаре CIM** указывает, какие элементы могут быть запасными или заменить другие агрегированные элементы.</span><span class="sxs-lookup"><span data-stu-id="b48bf-105">The **CIM\_ActsAsSpare** association indicates which elements can be spares or replace other aggregated elements.</span></span> <span data-ttu-id="b48bf-106">Запасной элемент может действовать в режиме "горячего резервирования", как указано в отдельном элементе.</span><span class="sxs-lookup"><span data-stu-id="b48bf-106">A spare can operate in "hot-standby" mode as specified on an element-by-element basis.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b48bf-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="b48bf-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b48bf-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b48bf-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b48bf-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="b48bf-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b48bf-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="b48bf-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b48bf-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b48bf-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a><span data-ttu-id="b48bf-112">Члены</span><span class="sxs-lookup"><span data-stu-id="b48bf-112">Members</span></span>

<span data-ttu-id="b48bf-113">Класс **CIM \_ актсасспаре** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b48bf-113">The **CIM\_ActsAsSpare** class has these types of members:</span></span>

-   [<span data-ttu-id="b48bf-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="b48bf-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b48bf-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="b48bf-115">Properties</span></span>

<span data-ttu-id="b48bf-116">Класс **CIM \_ актсасспаре** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="b48bf-116">The **CIM\_ActsAsSpare** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b48bf-117">**Группа**</span><span class="sxs-lookup"><span data-stu-id="b48bf-117">**Group**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48bf-118">Тип данных: **CIM \_ спареграуп**</span><span class="sxs-lookup"><span data-stu-id="b48bf-118">Data type: **CIM\_SpareGroup**</span></span>
</dt> <dt>

<span data-ttu-id="b48bf-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b48bf-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b48bf-120">Ссылка на свойство **Group** , представляющее класс [**CIM \_ спареграуп**](cim-sparegroup.md) .</span><span class="sxs-lookup"><span data-stu-id="b48bf-120">Reference to the **Group** property that represents the [**CIM\_SpareGroup**](cim-sparegroup.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b48bf-121">**хотстандби**</span><span class="sxs-lookup"><span data-stu-id="b48bf-121">**HotStandby**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48bf-122">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="b48bf-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b48bf-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b48bf-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b48bf-124">Если задано **значение true**, запасной диск работает в режиме горячей замены.</span><span class="sxs-lookup"><span data-stu-id="b48bf-124">If **TRUE**, the spare is operating as a hot standby.</span></span>

</dd> <dt>

<span data-ttu-id="b48bf-125">**Перенести**</span><span class="sxs-lookup"><span data-stu-id="b48bf-125">**Spare**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b48bf-126">Тип данных: **CIM \_ манажедсистемелемент**</span><span class="sxs-lookup"><span data-stu-id="b48bf-126">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="b48bf-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="b48bf-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b48bf-128">Ссылка на управляемый системный элемент, выступающий в качестве запасного участника и участвующего в группе запчастей.</span><span class="sxs-lookup"><span data-stu-id="b48bf-128">Reference to a managed system element acting as a spare and participating in the spare group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b48bf-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b48bf-129">Remarks</span></span>

<span data-ttu-id="b48bf-130">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="b48bf-130">WMI does not implement this class.</span></span>

<span data-ttu-id="b48bf-131">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="b48bf-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b48bf-132">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="b48bf-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b48bf-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b48bf-133">Requirements</span></span>



| <span data-ttu-id="b48bf-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b48bf-134">Requirement</span></span> | <span data-ttu-id="b48bf-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b48bf-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b48bf-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b48bf-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b48bf-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b48bf-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b48bf-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b48bf-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b48bf-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b48bf-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b48bf-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b48bf-140">Namespace</span></span><br/>                | <span data-ttu-id="b48bf-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="b48bf-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b48bf-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b48bf-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b48bf-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b48bf-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b48bf-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b48bf-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b48bf-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b48bf-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b48bf-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b48bf-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b48bf-147">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="b48bf-147">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

