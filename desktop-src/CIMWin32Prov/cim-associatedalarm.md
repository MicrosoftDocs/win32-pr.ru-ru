---
description: '\_Зависимость АССОЦИАТЕДАЛАРМ CIM связывает сигнал с логическим устройством.'
ms.assetid: ed0ccc81-6d1b-45b0-abf0-7a2bd9a50193
ms.tgt_platform: multiple
title: Класс CIM_AssociatedAlarm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedAlarm
- CIM_AssociatedAlarm.Dependent
- CIM_AssociatedAlarm.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fe6a637482526feecc7528eadc70dc695dafca9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807679"
---
# <a name="cim_associatedalarm-class"></a><span data-ttu-id="234ae-103">\_Класс CIM ассоЦиатедаларм</span><span class="sxs-lookup"><span data-stu-id="234ae-103">CIM\_AssociatedAlarm class</span></span>

<span data-ttu-id="234ae-104">Зависимость **\_ ассоЦиатедаларм CIM** связывает сигнал с логическим устройством.</span><span class="sxs-lookup"><span data-stu-id="234ae-104">The **CIM\_AssociatedAlarm** dependency associates an alarm with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="234ae-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="234ae-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="234ae-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="234ae-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="234ae-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="234ae-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="234ae-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="234ae-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{2280CB02-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AssociatedAlarm : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_AlarmDevice   REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="234ae-109">Члены</span><span class="sxs-lookup"><span data-stu-id="234ae-109">Members</span></span>

<span data-ttu-id="234ae-110">Класс **CIM \_ ассоЦиатедаларм** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="234ae-110">The **CIM\_AssociatedAlarm** class has these types of members:</span></span>

-   [<span data-ttu-id="234ae-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="234ae-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="234ae-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="234ae-112">Properties</span></span>

<span data-ttu-id="234ae-113">Класс **CIM \_ ассоЦиатедаларм** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="234ae-113">The **CIM\_AssociatedAlarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="234ae-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="234ae-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234ae-115">Тип данных: **CIM \_ алармдевице**</span><span class="sxs-lookup"><span data-stu-id="234ae-115">Data type: **CIM\_AlarmDevice**</span></span>
</dt> <dt>

<span data-ttu-id="234ae-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234ae-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234ae-117">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="234ae-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="234ae-118">[**\_ Алармдевице CIM**](cim-alarmdevice.md) , содержащий сигнальное устройство.</span><span class="sxs-lookup"><span data-stu-id="234ae-118">A [**CIM\_AlarmDevice**](cim-alarmdevice.md) that contains the alarm device.</span></span>

</dd> <dt>

<span data-ttu-id="234ae-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="234ae-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="234ae-120">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="234ae-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="234ae-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="234ae-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="234ae-122">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="234ae-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="234ae-123">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , которая содержит логическое устройство с оповещением.</span><span class="sxs-lookup"><span data-stu-id="234ae-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device that is alarmed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="234ae-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="234ae-124">Remarks</span></span>

<span data-ttu-id="234ae-125">Класс **CIM \_ ассоЦиатедаларм** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="234ae-125">The **CIM\_AssociatedAlarm** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="234ae-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="234ae-126">WMI does not implement this class.</span></span>

<span data-ttu-id="234ae-127">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="234ae-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="234ae-128">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="234ae-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="234ae-129">Требования</span><span class="sxs-lookup"><span data-stu-id="234ae-129">Requirements</span></span>



| <span data-ttu-id="234ae-130">Требование</span><span class="sxs-lookup"><span data-stu-id="234ae-130">Requirement</span></span> | <span data-ttu-id="234ae-131">Значение</span><span class="sxs-lookup"><span data-stu-id="234ae-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="234ae-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="234ae-132">Minimum supported client</span></span><br/> | <span data-ttu-id="234ae-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="234ae-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="234ae-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="234ae-134">Minimum supported server</span></span><br/> | <span data-ttu-id="234ae-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="234ae-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="234ae-136">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="234ae-136">Namespace</span></span><br/>                | <span data-ttu-id="234ae-137">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="234ae-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="234ae-138">MOF</span><span class="sxs-lookup"><span data-stu-id="234ae-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="234ae-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="234ae-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="234ae-140">DLL</span><span class="sxs-lookup"><span data-stu-id="234ae-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="234ae-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="234ae-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="234ae-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="234ae-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="234ae-143">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="234ae-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

