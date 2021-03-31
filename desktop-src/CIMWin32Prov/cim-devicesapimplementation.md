---
description: Класс CIM \_ девицесапимплементатион представляет связь между точкой доступа к службе (SAP) и ее реализацией.
ms.assetid: 6c059507-bfc0-4630-9b39-9c4bae2bf138
ms.tgt_platform: multiple
title: Класс CIM_DeviceSAPImplementation (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSAPImplementation
- CIM_DeviceSAPImplementation.Dependent
- CIM_DeviceSAPImplementation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eadc1e42427c06717c7b0d7a13aba8a2a71ccddb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807673"
---
# <a name="cim_devicesapimplementation-class-cimwin32-wmi-providers"></a><span data-ttu-id="ad493-103">Класс CIM_DeviceSAPImplementation (поставщики WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="ad493-103">CIM_DeviceSAPImplementation class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="ad493-104">Класс **CIM \_ девицесапимплементатион** представляет связь между точкой доступа к службе (SAP) и ее реализацией.</span><span class="sxs-lookup"><span data-stu-id="ad493-104">The **CIM\_DeviceSAPImplementation** class represents an association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="ad493-105">Если с одним SAP связано много логических устройств, они работают совместно, чтобы предоставить точку доступа.</span><span class="sxs-lookup"><span data-stu-id="ad493-105">When many logical devices are associated with one SAP, the elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="ad493-106">При наличии различных реализаций SAP каждая реализация приводит к отдельным экземплярам объекта SAP.</span><span class="sxs-lookup"><span data-stu-id="ad493-106">If different implementations of a SAP exist, each implementation results in individual instantiations of the SAP object.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ad493-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ad493-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ad493-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ad493-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ad493-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ad493-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ad493-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ad493-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad493-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ad493-111">Syntax</span></span>

``` syntax
[UUID("{1BE949DA-DB36-11d2-85FC-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_DeviceSAPImplementation : CIM_Dependency
{
  CIM_ServiceAccessPoint REF Dependent;
  CIM_LogicalDevice      REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ad493-112">Члены</span><span class="sxs-lookup"><span data-stu-id="ad493-112">Members</span></span>

<span data-ttu-id="ad493-113">Класс **CIM \_ девицесапимплементатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ad493-113">The **CIM\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="ad493-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad493-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ad493-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="ad493-115">Properties</span></span>

<span data-ttu-id="ad493-116">Класс **CIM \_ девицесапимплементатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ad493-116">The **CIM\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ad493-117">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="ad493-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad493-118">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="ad493-118">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ad493-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad493-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad493-120">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ad493-120">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ad493-121">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , описывающая логическое устройство.</span><span class="sxs-lookup"><span data-stu-id="ad493-121">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="ad493-122">**Него**</span><span class="sxs-lookup"><span data-stu-id="ad493-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ad493-123">Тип данных: **CIM \_ сервицеакцесспоинт**</span><span class="sxs-lookup"><span data-stu-id="ad493-123">Data type: **CIM\_ServiceAccessPoint**</span></span>
</dt> <dt>

<span data-ttu-id="ad493-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ad493-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ad493-125">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="ad493-125">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ad493-126">[**\_ Сервицеакцесспоинт CIM**](cim-serviceaccesspoint.md) , описывающий точку доступа к службе, реализованную с помощью логического устройства.</span><span class="sxs-lookup"><span data-stu-id="ad493-126">A [**CIM\_ServiceAccessPoint**](cim-serviceaccesspoint.md) that describes the service access point implemented using the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ad493-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ad493-127">Remarks</span></span>

<span data-ttu-id="ad493-128">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ad493-128">WMI does not implement this class.</span></span>

<span data-ttu-id="ad493-129">Класс **CIM \_ девицесапимплементатион** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ad493-129">The **CIM\_DeviceSAPImplementation** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ad493-130">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ad493-130">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ad493-131">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ad493-131">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad493-132">Требования</span><span class="sxs-lookup"><span data-stu-id="ad493-132">Requirements</span></span>



| <span data-ttu-id="ad493-133">Требование</span><span class="sxs-lookup"><span data-stu-id="ad493-133">Requirement</span></span> | <span data-ttu-id="ad493-134">Значение</span><span class="sxs-lookup"><span data-stu-id="ad493-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad493-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ad493-135">Minimum supported client</span></span><br/> | <span data-ttu-id="ad493-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ad493-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ad493-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ad493-137">Minimum supported server</span></span><br/> | <span data-ttu-id="ad493-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ad493-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ad493-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ad493-139">Namespace</span></span><br/>                | <span data-ttu-id="ad493-140">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ad493-140">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ad493-141">MOF</span><span class="sxs-lookup"><span data-stu-id="ad493-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ad493-142"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ad493-142"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ad493-143">DLL</span><span class="sxs-lookup"><span data-stu-id="ad493-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad493-144"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad493-144"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad493-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ad493-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad493-146">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="ad493-146">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

