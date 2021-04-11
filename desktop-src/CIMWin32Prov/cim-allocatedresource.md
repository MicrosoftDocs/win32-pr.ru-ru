---
description: Класс CIM \_ аллокатедресаурце представляет связь между логическими устройствами и системными ресурсами и указывает, что ресурс назначен устройству.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: Класс CIM_AllocatedResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142103"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="da39f-103">\_Класс CIM аллокатедресаурце</span><span class="sxs-lookup"><span data-stu-id="da39f-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="da39f-104">Класс **CIM \_ аллокатедресаурце** представляет связь между логическими устройствами и системными ресурсами и указывает, что ресурс назначен устройству.</span><span class="sxs-lookup"><span data-stu-id="da39f-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da39f-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="da39f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="da39f-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="da39f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="da39f-107">Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="da39f-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="da39f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da39f-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="da39f-109">Члены</span><span class="sxs-lookup"><span data-stu-id="da39f-109">Members</span></span>

<span data-ttu-id="da39f-110">Класс **CIM \_ аллокатедресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="da39f-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="da39f-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="da39f-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="da39f-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="da39f-112">Properties</span></span>

<span data-ttu-id="da39f-113">Класс **CIM \_ аллокатедресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="da39f-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="da39f-114">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="da39f-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da39f-115">Тип данных: **CIM \_ системресаурце**</span><span class="sxs-lookup"><span data-stu-id="da39f-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="da39f-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="da39f-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da39f-117">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="da39f-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="da39f-118">[**\_ Системресаурце CIM**](cim-systemresource.md) , описывающий ресурс.</span><span class="sxs-lookup"><span data-stu-id="da39f-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="da39f-119">**Него**</span><span class="sxs-lookup"><span data-stu-id="da39f-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="da39f-120">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="da39f-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="da39f-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="da39f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="da39f-122">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="da39f-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="da39f-123">Логическая [**модель \_ CIM**](cim-logicaldevice.md) , которая содержит логическое устройство, которому назначен ресурс.</span><span class="sxs-lookup"><span data-stu-id="da39f-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da39f-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da39f-124">Remarks</span></span>

<span data-ttu-id="da39f-125">Класс **CIM \_ аллокатедресаурце** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="da39f-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="da39f-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="da39f-126">WMI does not implement this class.</span></span> <span data-ttu-id="da39f-127">Дополнительные сведения о классах, производных от **CIM \_ аллокатедресаурце**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="da39f-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="da39f-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="da39f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="da39f-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="da39f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="da39f-130">Требования</span><span class="sxs-lookup"><span data-stu-id="da39f-130">Requirements</span></span>



| <span data-ttu-id="da39f-131">Требование</span><span class="sxs-lookup"><span data-stu-id="da39f-131">Requirement</span></span> | <span data-ttu-id="da39f-132">Значение</span><span class="sxs-lookup"><span data-stu-id="da39f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da39f-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da39f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="da39f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="da39f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="da39f-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da39f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="da39f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="da39f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="da39f-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="da39f-137">Namespace</span></span><br/>                | <span data-ttu-id="da39f-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="da39f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="da39f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="da39f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="da39f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="da39f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="da39f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="da39f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da39f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da39f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da39f-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da39f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da39f-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="da39f-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

