---
description: '\_Абстрактный класс WMI Системмемориресаурце Win32 представляет ресурс системной памяти в компьютерной системе под Windows.'
ms.assetid: a834a1e4-f3e4-4b57-9521-98520c301016
ms.tgt_platform: multiple
title: Класс Win32_SystemMemoryResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemMemoryResource
- Win32_SystemMemoryResource.Caption
- Win32_SystemMemoryResource.Description
- Win32_SystemMemoryResource.InstallDate
- Win32_SystemMemoryResource.Name
- Win32_SystemMemoryResource.Status
- Win32_SystemMemoryResource.CreationClassName
- Win32_SystemMemoryResource.CSCreationClassName
- Win32_SystemMemoryResource.CSName
- Win32_SystemMemoryResource.EndingAddress
- Win32_SystemMemoryResource.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6064f2d983978998c47518ee50b93c3a7fedfde
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896430"
---
# <a name="win32_systemmemoryresource-class"></a><span data-ttu-id="91663-103">\_Класс Win32 системмемориресаурце</span><span class="sxs-lookup"><span data-stu-id="91663-103">Win32\_SystemMemoryResource class</span></span>

<span data-ttu-id="91663-104">Абстрактный [класс WMI](../wmisdk/retrieving-a-class.md) **\_ системмемориресаурце Win32** представляет ресурс системной памяти в компьютерной системе под Windows.</span><span class="sxs-lookup"><span data-stu-id="91663-104">The **Win32\_SystemMemoryResource** abstract [WMI class](../wmisdk/retrieving-a-class.md) represents a system memory resource on a computer system running Windows.</span></span>

<span data-ttu-id="91663-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="91663-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="91663-106">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="91663-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="91663-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="91663-107">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C4CE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemMemoryResource : CIM_MemoryMappedIO
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

## <a name="members"></a><span data-ttu-id="91663-108">Члены</span><span class="sxs-lookup"><span data-stu-id="91663-108">Members</span></span>

<span data-ttu-id="91663-109">Класс **Win32 \_ системмемориресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="91663-109">The **Win32\_SystemMemoryResource** class has these types of members:</span></span>

-   [<span data-ttu-id="91663-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="91663-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="91663-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="91663-111">Properties</span></span>

<span data-ttu-id="91663-112">Класс **Win32 \_ системмемориресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="91663-112">The **Win32\_SystemMemoryResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="91663-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="91663-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-116">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="91663-116">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="91663-117">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="91663-117">A short textual description of the object.</span></span>

<span data-ttu-id="91663-118">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91663-118">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-119">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="91663-119">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-122">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="91663-122">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="91663-123">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="91663-123">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="91663-124">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="91663-124">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="91663-125">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="91663-125">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-126">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="91663-126">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-129">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="91663-129">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="91663-130">Определение области свойства **CreationClassName** системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="91663-130">Scoping computer system's **CreationClassName** property.</span></span>

<span data-ttu-id="91663-131">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="91663-131">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-132">**CSName**</span><span class="sxs-lookup"><span data-stu-id="91663-132">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-135">Квалификаторы: [**распространяются**](../wmisdk/standard-qualifiers.md) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="91663-135">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="91663-136">Определение области для свойства **имени** системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="91663-136">Scoping computer system's **Name** property.</span></span>

<span data-ttu-id="91663-137">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="91663-137">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-138">**Описание**</span><span class="sxs-lookup"><span data-stu-id="91663-138">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-141">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="91663-141">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="91663-142">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="91663-142">A textual description of the object.</span></span>

<span data-ttu-id="91663-143">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91663-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-144">**ендингаддресс**</span><span class="sxs-lookup"><span data-stu-id="91663-144">**EndingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-145">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91663-145">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91663-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-147">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="91663-147">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="91663-148">Конечный адрес сопоставленного ввода-вывода памяти.</span><span class="sxs-lookup"><span data-stu-id="91663-148">Ending address of memory mapped I/O.</span></span>

<span data-ttu-id="91663-149">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91663-149">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="91663-150">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="91663-150">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-151">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="91663-151">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-152">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="91663-152">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="91663-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-153">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-154">Квалификаторы: [**маппингстрингс**](../wmisdk/standard-qualifiers.md) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="91663-154">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="91663-155">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="91663-155">Indicates when the object was installed.</span></span> <span data-ttu-id="91663-156">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="91663-156">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="91663-157">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91663-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="91663-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-161">Квалификаторы: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("имя")</span><span class="sxs-lookup"><span data-stu-id="91663-161">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="91663-162">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="91663-162">Label by which the object is known.</span></span> <span data-ttu-id="91663-163">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="91663-163">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="91663-164">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91663-164">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-165">**стартингаддресс**</span><span class="sxs-lookup"><span data-stu-id="91663-165">**StartingAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-166">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="91663-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="91663-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-167">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-168">Квалификаторы: [**\_ ключ CIM**](../wmisdk/standard-wmi-qualifiers.md), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("MIF. \|Сопоставленный в памяти DMTF ввод-вывод \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="91663-168">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Memory Mapped I/O\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="91663-169">Начальный адрес сопоставленного в памяти ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="91663-169">Starting address of memory mapped I/O.</span></span> <span data-ttu-id="91663-170">Для свойства идентификатора ресурса оборудования необходимо задать это значение, чтобы создать сопоставленный ключ ресурса ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="91663-170">The hardware resource identifier property should be set to this value to construct the mapped I/O resource key.</span></span>

<span data-ttu-id="91663-171">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](../wmisdk/creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="91663-171">For more information about using **uint64** values in scripts, see [Scripting in WMI](../wmisdk/creating-a-wmi-script.md).</span></span>

<span data-ttu-id="91663-172">Это свойство наследуется от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="91663-172">This property is inherited from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

</dd> <dt>

<span data-ttu-id="91663-173">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="91663-173">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="91663-174">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="91663-174">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="91663-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="91663-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="91663-176">Квалификаторы: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="91663-176">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="91663-177">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="91663-177">String that indicates the current status of the object.</span></span> <span data-ttu-id="91663-178">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="91663-178">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="91663-179">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="91663-179">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="91663-180">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="91663-180">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="91663-181">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="91663-181">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="91663-182">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="91663-182">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="91663-183">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="91663-183">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="91663-184">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="91663-184">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="91663-185">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="91663-185">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="91663-186">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="91663-186">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="91663-187">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="91663-187">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="91663-188">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="91663-188">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="91663-189">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="91663-189">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="91663-190">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="91663-190">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="91663-191">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="91663-191">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="91663-192">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="91663-192">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="91663-193">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="91663-193">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="91663-194">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="91663-194">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="91663-195">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="91663-195">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="91663-196">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="91663-196">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="91663-197">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="91663-197">**Lost Comm** ("Lost Comm")</span></span>


<span data-ttu-id="91663-198"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="91663-198"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="91663-199">Комментарии</span><span class="sxs-lookup"><span data-stu-id="91663-199">Remarks</span></span>

<span data-ttu-id="91663-200">Класс **Win32 \_ системмемориресаурце** является производным от [**CIM \_ меморимаппедио**](cim-memorymappedio.md).</span><span class="sxs-lookup"><span data-stu-id="91663-200">The **Win32\_SystemMemoryResource** class is derived from [**CIM\_MemoryMappedIO**](cim-memorymappedio.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91663-201">Требования</span><span class="sxs-lookup"><span data-stu-id="91663-201">Requirements</span></span>



| <span data-ttu-id="91663-202">Требование</span><span class="sxs-lookup"><span data-stu-id="91663-202">Requirement</span></span> | <span data-ttu-id="91663-203">Значение</span><span class="sxs-lookup"><span data-stu-id="91663-203">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="91663-204">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="91663-204">Minimum supported client</span></span><br/> | <span data-ttu-id="91663-205">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91663-205">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="91663-206">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="91663-206">Minimum supported server</span></span><br/> | <span data-ttu-id="91663-207">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91663-207">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="91663-208">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="91663-208">Namespace</span></span><br/>                | <span data-ttu-id="91663-209">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="91663-209">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="91663-210">MOF</span><span class="sxs-lookup"><span data-stu-id="91663-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="91663-211"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="91663-211"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="91663-212">DLL</span><span class="sxs-lookup"><span data-stu-id="91663-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91663-213"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91663-213"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91663-214">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="91663-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91663-215">**\_МЕМОРИМАППЕДИО CIM**</span><span class="sxs-lookup"><span data-stu-id="91663-215">**CIM\_MemoryMappedIO**</span></span>](cim-memorymappedio.md)
</dt> <dt>

[<span data-ttu-id="91663-216">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="91663-216">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

 
