---
description: '\_Класс СОПОСТАВЛЕНИЯ CIM девицеакцесседбифиле указывает логическое устройство, доступ к которому осуществляется с помощью упоминаемого \_ класса CIM девицефиле.'
ms.assetid: 8ba44f40-8b84-4f5c-b719-aded10877654
ms.tgt_platform: multiple
title: Класс CIM_DeviceAccessedByFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceAccessedByFile
- CIM_DeviceAccessedByFile.Dependent
- CIM_DeviceAccessedByFile.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cf84d2e7943dfe6da88f81ef6963190553f028e7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896037"
---
# <a name="cim_deviceaccessedbyfile-class"></a><span data-ttu-id="ba879-103">\_Класс CIM девицеакцесседбифиле</span><span class="sxs-lookup"><span data-stu-id="ba879-103">CIM\_DeviceAccessedByFile class</span></span>

<span data-ttu-id="ba879-104">Класс сопоставления **CIM \_ девицеакцесседбифиле** указывает логическое устройство, доступ к которому осуществляется с помощью упоминаемого класса [**CIM \_ девицефиле**](cim-devicefile.md) .</span><span class="sxs-lookup"><span data-stu-id="ba879-104">The **CIM\_DeviceAccessedByFile** association class specifies the logical device accessed by using the referenced [**CIM\_DeviceFile**](cim-devicefile.md) class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba879-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="ba879-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ba879-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ba879-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ba879-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="ba879-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="ba879-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="ba879-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba879-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba879-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{05D1FFF2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceAccessedByFile : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_DeviceFile    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="ba879-110">Члены</span><span class="sxs-lookup"><span data-stu-id="ba879-110">Members</span></span>

<span data-ttu-id="ba879-111">Класс **CIM \_ девицеакцесседбифиле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ba879-111">The **CIM\_DeviceAccessedByFile** class has these types of members:</span></span>

-   [<span data-ttu-id="ba879-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba879-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ba879-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="ba879-113">Properties</span></span>

<span data-ttu-id="ba879-114">Класс **CIM \_ девицеакцесседбифиле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ba879-114">The **CIM\_DeviceAccessedByFile** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ba879-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="ba879-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba879-116">Тип данных: **CIM \_ девицефиле**</span><span class="sxs-lookup"><span data-stu-id="ba879-116">Data type: **CIM\_DeviceFile**</span></span>
</dt> <dt>

<span data-ttu-id="ba879-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba879-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba879-118">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="ba879-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="ba879-119">[**\_ Девицефиле CIM**](cim-devicefile.md) , описывающий файл устройства.</span><span class="sxs-lookup"><span data-stu-id="ba879-119">A [**CIM\_DeviceFile**](cim-devicefile.md) that describes the device file.</span></span>

</dd> <dt>

<span data-ttu-id="ba879-120">**Него**</span><span class="sxs-lookup"><span data-stu-id="ba879-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ba879-121">Тип данных: **CIM \_** с типом "модель"</span><span class="sxs-lookup"><span data-stu-id="ba879-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="ba879-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ba879-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ba879-123">Квалификаторы: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="ba879-123">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="ba879-124">Логическое значение типа [**CIM \_**](cim-logicaldevice.md) , которое описывает устройство, доступ к которому осуществляется с помощью файла устройства.</span><span class="sxs-lookup"><span data-stu-id="ba879-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the device that is accessed using the device file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba879-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba879-125">Remarks</span></span>

<span data-ttu-id="ba879-126">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="ba879-126">WMI does not implement this class.</span></span>

<span data-ttu-id="ba879-127">Класс **CIM \_ девицеакцесседбифиле** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="ba879-127">The **CIM\_DeviceAccessedByFile** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="ba879-128">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="ba879-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ba879-129">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="ba879-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba879-130">Требования</span><span class="sxs-lookup"><span data-stu-id="ba879-130">Requirements</span></span>



| <span data-ttu-id="ba879-131">Требование</span><span class="sxs-lookup"><span data-stu-id="ba879-131">Requirement</span></span> | <span data-ttu-id="ba879-132">Значение</span><span class="sxs-lookup"><span data-stu-id="ba879-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba879-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba879-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ba879-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba879-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba879-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba879-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ba879-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba879-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba879-137">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ba879-137">Namespace</span></span><br/>                | <span data-ttu-id="ba879-138">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ba879-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ba879-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ba879-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ba879-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ba879-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ba879-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ba879-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba879-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba879-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba879-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba879-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba879-144">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="ba879-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

