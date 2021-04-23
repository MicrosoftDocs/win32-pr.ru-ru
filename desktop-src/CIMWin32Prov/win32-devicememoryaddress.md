---
description: '\_Класс WMI девицемеморяддресс для Win32 представляет адрес памяти устройства в компьютерной системе под Windows.'
ms.assetid: f0a70724-5ced-47fe-b17e-e153e65b80df
ms.tgt_platform: multiple
title: Класс Win32_DeviceMemoryAddress
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aa7472e3c20808ff52f6f45b0dca57fd19f9dd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990700"
---
# <a name="win32_devicememoryaddress-class"></a><span data-ttu-id="a477e-103">\_Класс Win32 девицемеморяддресс</span><span class="sxs-lookup"><span data-stu-id="a477e-103">Win32\_DeviceMemoryAddress class</span></span>

<span data-ttu-id="a477e-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ девицемеморяддресс для Win32** представляет адрес памяти устройства в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="a477e-104">The **Win32\_DeviceMemoryAddress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a device memory address on a computer system running Windows.</span></span>

<span data-ttu-id="a477e-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="a477e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a477e-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="a477e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a477e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a477e-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4CF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceMemoryAddress : Win32_SystemMemoryResource
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   MemoryType;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="a477e-108">Члены</span><span class="sxs-lookup"><span data-stu-id="a477e-108">Members</span></span>

<span data-ttu-id="a477e-109">Класс **Win32 \_ девицемеморяддресс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a477e-109">The **Win32\_DeviceMemoryAddress** class has these types of members:</span></span>

-   [<span data-ttu-id="a477e-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="a477e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a477e-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="a477e-111">Properties</span></span>

<span data-ttu-id="a477e-112">Класс **Win32 \_ девицемеморяддресс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="a477e-112">The **Win32\_DeviceMemoryAddress** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a477e-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="a477e-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-116">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="a477e-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-117">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="a477e-117">Short description of the object a one-line string.</span></span>

<span data-ttu-id="a477e-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="a477e-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-122">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a477e-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a477e-123">Имя первого конкретного класса, который отображается в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="a477e-123">Name of the first concrete class that appears in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="a477e-124">При использовании с другими ключевыми свойствами класса свойство позволяет уникально идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="a477e-124">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be identified uniquely.</span></span>

<span data-ttu-id="a477e-125">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-126">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="a477e-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-129">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="a477e-129">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a477e-130">Имя класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="a477e-130">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="a477e-131">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="a477e-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-135">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a477e-135">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a477e-136">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="a477e-136">Name of the scoping computer system.</span></span>

<span data-ttu-id="a477e-137">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a477e-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-141">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="a477e-141">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-142">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="a477e-142">Description of the object.</span></span>

<span data-ttu-id="a477e-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-144">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="a477e-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-145">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a477e-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-147">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="a477e-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-148">Конечный адрес сопоставленного в памяти ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a477e-148">Ending address of memory-mapped I/O.</span></span>

<span data-ttu-id="a477e-149">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-149">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="a477e-150">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a477e-150">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a477e-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-152">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a477e-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-154">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="a477e-154">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-155">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="a477e-155">Date and time the object was installed.</span></span> <span data-ttu-id="a477e-156">Для этого свойства не требуется указывать значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="a477e-156">This property does not require a value to indicate that the object is installed.</span></span>

<span data-ttu-id="a477e-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-158">**меморитипе**</span><span class="sxs-lookup"><span data-stu-id="a477e-158">**MemoryType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-161">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| системструктурес \| cm \_ partial \_ Resource \_ \| Flags")</span><span class="sxs-lookup"><span data-stu-id="a477e-161">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|SystemStructures\|CM\_PARTIAL\_RESOURCE\_DESCRIPTOR\|Flags")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-162">Характеристики ресурса памяти в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="a477e-162">Characteristics of the memory resource on the computer system running Windows.</span></span> <span data-ttu-id="a477e-163">Ниже приведены значения.</span><span class="sxs-lookup"><span data-stu-id="a477e-163">Values are the following.</span></span>

<dt>

<span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>

<span data-ttu-id="a477e-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span><span class="sxs-lookup"><span data-stu-id="a477e-164"><span id="ReadWrite"></span><span id="readwrite"></span><span id="READWRITE"></span>**ReadWrite** ("ReadWrite")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-165">Память может считываться и записываться.</span><span class="sxs-lookup"><span data-stu-id="a477e-165">The memory can be both read and written.</span></span>

</dd> <dt>

<span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>

<span data-ttu-id="a477e-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** (ReadOnly)</span><span class="sxs-lookup"><span data-stu-id="a477e-166"><span id="ReadOnly"></span><span id="readonly"></span><span id="READONLY"></span>**ReadOnly** ("ReadOnly")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-167">Память доступна только для чтения.</span><span class="sxs-lookup"><span data-stu-id="a477e-167">The memory is read-only.</span></span>

</dd> <dt>

<span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>

<span data-ttu-id="a477e-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span><span class="sxs-lookup"><span data-stu-id="a477e-168"><span id="WriteOnly"></span><span id="writeonly"></span><span id="WRITEONLY"></span>**WriteOnly** ("WriteOnly")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-169">Память может быть записана только.</span><span class="sxs-lookup"><span data-stu-id="a477e-169">The memory can only be written.</span></span>

</dd> <dt>

<span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>

<span data-ttu-id="a477e-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Предзагрузка** ("с предвыборкой")</span><span class="sxs-lookup"><span data-stu-id="a477e-170"><span id="Prefetchable"></span><span id="prefetchable"></span><span id="PREFETCHABLE"></span>**Prefetchable** ("Prefetchable")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-171">Блок памяти копируется из основной памяти в небольшой буфер, управляемый набором микросхем памяти.</span><span class="sxs-lookup"><span data-stu-id="a477e-171">A block of memory is copied from main memory into a small buffer managed by the memory chipset.</span></span> <span data-ttu-id="a477e-172">Повторные операции чтения из одной и той же части памяти выполняются быстрее с использованием памяти с предвыборкой.</span><span class="sxs-lookup"><span data-stu-id="a477e-172">Repeated read operations from the same part of memory are faster with prefetchable memory.</span></span>

</dd> <dt>

<span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>

<span data-ttu-id="a477e-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**Комбинедврите** ("комбинедврите")</span><span class="sxs-lookup"><span data-stu-id="a477e-173"><span id="CombinedWrite"></span><span id="combinedwrite"></span><span id="COMBINEDWRITE"></span>**CombinedWrite** ("CombinedWrite")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-174">TBD</span><span class="sxs-lookup"><span data-stu-id="a477e-174">TBD</span></span>

</dd> <dt>

<span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>

<span data-ttu-id="a477e-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span><span class="sxs-lookup"><span data-stu-id="a477e-175"><span id="Type24"></span><span id="type24"></span><span id="TYPE24"></span>**Type24** ("Type24")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-176">TBD</span><span class="sxs-lookup"><span data-stu-id="a477e-176">TBD</span></span>

</dd> <dt>

<span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>

<span data-ttu-id="a477e-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Кэширование** ("кэшируется")</span><span class="sxs-lookup"><span data-stu-id="a477e-177"><span id="Cacheable"></span><span id="cacheable"></span><span id="CACHEABLE"></span>**Cacheable** ("Cacheable")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-178">TBD</span><span class="sxs-lookup"><span data-stu-id="a477e-178">TBD</span></span>

</dd> <dt>

<span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>

<span data-ttu-id="a477e-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**Виндовдекоде** ("виндовдекоде")</span><span class="sxs-lookup"><span data-stu-id="a477e-179"><span id="WindowDecode"></span><span id="windowdecode"></span><span id="WINDOWDECODE"></span>**WindowDecode** ("WindowDecode")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-180">TBD</span><span class="sxs-lookup"><span data-stu-id="a477e-180">TBD</span></span>

</dd> <dt>

<span id="Bar"></span><span id="bar"></span><span id="BAR"></span>

<span data-ttu-id="a477e-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Линейчатая** ("линейчатая")</span><span class="sxs-lookup"><span data-stu-id="a477e-181"><span id="Bar"></span><span id="bar"></span><span id="BAR"></span>**Bar** ("Bar")</span></span>


</dt> <dd>

<span data-ttu-id="a477e-182">TBD</span><span class="sxs-lookup"><span data-stu-id="a477e-182">TBD</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="a477e-183">**Name**</span><span class="sxs-lookup"><span data-stu-id="a477e-183">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-185">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-186">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="a477e-186">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-187">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="a477e-187">Label by which the object is known.</span></span> <span data-ttu-id="a477e-188">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="a477e-188">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="a477e-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-190">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="a477e-190">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-191">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a477e-191">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-192">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-193">Квалификаторы: [**переопределить**](/windows/desktop/WmiSdk/standard-qualifiers) ("стартингаддресс"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="a477e-193">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartingAddress"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-194">Начальный адрес сопоставленного в памяти ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a477e-194">Starting address of memory-mapped I/O.</span></span> <span data-ttu-id="a477e-195">Для свойства идентификатора ресурса оборудования необходимо задать это значение, чтобы создать сопоставленный ключ ресурса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="a477e-195">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="a477e-196">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-196">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="a477e-197">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="a477e-197">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="a477e-198">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="a477e-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a477e-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="a477e-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a477e-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="a477e-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a477e-201">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="a477e-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="a477e-202">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="a477e-202">Current status of the object.</span></span> <span data-ttu-id="a477e-203">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="a477e-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a477e-204">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="a477e-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a477e-205">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="a477e-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a477e-206">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="a477e-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a477e-207">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="a477e-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a477e-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="a477e-209">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="a477e-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="a477e-210">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="a477e-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="a477e-211">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="a477e-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="a477e-212">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="a477e-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a477e-213">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="a477e-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="a477e-214">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="a477e-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="a477e-215">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="a477e-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="a477e-216">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="a477e-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="a477e-217">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="a477e-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="a477e-218">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="a477e-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="a477e-219">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="a477e-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="a477e-220">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="a477e-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="a477e-221">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="a477e-221">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="a477e-222"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a477e-222"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="a477e-223">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a477e-223">Remarks</span></span>

<span data-ttu-id="a477e-224">Класс **Win32 \_ девицемеморяддресс** является производным от [**Win32 \_ системмемориресаурце**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="a477e-224">The **Win32\_DeviceMemoryAddress** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a477e-225">Требования</span><span class="sxs-lookup"><span data-stu-id="a477e-225">Requirements</span></span>



| <span data-ttu-id="a477e-226">Требование</span><span class="sxs-lookup"><span data-stu-id="a477e-226">Requirement</span></span> | <span data-ttu-id="a477e-227">Значение</span><span class="sxs-lookup"><span data-stu-id="a477e-227">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a477e-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a477e-228">Minimum supported client</span></span><br/> | <span data-ttu-id="a477e-229">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a477e-229">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a477e-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a477e-230">Minimum supported server</span></span><br/> | <span data-ttu-id="a477e-231">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a477e-231">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a477e-232">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="a477e-232">Namespace</span></span><br/>                | <span data-ttu-id="a477e-233">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a477e-233">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a477e-234">MOF</span><span class="sxs-lookup"><span data-stu-id="a477e-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a477e-235"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a477e-235"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a477e-236">DLL</span><span class="sxs-lookup"><span data-stu-id="a477e-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a477e-237"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a477e-237"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a477e-238">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a477e-238">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a477e-239">**\_Системмемориресаурце Win32**</span><span class="sxs-lookup"><span data-stu-id="a477e-239">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="a477e-240">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="a477e-240">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

