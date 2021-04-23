---
description: Класс CIM \_ сеттингконтекст связывает объекты конфигурации с объектами Setting.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Класс CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 867be99e1630f02c0163516ad7a86cf84c2fac13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990456"
---
# <a name="cim_settingcontext-class"></a><span data-ttu-id="e8e1f-103">\_Класс CIM сеттингконтекст</span><span class="sxs-lookup"><span data-stu-id="e8e1f-103">CIM\_SettingContext class</span></span>

<span data-ttu-id="e8e1f-104">Класс **CIM \_ сеттингконтекст** связывает объекты конфигурации с объектами Setting.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-104">The **CIM\_SettingContext** class associates configuration objects with setting objects.</span></span> <span data-ttu-id="e8e1f-105">Например, параметры сетевого адаптера могут измениться в зависимости от сайта или сети, к которой подключена система компьютера, на котором он размещен.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-105">For example, a network adapter's settings could change based on the site or network to which its hosting computer system is attached.</span></span> <span data-ttu-id="e8e1f-106">В этом случае компьютерная система будет иметь два различных объекта конфигурации, соответствующие различиям в конфигурации сети для двух сегментов сети.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-106">In which case, the computer system would have two different configuration objects, corresponding to the differences in network configuration for the two network segments.</span></span> <span data-ttu-id="e8e1f-107">При использовании одной конфигурации объект параметра для сетевого адаптера будет агрегирован при работе в одном сегменте. в то же время другая конфигурация будет выполнять статистическую обработку другого объекта параметра сетевого адаптера, относящегося к другому сегменту.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-107">One configuration would aggregate a setting object for the network adapter when operating on one segment; whereas, the other configuration would aggregate a different network adapter setting object, specific to another segment.</span></span> <span data-ttu-id="e8e1f-108">Обратите внимание, что многие параметры компьютера не зависят от конфигурации сети.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-108">Note that many computer settings are independent of the network configuration.</span></span> <span data-ttu-id="e8e1f-109">Например, обе конфигурации будут вычислять один и тот же объект параметра для разрешения монитора компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-109">For example, both configurations would aggregate the same setting object for the computer system's monitor resolution.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e8e1f-110">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-110">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e8e1f-111">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e8e1f-111">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e8e1f-112">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-112">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e8e1f-113">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-113">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e1f-114">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8e1f-114">Syntax</span></span>

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="e8e1f-115">Члены</span><span class="sxs-lookup"><span data-stu-id="e8e1f-115">Members</span></span>

<span data-ttu-id="e8e1f-116">Класс **CIM \_ сеттингконтекст** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e8e1f-116">The **CIM\_SettingContext** class has these types of members:</span></span>

-   [<span data-ttu-id="e8e1f-117">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8e1f-117">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e8e1f-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="e8e1f-118">Properties</span></span>

<span data-ttu-id="e8e1f-119">Класс **CIM \_ сеттингконтекст** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-119">The **CIM\_SettingContext** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e8e1f-120">**Контекст**</span><span class="sxs-lookup"><span data-stu-id="e8e1f-120">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8e1f-121">Тип данных: **\_ Конфигурация CIM**</span><span class="sxs-lookup"><span data-stu-id="e8e1f-121">Data type: **CIM\_Configuration**</span></span>
</dt> <dt>

<span data-ttu-id="e8e1f-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8e1f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e8e1f-123">Квалификаторы: [ **Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e8e1f-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e8e1f-124">Ссылка на объект конфигурации, который выполняет статистическую обработку параметра.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-124">Reference to the configuration object that aggregates the setting.</span></span>

</dd> <dt>

<span data-ttu-id="e8e1f-125">**Параметр**</span><span class="sxs-lookup"><span data-stu-id="e8e1f-125">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e8e1f-126">Тип данных: **\_ параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="e8e1f-126">Data type: **CIM\_Setting**</span></span>
</dt> <dt>

<span data-ttu-id="e8e1f-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e8e1f-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e8e1f-128">Ссылка на агрегированный параметр.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-128">Reference to an aggregated setting.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e8e1f-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e8e1f-129">Remarks</span></span>

<span data-ttu-id="e8e1f-130">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-130">WMI does not implement this class.</span></span>

<span data-ttu-id="e8e1f-131">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e8e1f-132">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e8e1f-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e1f-133">Требования</span><span class="sxs-lookup"><span data-stu-id="e8e1f-133">Requirements</span></span>



| <span data-ttu-id="e8e1f-134">Требование</span><span class="sxs-lookup"><span data-stu-id="e8e1f-134">Requirement</span></span> | <span data-ttu-id="e8e1f-135">Значение</span><span class="sxs-lookup"><span data-stu-id="e8e1f-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e1f-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e8e1f-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e1f-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8e1f-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e8e1f-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e8e1f-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e1f-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8e1f-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e8e1f-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e8e1f-140">Namespace</span></span><br/>                | <span data-ttu-id="e8e1f-141">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="e8e1f-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e8e1f-142">MOF</span><span class="sxs-lookup"><span data-stu-id="e8e1f-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8e1f-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1f-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8e1f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="e8e1f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8e1f-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8e1f-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

