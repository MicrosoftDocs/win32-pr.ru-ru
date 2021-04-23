---
description: '\_Класс WMI портресаурце для Win32 представляет порт ввода-вывода в компьютерной системе под Windows.'
ms.assetid: 820f4f49-571c-4044-aefc-69bac5d59e6f
ms.tgt_platform: multiple
title: Класс Win32_PortResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PortResource
- Win32_PortResource.Alias
- Win32_PortResource.Caption
- Win32_PortResource.CreationClassName
- Win32_PortResource.CSCreationClassName
- Win32_PortResource.CSName
- Win32_PortResource.Description
- Win32_PortResource.EndingAddress
- Win32_PortResource.InstallDate
- Win32_PortResource.Name
- Win32_PortResource.StartingAddress
- Win32_PortResource.Status
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e3c08424dd1aee555068c78a9308afe732634c61
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990414"
---
# <a name="win32_portresource-class"></a><span data-ttu-id="2c880-103">\_Класс Win32 портресаурце</span><span class="sxs-lookup"><span data-stu-id="2c880-103">Win32\_PortResource class</span></span>

<span data-ttu-id="2c880-104">[Класс WMI](../wmisdk/retrieving-a-class.md) **\_ портресаурце для Win32** представляет порт ввода-вывода в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="2c880-104">The **Win32\_PortResource** [WMI class](../wmisdk/retrieving-a-class.md) represents an I/O port on a computer system running Windows.</span></span>

<span data-ttu-id="2c880-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="2c880-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="2c880-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="2c880-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c880-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2c880-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_PortResource : Win32_SystemMemoryResource
{
  boolean  Alias;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   EndingAddress;
  datetime InstallDate;
  string   Name;
  uint64   StartingAddress;
  string   Status;
};
```

## <a name="members"></a><span data-ttu-id="2c880-108">Члены</span><span class="sxs-lookup"><span data-stu-id="2c880-108">Members</span></span>

<span data-ttu-id="2c880-109">Класс **Win32 \_ портресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2c880-109">The **Win32\_PortResource** class has these types of members:</span></span>

-   [<span data-ttu-id="2c880-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c880-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2c880-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="2c880-111">Properties</span></span>

<span data-ttu-id="2c880-112">Класс **Win32 \_ портресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2c880-112">The **Win32\_PortResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2c880-113">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="2c880-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-114">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="2c880-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-116">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Win32API \| Configuration Manager структурные \| \_ данные ввода-вывода")</span><span class="sxs-lookup"><span data-stu-id="2c880-116">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Configuration Manager Structures\|IO\_INFO")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-117">Если **значение — true**, этот экземпляр представляет один из диапазонов с псевдонимом.</span><span class="sxs-lookup"><span data-stu-id="2c880-117">If **TRUE**, this instance represents one of the ranges with an alias.</span></span> <span data-ttu-id="2c880-118">Если **значение равно false**, экземпляр представляет базовый адрес порта.</span><span class="sxs-lookup"><span data-stu-id="2c880-118">If **FALSE**, the instance represents a base port address.</span></span> <span data-ttu-id="2c880-119">Базовый адрес порта — это заранее определенный адрес порта, выделенный для конкретной службы или устройства.</span><span class="sxs-lookup"><span data-stu-id="2c880-119">A base port address is a predetermined port address dedicated to a specific service or device.</span></span> <span data-ttu-id="2c880-120">Адрес псевдонима порта — это порт, в ответ на который устройство отвечает, как будто оно является фактическим адресом порта ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2c880-120">A port alias address is one that a device responds to as if it were the actual address of an I/O port.</span></span>

</dd> <dt>

<span data-ttu-id="2c880-121">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="2c880-121">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-124">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="2c880-124">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-125">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2c880-125">Short description of the object.</span></span>

<span data-ttu-id="2c880-126">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-126">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-127">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2c880-127">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-130">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2c880-130">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2c880-131">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="2c880-131">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="2c880-132">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="2c880-132">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="2c880-133">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-133">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-134">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="2c880-134">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-137">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="2c880-137">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2c880-138">Имя класса создания для системы компьютера с областями.</span><span class="sxs-lookup"><span data-stu-id="2c880-138">Creation class name of the scoping computer system.</span></span>

<span data-ttu-id="2c880-139">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-139">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-140">**CSName**</span><span class="sxs-lookup"><span data-stu-id="2c880-140">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-141">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-142">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-143">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="2c880-143">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="2c880-144">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="2c880-144">Name of the scoping computer system.</span></span>

<span data-ttu-id="2c880-145">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-145">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-146">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2c880-146">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-149">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="2c880-149">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-150">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="2c880-150">Description of the object.</span></span>

<span data-ttu-id="2c880-151">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-151">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-152">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="2c880-152">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-153">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c880-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-155">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="2c880-155">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-156">Конечный адрес сопоставленного ввода-вывода памяти.</span><span class="sxs-lookup"><span data-stu-id="2c880-156">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="2c880-157">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-157">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="2c880-158">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-158">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="2c880-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-160">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2c880-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-161">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-162">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="2c880-162">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-163">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="2c880-163">Date and time the object was installed.</span></span> <span data-ttu-id="2c880-164">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="2c880-164">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="2c880-165">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="2c880-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-169">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="2c880-169">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-170">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="2c880-170">Label by which the object is known.</span></span> <span data-ttu-id="2c880-171">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="2c880-171">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="2c880-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-173">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="2c880-173">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-174">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2c880-174">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-176">Квалификаторы: [**переопределить**](../wmisdk/standard-qualifiers.md) ("стартингаддресс"), [**Key**](../wmisdk/key-qualifier.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="2c880-176">Qualifiers: [**Override**](../wmisdk/standard-qualifiers.md) ("StartingAddress"), [**Key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-177">Начальный адрес сопоставленного в памяти ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2c880-177">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="2c880-178">Для свойства идентификатора ресурса оборудования необходимо задать это значение, чтобы создать сопоставленный ключ ресурса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="2c880-178">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="2c880-179">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-179">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

<span data-ttu-id="2c880-180">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-180">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

</dd> <dt>

<span data-ttu-id="2c880-181">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="2c880-181">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2c880-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2c880-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2c880-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2c880-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2c880-184">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="2c880-184">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="2c880-185">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="2c880-185">Current status of the object.</span></span> <span data-ttu-id="2c880-186">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="2c880-186">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="2c880-187">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="2c880-187">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="2c880-188">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="2c880-188">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="2c880-189">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="2c880-189">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="2c880-190">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="2c880-190">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="2c880-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="2c880-192">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="2c880-192">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="2c880-193">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="2c880-193">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="2c880-194">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="2c880-194">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="2c880-195">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="2c880-195">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="2c880-196">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="2c880-196">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="2c880-197">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="2c880-197">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="2c880-198">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="2c880-198">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="2c880-199">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="2c880-199">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="2c880-200">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="2c880-200">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="2c880-201">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="2c880-201">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="2c880-202">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="2c880-202">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="2c880-203">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="2c880-203">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="2c880-204">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="2c880-204">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="2c880-205"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2c880-205"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="2c880-206">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2c880-206">Remarks</span></span>

<span data-ttu-id="2c880-207">Класс **Win32 \_ портресаурце** является производным от [**Win32 \_ системмемориресаурце**](win32-systemmemoryresource.md).</span><span class="sxs-lookup"><span data-stu-id="2c880-207">The **Win32\_PortResource** class is derived from [**Win32\_SystemMemoryResource**](win32-systemmemoryresource.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c880-208">Требования</span><span class="sxs-lookup"><span data-stu-id="2c880-208">Requirements</span></span>



| <span data-ttu-id="2c880-209">Требование</span><span class="sxs-lookup"><span data-stu-id="2c880-209">Requirement</span></span> | <span data-ttu-id="2c880-210">Значение</span><span class="sxs-lookup"><span data-stu-id="2c880-210">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c880-211">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2c880-211">Minimum supported client</span></span><br/> | <span data-ttu-id="2c880-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c880-212">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2c880-213">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2c880-213">Minimum supported server</span></span><br/> | <span data-ttu-id="2c880-214">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c880-214">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2c880-215">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2c880-215">Namespace</span></span><br/>                | <span data-ttu-id="2c880-216">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2c880-216">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2c880-217">MOF</span><span class="sxs-lookup"><span data-stu-id="2c880-217">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2c880-218"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2c880-218"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2c880-219">DLL</span><span class="sxs-lookup"><span data-stu-id="2c880-219">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c880-220"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c880-220"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c880-221">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2c880-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c880-222">**\_Системмемориресаурце Win32**</span><span class="sxs-lookup"><span data-stu-id="2c880-222">**Win32\_SystemMemoryResource**</span></span>](win32-systemmemoryresource.md)
</dt> <dt>

[<span data-ttu-id="2c880-223">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="2c880-223">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
