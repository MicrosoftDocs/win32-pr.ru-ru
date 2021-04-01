---
description: Класс CIM \_ процессексекутабле представляет связь между процессом и файлом данных и указывает, что файл участвует в выполнении процесса.
ms.assetid: 6db69bf3-b28e-4d0b-8878-558e12052767
ms.tgt_platform: multiple
title: Класс CIM_ProcessExecutable
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProcessExecutable
- CIM_ProcessExecutable.Dependent
- CIM_ProcessExecutable.Antecedent
- CIM_ProcessExecutable.BaseAddress
- CIM_ProcessExecutable.GlobalProcessCount
- CIM_ProcessExecutable.ModuleInstance
- CIM_ProcessExecutable.ProcessCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: aedb1e79ad842e4cb04746ff47bfab142a536f43
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072540"
---
# <a name="cim_processexecutable-class"></a><span data-ttu-id="befb3-103">\_Класс CIM процессексекутабле</span><span class="sxs-lookup"><span data-stu-id="befb3-103">CIM\_ProcessExecutable class</span></span>

<span data-ttu-id="befb3-104">Класс **CIM \_ процессексекутабле** представляет связь между процессом и файлом данных и указывает, что файл участвует в выполнении процесса.</span><span class="sxs-lookup"><span data-stu-id="befb3-104">The **CIM\_ProcessExecutable** class represents a link between a process and data file, and indicates that the file participates in the execution of the process.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="befb3-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="befb3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="befb3-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="befb3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="befb3-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="befb3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="befb3-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="befb3-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="befb3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="befb3-109">Syntax</span></span>

``` syntax
[Privileges("SeDebugPrivilege"), Dynamic, Provider("CIMWin32"), UUID("{8502C542-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_ProcessExecutable : CIM_Dependency
{
  CIM_Process  REF Dependent;
  CIM_DataFile REF Antecedent;
  uint64           BaseAddress;
  uint32           GlobalProcessCount;
  uint32           ModuleInstance;
  uint32           ProcessCount;
};
```

## <a name="members"></a><span data-ttu-id="befb3-110">Члены</span><span class="sxs-lookup"><span data-stu-id="befb3-110">Members</span></span>

<span data-ttu-id="befb3-111">Класс **CIM \_ процессексекутабле** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="befb3-111">The **CIM\_ProcessExecutable** class has these types of members:</span></span>

-   [<span data-ttu-id="befb3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="befb3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="befb3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="befb3-113">Properties</span></span>

<span data-ttu-id="befb3-114">Класс **CIM \_ процессексекутабле** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="befb3-114">The **CIM\_ProcessExecutable** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="befb3-115">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="befb3-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befb3-116">Тип данных: **CIM \_ File**</span><span class="sxs-lookup"><span data-stu-id="befb3-116">Data type: **CIM\_DataFile**</span></span>
</dt> <dt>

<span data-ttu-id="befb3-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="befb3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="befb3-118">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="befb3-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Antecedent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="befb3-119">[**CIM- \_ файл**](cim-datafile.md) , описывающий файл данных, участвующий в выполнении процесса.</span><span class="sxs-lookup"><span data-stu-id="befb3-119">A [**CIM\_DataFile**](cim-datafile.md) that describes the data file participating in the execution of the process.</span></span>

</dd> <dt>

<span data-ttu-id="befb3-120">**BaseAddress**</span><span class="sxs-lookup"><span data-stu-id="befb3-120">**BaseAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befb3-121">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="befb3-121">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="befb3-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="befb3-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="befb3-123">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="befb3-123">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="befb3-124">Базовый адрес модуля в адресном пространстве связанного процесса.</span><span class="sxs-lookup"><span data-stu-id="befb3-124">Base address of the module in the address space of the associated process.</span></span>

<span data-ttu-id="befb3-125">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="befb3-125">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="befb3-126">**Него**</span><span class="sxs-lookup"><span data-stu-id="befb3-126">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befb3-127">Тип данных: **\_ процесс CIM**</span><span class="sxs-lookup"><span data-stu-id="befb3-127">Data type: **CIM\_Process**</span></span>
</dt> <dt>

<span data-ttu-id="befb3-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="befb3-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="befb3-129">Квалификаторы: [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) (зависимое), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="befb3-129">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) (Dependent), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="befb3-130">[**\_ Процесс CIM**](cim-process.md) , описывающий процесс.</span><span class="sxs-lookup"><span data-stu-id="befb3-130">A [**CIM\_Process**](cim-process.md) that describes the process.</span></span>

</dd> <dt>

<span data-ttu-id="befb3-131">**глобалпроцесскаунт**</span><span class="sxs-lookup"><span data-stu-id="befb3-131">**GlobalProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befb3-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="befb3-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="befb3-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="befb3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="befb3-134">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="befb3-134">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="befb3-135">Текущее количество процессов, в которых файл загружен в память.</span><span class="sxs-lookup"><span data-stu-id="befb3-135">Current number of processes that have the file loaded in memory.</span></span>

</dd> <dt>

<span data-ttu-id="befb3-136">**модулеинстанце**</span><span class="sxs-lookup"><span data-stu-id="befb3-136">**ModuleInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befb3-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="befb3-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="befb3-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="befb3-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="befb3-139">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="befb3-139">Qualifiers: [**DEPRECATED**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="befb3-140">Маркер экземпляра Win32.</span><span class="sxs-lookup"><span data-stu-id="befb3-140">Win32 instance handle.</span></span> <span data-ttu-id="befb3-141">Это свойство является устаревшим и не имеет заменяющего значения.</span><span class="sxs-lookup"><span data-stu-id="befb3-141">This property is obsolete, and there is no replacement value.</span></span>

</dd> <dt>

<span data-ttu-id="befb3-142">**процесскаунт**</span><span class="sxs-lookup"><span data-stu-id="befb3-142">**ProcessCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befb3-143">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="befb3-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="befb3-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="befb3-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="befb3-145">Квалификаторы: [**схема**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="befb3-145">Qualifiers: [**Schema**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="befb3-146">Число ссылок на файл в связанном процессе.</span><span class="sxs-lookup"><span data-stu-id="befb3-146">Reference count of the file in the associated process.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="befb3-147">Комментарии</span><span class="sxs-lookup"><span data-stu-id="befb3-147">Remarks</span></span>

<span data-ttu-id="befb3-148">Класс **CIM \_ процессексекутабле** является производным от [**\_ зависимости CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="befb3-148">The **CIM\_ProcessExecutable** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="befb3-149">WMI реализует класс **CIM \_ процессексекутабле** .</span><span class="sxs-lookup"><span data-stu-id="befb3-149">WMI implements the **CIM\_ProcessExecutable** class.</span></span> <span data-ttu-id="befb3-150">Класс **CIM \_ процессексекутабле** является динамическим классом.</span><span class="sxs-lookup"><span data-stu-id="befb3-150">The **CIM\_ProcessExecutable** class is a dynamic class.</span></span>

<span data-ttu-id="befb3-151">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="befb3-151">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="befb3-152">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="befb3-152">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="befb3-153">Требования</span><span class="sxs-lookup"><span data-stu-id="befb3-153">Requirements</span></span>



| <span data-ttu-id="befb3-154">Требование</span><span class="sxs-lookup"><span data-stu-id="befb3-154">Requirement</span></span> | <span data-ttu-id="befb3-155">Значение</span><span class="sxs-lookup"><span data-stu-id="befb3-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="befb3-156">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="befb3-156">Minimum supported client</span></span><br/> | <span data-ttu-id="befb3-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="befb3-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="befb3-158">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="befb3-158">Minimum supported server</span></span><br/> | <span data-ttu-id="befb3-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="befb3-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="befb3-160">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="befb3-160">Namespace</span></span><br/>                | <span data-ttu-id="befb3-161">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="befb3-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="befb3-162">MOF</span><span class="sxs-lookup"><span data-stu-id="befb3-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="befb3-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="befb3-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="befb3-164">DLL</span><span class="sxs-lookup"><span data-stu-id="befb3-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="befb3-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="befb3-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befb3-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="befb3-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befb3-167">**\_Зависимость CIM**</span><span class="sxs-lookup"><span data-stu-id="befb3-167">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

