---
description: Класс CIM \_ сторажееррор представляет блоки мультимедиа или пространства памяти, которые сопоставлены неиспользуемыми из-за ошибок. Ключ класса является свойством Стартингаддресс объекта Bytes in Error.
ms.assetid: e786aa39-4718-416b-b659-bf4b8d3e2851
ms.tgt_platform: multiple
title: Класс CIM_StorageError
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageError
- CIM_StorageError.DeviceCreationClassName
- CIM_StorageError.DeviceID
- CIM_StorageError.EndingAddress
- CIM_StorageError.StartingAddress
- CIM_StorageError.SystemCreationClassName
- CIM_StorageError.SystemName
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6f5b197a5c82e61e054f5875fad466cac808ec38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655754"
---
# <a name="cim_storageerror-class"></a><span data-ttu-id="467e8-104">\_Класс CIM сторажееррор</span><span class="sxs-lookup"><span data-stu-id="467e8-104">CIM\_StorageError class</span></span>

<span data-ttu-id="467e8-105">Класс **CIM \_ сторажееррор** представляет блоки мультимедиа или пространства памяти, которые сопоставлены неиспользуемыми из-за ошибок.</span><span class="sxs-lookup"><span data-stu-id="467e8-105">The **CIM\_StorageError** class represents blocks of media or memory space that are mapped out-of-use due to errors.</span></span> <span data-ttu-id="467e8-106">Ключ класса является свойством **стартингаддресс** объекта Bytes in Error.</span><span class="sxs-lookup"><span data-stu-id="467e8-106">The key of the class is the **StartingAddress** property of the bytes in error.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="467e8-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="467e8-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="467e8-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="467e8-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="467e8-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="467e8-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="467e8-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="467e8-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="467e8-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="467e8-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{71312AB6-DB31-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_StorageError
{
  string DeviceCreationClassName;
  string DeviceID;
  uint64 EndingAddress;
  uint64 StartingAddress;
  string SystemCreationClassName;
  string SystemName;
};
```

## <a name="members"></a><span data-ttu-id="467e8-112">Члены</span><span class="sxs-lookup"><span data-stu-id="467e8-112">Members</span></span>

<span data-ttu-id="467e8-113">Класс **CIM \_ сторажееррор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="467e8-113">The **CIM\_StorageError** class has these types of members:</span></span>

-   [<span data-ttu-id="467e8-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="467e8-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="467e8-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="467e8-115">Properties</span></span>

<span data-ttu-id="467e8-116">Класс **CIM \_ сторажееррор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="467e8-116">The **CIM\_StorageError** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="467e8-117">**девицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="467e8-117">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467e8-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="467e8-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="467e8-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="467e8-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467e8-120">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**CreationClassName**")</span><span class="sxs-lookup"><span data-stu-id="467e8-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**CreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="467e8-121">Определение области действия имени класса для создания экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="467e8-121">Scoping storage extent's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="467e8-122">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="467e8-122">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467e8-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="467e8-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="467e8-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="467e8-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467e8-125">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**DeviceID**)</span><span class="sxs-lookup"><span data-stu-id="467e8-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**DeviceID**")</span></span>
</dt> </dl>

<span data-ttu-id="467e8-126">Определение области идентификатора устройства для экстента хранения.</span><span class="sxs-lookup"><span data-stu-id="467e8-126">Scoping storage extent's device identifier.</span></span>

</dd> <dt>

<span data-ttu-id="467e8-127">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="467e8-127">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467e8-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="467e8-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="467e8-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="467e8-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="467e8-130">Конечный адрес байт в ошибке.</span><span class="sxs-lookup"><span data-stu-id="467e8-130">Ending address of the bytes in error.</span></span>

<span data-ttu-id="467e8-131">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="467e8-131">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="467e8-132">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="467e8-132">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467e8-133">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="467e8-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="467e8-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="467e8-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467e8-135">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="467e8-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="467e8-136">Начальный адрес байт в ошибке.</span><span class="sxs-lookup"><span data-stu-id="467e8-136">Starting address of the bytes in error.</span></span>

<span data-ttu-id="467e8-137">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="467e8-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="467e8-138">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="467e8-138">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467e8-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="467e8-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="467e8-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="467e8-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467e8-141">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**Системкреатионкласснаме**")</span><span class="sxs-lookup"><span data-stu-id="467e8-141">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemCreationClassName**")</span></span>
</dt> </dl>

<span data-ttu-id="467e8-142">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="467e8-142">Scoping system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="467e8-143">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="467e8-143">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467e8-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="467e8-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="467e8-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="467e8-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="467e8-146">Квалификаторы: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**распространяемый**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ сторажеекстент**](cim-storageextent.md).**SystemName**")</span><span class="sxs-lookup"><span data-stu-id="467e8-146">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_StorageExtent**](cim-storageextent.md).**SystemName**")</span></span>
</dt> </dl>

<span data-ttu-id="467e8-147">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="467e8-147">Scoping system's name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="467e8-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="467e8-148">Remarks</span></span>

<span data-ttu-id="467e8-149">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="467e8-149">WMI does not implement this class.</span></span>

<span data-ttu-id="467e8-150">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="467e8-150">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="467e8-151">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="467e8-151">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="467e8-152">Требования</span><span class="sxs-lookup"><span data-stu-id="467e8-152">Requirements</span></span>



| <span data-ttu-id="467e8-153">Требование</span><span class="sxs-lookup"><span data-stu-id="467e8-153">Requirement</span></span> | <span data-ttu-id="467e8-154">Значение</span><span class="sxs-lookup"><span data-stu-id="467e8-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="467e8-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="467e8-155">Minimum supported client</span></span><br/> | <span data-ttu-id="467e8-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="467e8-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="467e8-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="467e8-157">Minimum supported server</span></span><br/> | <span data-ttu-id="467e8-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="467e8-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="467e8-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="467e8-159">Namespace</span></span><br/>                | <span data-ttu-id="467e8-160">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="467e8-160">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="467e8-161">MOF</span><span class="sxs-lookup"><span data-stu-id="467e8-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="467e8-162"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="467e8-162"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="467e8-163">DLL</span><span class="sxs-lookup"><span data-stu-id="467e8-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="467e8-164"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="467e8-164"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

