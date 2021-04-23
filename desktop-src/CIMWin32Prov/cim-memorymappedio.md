---
description: Класс CIM \_ меморимаппедио представляет сопоставленный в памяти ввод-вывод архитектуры компьютера. Этот класс предназначен для адресации ресурсов памяти и портов ввода-вывода.
ms.assetid: cf418cd0-1ace-4d86-a878-65e81771787e
ms.tgt_platform: multiple
title: Класс CIM_MemoryMappedIO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MemoryMappedIO
- CIM_MemoryMappedIO.Caption
- CIM_MemoryMappedIO.Description
- CIM_MemoryMappedIO.InstallDate
- CIM_MemoryMappedIO.Name
- CIM_MemoryMappedIO.Status
- CIM_MemoryMappedIO.CreationClassName
- CIM_MemoryMappedIO.CSCreationClassName
- CIM_MemoryMappedIO.CSName
- CIM_MemoryMappedIO.EndingAddress
- CIM_MemoryMappedIO.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 28ce4d60a6bba10e857afae7cc93d2e94c69b29f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072490"
---
# <a name="cim_memorymappedio-class"></a><span data-ttu-id="f3374-104">\_Класс CIM меморимаппедио</span><span class="sxs-lookup"><span data-stu-id="f3374-104">CIM\_MemoryMappedIO class</span></span>

<span data-ttu-id="f3374-105">Класс **CIM \_ меморимаппедио** представляет сопоставленный в памяти ввод-вывод архитектуры компьютера.</span><span class="sxs-lookup"><span data-stu-id="f3374-105">The **CIM\_MemoryMappedIO** class represents computer architecture memory-mapped I/O.</span></span> <span data-ttu-id="f3374-106">Этот класс предназначен для адресации ресурсов памяти и портов ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f3374-106">This class addresses memory and port I/O resources.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f3374-107">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f3374-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f3374-108">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f3374-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f3374-109">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f3374-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f3374-110">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f3374-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3374-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3374-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51B-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_MemoryMappedIO : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint64   EndingAddress;
  uint64   StartingAddress;
};
```

## <a name="members"></a><span data-ttu-id="f3374-112">Члены</span><span class="sxs-lookup"><span data-stu-id="f3374-112">Members</span></span>

<span data-ttu-id="f3374-113">Класс **CIM \_ меморимаппедио** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f3374-113">The **CIM\_MemoryMappedIO** class has these types of members:</span></span>

-   [<span data-ttu-id="f3374-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3374-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3374-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="f3374-115">Properties</span></span>

<span data-ttu-id="f3374-116">Класс **CIM \_ меморимаппедио** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="f3374-116">The **CIM\_MemoryMappedIO** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3374-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f3374-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-120">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f3374-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-121">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f3374-121">A short textual description of the object.</span></span>

<span data-ttu-id="f3374-122">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3374-123">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f3374-123">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-124">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-126">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3374-126">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3374-127">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f3374-127">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f3374-128">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f3374-128">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f3374-129">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f3374-129">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-132">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f3374-132">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f3374-133">Определение области свойства **CreationClassName** системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f3374-133">Scoping computer system's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="f3374-134">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f3374-134">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-137">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="f3374-137">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="f3374-138">Определение области для свойства **имени** системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f3374-138">Scoping computer system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="f3374-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f3374-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-142">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f3374-142">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-143">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f3374-143">A textual description of the object.</span></span>

<span data-ttu-id="f3374-144">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-144">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3374-145">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f3374-145">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-146">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3374-146">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-148">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f3374-148">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-149">Конечный адрес сопоставленного ввода-вывода памяти.</span><span class="sxs-lookup"><span data-stu-id="f3374-149">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="f3374-150">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f3374-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f3374-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f3374-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-152">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f3374-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-154">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f3374-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-155">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="f3374-155">Indicates when the object was installed.</span></span> <span data-ttu-id="f3374-156">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f3374-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f3374-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3374-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="f3374-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-161">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f3374-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-162">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f3374-162">Label by which the object is known.</span></span> <span data-ttu-id="f3374-163">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f3374-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f3374-164">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f3374-165">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="f3374-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-166">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="f3374-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-168">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="f3374-168">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-169">Начальный адрес сопоставленного в памяти ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f3374-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="f3374-170">Для свойства идентификатора ресурса оборудования необходимо задать это значение, чтобы создать сопоставленный ключ ресурса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="f3374-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="f3374-171">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="f3374-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="f3374-172">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f3374-172">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3374-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f3374-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f3374-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f3374-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f3374-175">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f3374-175">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f3374-176">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f3374-176">String that indicates the current status of the object.</span></span> <span data-ttu-id="f3374-177">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="f3374-177">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f3374-178">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="f3374-178">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f3374-179">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="f3374-179">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f3374-180">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="f3374-180">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f3374-181">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="f3374-181">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f3374-182">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f3374-182">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f3374-183">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-183">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f3374-184">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f3374-184">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f3374-185">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f3374-185">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f3374-186">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f3374-186">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f3374-187">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f3374-187">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f3374-188">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f3374-188">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f3374-189">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f3374-189">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f3374-190">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f3374-190">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f3374-191">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f3374-191">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f3374-192">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f3374-192">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f3374-193">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f3374-193">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f3374-194">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f3374-194">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f3374-195">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f3374-195">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f3374-196">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f3374-196">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="f3374-197"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f3374-197"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f3374-198">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3374-198">Remarks</span></span>

<span data-ttu-id="f3374-199">Класс **CIM \_ меморимаппедио** является производным от [**CIM \_ системресаурце**](cim-systemresource.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-199">The **CIM\_MemoryMappedIO** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span>

<span data-ttu-id="f3374-200">Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f3374-200">WMI does not implement this class.</span></span> <span data-ttu-id="f3374-201">Классы, производные от **CIM \_ меморимаппедио**, см. в разделе [Классы Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f3374-201">For classes derived from **CIM\_MemoryMappedIO**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f3374-202">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f3374-202">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f3374-203">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f3374-203">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3374-204">Требования</span><span class="sxs-lookup"><span data-stu-id="f3374-204">Requirements</span></span>



| <span data-ttu-id="f3374-205">Требование</span><span class="sxs-lookup"><span data-stu-id="f3374-205">Requirement</span></span> | <span data-ttu-id="f3374-206">Значение</span><span class="sxs-lookup"><span data-stu-id="f3374-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3374-207">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3374-207">Minimum supported client</span></span><br/> | <span data-ttu-id="f3374-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3374-208">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3374-209">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3374-209">Minimum supported server</span></span><br/> | <span data-ttu-id="f3374-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3374-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3374-211">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f3374-211">Namespace</span></span><br/>                | <span data-ttu-id="f3374-212">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3374-212">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3374-213">MOF</span><span class="sxs-lookup"><span data-stu-id="f3374-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3374-214"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3374-214"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3374-215">DLL</span><span class="sxs-lookup"><span data-stu-id="f3374-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3374-216"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3374-216"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3374-217">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f3374-217">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3374-218">**\_СИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f3374-218">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

