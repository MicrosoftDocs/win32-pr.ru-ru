---
description: '\_Зависимость АССОЦИАТЕДБАТТЕРИ CIM связывает батарею с логическим устройством. Используйте эту связь для моделирования отдельных аккумуляторов, составляющих источник бесперебойного питания (ИБП).'
ms.assetid: f8d8b3d3-edc5-438a-8be6-3ea4d765085b
ms.tgt_platform: multiple
title: Класс CIM_AssociatedBattery
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedBattery
- CIM_AssociatedBattery.Dependent
- CIM_AssociatedBattery.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 98c6394df79e53698ab6394f8572768f3728c503
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262712"
---
# <a name="cim_associatedbattery-class"></a><span data-ttu-id="a1fd6-104">\_Класс CIM ассоЦиатедбаттери</span><span class="sxs-lookup"><span data-stu-id="a1fd6-104">CIM\_AssociatedBattery class</span></span>

<span data-ttu-id="a1fd6-105">Зависимость **\_ ассоЦиатедбаттери CIM** связывает батарею с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-105">The **CIM\_AssociatedBattery** dependency associates a battery with a logical device.</span></span> <span data-ttu-id="a1fd6-106">Используйте эту связь для моделирования отдельных аккумуляторов, составляющих источник бесперебойного питания (ИБП).</span><span class="sxs-lookup"><span data-stu-id="a1fd6-106">Use this association to model individual batteries that make up an uninterruptible power supply (UPS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1fd6-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a1fd6-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a1fd6-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a1fd6-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a1fd6-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1fd6-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a1fd6-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C578-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedBattery : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Battery       REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a1fd6-112">Члены</span><span class="sxs-lookup"><span data-stu-id="a1fd6-112">Members</span></span>

<span data-ttu-id="a1fd6-113">Класс **CIM \_ ассоЦиатедбаттери** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a1fd6-113">The **CIM\_AssociatedBattery** class has these types of members:</span></span>

-   [<span data-ttu-id="a1fd6-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="a1fd6-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a1fd6-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="a1fd6-115">Properties</span></span>

<span data-ttu-id="a1fd6-116">Класс **CIM \_ ассоЦиатедбаттери** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-116">The **CIM\_AssociatedBattery** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a1fd6-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="a1fd6-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1fd6-118">Тип данных: **\_ аккумулятор CIM**</span><span class="sxs-lookup"><span data-stu-id="a1fd6-118">Data type: **CIM\_Battery**</span></span>
</dt> <dt>

<span data-ttu-id="a1fd6-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1fd6-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1fd6-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a1fd6-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a1fd6-121">[**\_ Аккумулятор CIM**](cim-battery.md) , описывающий батарею.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-121">A [**CIM\_Battery**](cim-battery.md) that describes the battery.</span></span>

</dd> <dt>

<span data-ttu-id="a1fd6-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="a1fd6-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a1fd6-123">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="a1fd6-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a1fd6-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a1fd6-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a1fd6-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="a1fd6-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a1fd6-126">[**Модель CIM \_**](cim-logicaldevice.md) , которая содержит логическое устройство, которое требуется или связано с батареей.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device needing or associated with the battery.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a1fd6-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1fd6-127">Remarks</span></span>

<span data-ttu-id="a1fd6-128">Класс **CIM \_ ассоЦиатедбаттери** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a1fd6-128">The **CIM\_AssociatedBattery** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a1fd6-129">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-129">WMI does not implement this class.</span></span> <span data-ttu-id="a1fd6-130">Дополнительные сведения о классах, производных от **CIM \_ ассоЦиатедбаттери**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a1fd6-130">For more information about classes derived from **CIM\_AssociatedBattery**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="a1fd6-131">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a1fd6-132">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="a1fd6-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1fd6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="a1fd6-133">Requirements</span></span>



| <span data-ttu-id="a1fd6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="a1fd6-134">Requirement</span></span> | <span data-ttu-id="a1fd6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="a1fd6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1fd6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1fd6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="a1fd6-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1fd6-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a1fd6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1fd6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="a1fd6-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1fd6-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a1fd6-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a1fd6-140">Namespace</span></span><br/>                | <span data-ttu-id="a1fd6-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a1fd6-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a1fd6-142">MOF</span><span class="sxs-lookup"><span data-stu-id="a1fd6-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a1fd6-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a1fd6-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a1fd6-144">DLL</span><span class="sxs-lookup"><span data-stu-id="a1fd6-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1fd6-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1fd6-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1fd6-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1fd6-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1fd6-147">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="a1fd6-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

