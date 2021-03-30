---
description: Класс CIM \_ IRQ представляет линию запроса на прерывание архитектуры Intel (IRQ).
ms.assetid: d72d4914-c57b-496d-a9fe-d8f5b522504c
ms.tgt_platform: multiple
title: Класс CIM_IRQ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_IRQ
- CIM_IRQ.Caption
- CIM_IRQ.Description
- CIM_IRQ.InstallDate
- CIM_IRQ.Name
- CIM_IRQ.Status
- CIM_IRQ.Availability
- CIM_IRQ.CreationClassName
- CIM_IRQ.CSCreationClassName
- CIM_IRQ.CSName
- CIM_IRQ.IRQNumber
- CIM_IRQ.Shareable
- CIM_IRQ.TriggerLevel
- CIM_IRQ.TriggerType
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 03a336caa02c766160fe6501f91b28f06a872ecb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896014"
---
# <a name="cim_irq-class"></a><span data-ttu-id="f11de-103">\_Класс IRQ CIM</span><span class="sxs-lookup"><span data-stu-id="f11de-103">CIM\_IRQ class</span></span>

<span data-ttu-id="f11de-104">Класс **CIM \_ IRQ** представляет линию запроса на прерывание архитектуры Intel (IRQ).</span><span class="sxs-lookup"><span data-stu-id="f11de-104">The **CIM\_IRQ** class represents an Intel architecture interrupt request line (IRQ).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f11de-105">Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI.</span><span class="sxs-lookup"><span data-stu-id="f11de-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f11de-106">В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f11de-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f11de-107">Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="f11de-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f11de-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="f11de-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f11de-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f11de-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C51A-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_IRQ : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  uint16   Availability;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  uint32   IRQNumber;
  boolean  Shareable;
  uint16   TriggerLevel;
  uint16   TriggerType;
};
```

## <a name="members"></a><span data-ttu-id="f11de-110">Члены</span><span class="sxs-lookup"><span data-stu-id="f11de-110">Members</span></span>

<span data-ttu-id="f11de-111">Класс **\_ IRQ CIM** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f11de-111">The **CIM\_IRQ** class has these types of members:</span></span>

-   [<span data-ttu-id="f11de-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="f11de-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f11de-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f11de-113">Properties</span></span>

<span data-ttu-id="f11de-114">Класс **\_ IRQ CIM** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="f11de-114">The **CIM\_IRQ** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f11de-115">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="f11de-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f11de-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ 001,2 (DMTF \| )</span><span class="sxs-lookup"><span data-stu-id="f11de-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-119">Доступность IRQ.</span><span class="sxs-lookup"><span data-stu-id="f11de-119">Availability of the IRQ.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f11de-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f11de-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f11de-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f11de-121"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="f11de-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Доступно** (3)</span><span class="sxs-lookup"><span data-stu-id="f11de-122"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="f11de-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Используется/недоступно** (4)</span><span class="sxs-lookup"><span data-stu-id="f11de-123"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="f11de-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Используется и доступно, а совместное использование** (5)</span><span class="sxs-lookup"><span data-stu-id="f11de-124"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="f11de-125">Используется и доступно, а совместное использование</span><span class="sxs-lookup"><span data-stu-id="f11de-125">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="f11de-126">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="f11de-126">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-127">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-129">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="f11de-129">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-130">Краткое текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f11de-130">A short textual description of the object.</span></span>

<span data-ttu-id="f11de-131">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f11de-132">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="f11de-132">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-135">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f11de-135">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f11de-136">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="f11de-136">Name of the class or subclass used in the creation of an instance.</span></span> <span data-ttu-id="f11de-137">При использовании с другими ключевыми свойствами класса это свойство позволяет однозначно идентифицировать все экземпляры класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="f11de-137">When used with other key properties of the class, this property allows all instances of the class and its subclasses to be uniquely identified.</span></span>

</dd> <dt>

<span data-ttu-id="f11de-138">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="f11de-138">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-141">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f11de-141">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f11de-142">Определение области имени класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f11de-142">Scoping computer system's creation class name.</span></span>

</dd> <dt>

<span data-ttu-id="f11de-143">**CSName**</span><span class="sxs-lookup"><span data-stu-id="f11de-143">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-146">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f11de-146">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f11de-147">Определение области имени системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="f11de-147">Scoping computer system's name.</span></span>

</dd> <dt>

<span data-ttu-id="f11de-148">**Описание**</span><span class="sxs-lookup"><span data-stu-id="f11de-148">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-151">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="f11de-151">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-152">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="f11de-152">A textual description of the object.</span></span>

<span data-ttu-id="f11de-153">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-153">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f11de-154">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="f11de-154">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-155">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="f11de-155">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-157">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="f11de-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-158">Указывает, когда был установлен объект.</span><span class="sxs-lookup"><span data-stu-id="f11de-158">Indicates when the object was installed.</span></span> <span data-ttu-id="f11de-159">Отсутствие значения не означает, что объект не установлен.</span><span class="sxs-lookup"><span data-stu-id="f11de-159">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="f11de-160">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-160">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f11de-161">**Номер запроса прерывания**</span><span class="sxs-lookup"><span data-stu-id="f11de-161">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f11de-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-164">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ \| 001,1 "), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f11de-164">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="f11de-165">Часть значения ключа объекта, номер IRQ.</span><span class="sxs-lookup"><span data-stu-id="f11de-165">Part of the object's key value, IRQ number.</span></span>

</dd> <dt>

<span data-ttu-id="f11de-166">**Name**</span><span class="sxs-lookup"><span data-stu-id="f11de-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-169">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="f11de-169">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-170">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="f11de-170">Label by which the object is known.</span></span> <span data-ttu-id="f11de-171">При создании подклассов это свойство может быть переопределено как свойство ключа.</span><span class="sxs-lookup"><span data-stu-id="f11de-171">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="f11de-172">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-172">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f11de-173">**Возможностью общего доступа**</span><span class="sxs-lookup"><span data-stu-id="f11de-173">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-174">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="f11de-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-175">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-175">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-176">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ 001,4 (DMTF \| )</span><span class="sxs-lookup"><span data-stu-id="f11de-176">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-177">**Значение true** показывает, что IRQ можно совместно использовать.</span><span class="sxs-lookup"><span data-stu-id="f11de-177">If **TRUE**, the IRQ can be shared.</span></span>

</dd> <dt>

<span data-ttu-id="f11de-178">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f11de-178">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="f11de-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-181">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="f11de-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-182">Строка, указывающая текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="f11de-182">String that indicates the current status of the object.</span></span> <span data-ttu-id="f11de-183">Можно определить операционное и нерабочее состояние.</span><span class="sxs-lookup"><span data-stu-id="f11de-183">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="f11de-184">Оперативное состояние может включать "ОК", "деградация" и "пред Fail".</span><span class="sxs-lookup"><span data-stu-id="f11de-184">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="f11de-185">"Пред-Fail" указывает, что элемент работает правильно, но прогнозирует сбой (например, жесткий диск с поддержкой SMART).</span><span class="sxs-lookup"><span data-stu-id="f11de-185">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="f11de-186">Нерабочее состояние может включать "Error", "starting", "остановка" и "обслуживание".</span><span class="sxs-lookup"><span data-stu-id="f11de-186">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="f11de-187">"Служба" может применяться при зеркальном отображении дисков, перезагрузке списка разрешений пользователя или выполнении других административных задач.</span><span class="sxs-lookup"><span data-stu-id="f11de-187">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="f11de-188">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни в одном из других состояний.</span><span class="sxs-lookup"><span data-stu-id="f11de-188">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="f11de-189">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="f11de-189">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="f11de-190">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="f11de-190">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="f11de-191">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="f11de-191">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="f11de-192">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="f11de-192">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="f11de-193">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="f11de-193">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f11de-194">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="f11de-194">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="f11de-195">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="f11de-195">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="f11de-196">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="f11de-196">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="f11de-197">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="f11de-197">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="f11de-198">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="f11de-198">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="f11de-199">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="f11de-199">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="f11de-200">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="f11de-200">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="f11de-201">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="f11de-201">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="f11de-202">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="f11de-202">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f11de-203">**тригжерлевел**</span><span class="sxs-lookup"><span data-stu-id="f11de-203">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-204">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f11de-204">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-206">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сведения о IRQ для системных ресурсов DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="f11de-206">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-207">Указывает, инициируется ли прерывание аппаратным сигналом с высоким или низким приоритетом.</span><span class="sxs-lookup"><span data-stu-id="f11de-207">Indicates whether the interruption is triggered by the hardware signal going high or low.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f11de-208">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f11de-208">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f11de-209">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f11de-209">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="f11de-210">**Активный низкий** (3)</span><span class="sxs-lookup"><span data-stu-id="f11de-210">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="f11de-211">**Активный высокий** (4)</span><span class="sxs-lookup"><span data-stu-id="f11de-211">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="f11de-212">**TriggerType может принимать**</span><span class="sxs-lookup"><span data-stu-id="f11de-212">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f11de-213">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f11de-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f11de-214">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="f11de-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f11de-215">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ \| 001,3 "," DMTF. \|Сведения о IRQ для системных ресурсов DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="f11de-215">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="f11de-216">Тип прерывания, которое может произойти.</span><span class="sxs-lookup"><span data-stu-id="f11de-216">Type of interruption that can occur.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="f11de-217">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="f11de-217">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="f11de-218">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="f11de-218">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="f11de-219">**Уровень** (3)</span><span class="sxs-lookup"><span data-stu-id="f11de-219">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="f11de-220">**Ребро** (4)</span><span class="sxs-lookup"><span data-stu-id="f11de-220">**Edge** (4)</span></span>


<span data-ttu-id="f11de-221"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f11de-221"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="f11de-222">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f11de-222">Remarks</span></span>

<span data-ttu-id="f11de-223">Класс **\_ IRQ CIM** является производным от [**CIM \_ системресаурце**](cim-systemresource.md). Инструментарий WMI не реализует этот класс.</span><span class="sxs-lookup"><span data-stu-id="f11de-223">The **CIM\_IRQ** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).WMI does not implement this class.</span></span> <span data-ttu-id="f11de-224">См. раздел [Классы Win32](win32-provider.md) для классов, производных от **\_ IRQ CIM**.</span><span class="sxs-lookup"><span data-stu-id="f11de-224">See [Win32 Classes](win32-provider.md) for classes derived from **CIM\_IRQ**.</span></span>

<span data-ttu-id="f11de-225">Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF.</span><span class="sxs-lookup"><span data-stu-id="f11de-225">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f11de-226">Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="f11de-226">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f11de-227">Требования</span><span class="sxs-lookup"><span data-stu-id="f11de-227">Requirements</span></span>



| <span data-ttu-id="f11de-228">Требование</span><span class="sxs-lookup"><span data-stu-id="f11de-228">Requirement</span></span> | <span data-ttu-id="f11de-229">Значение</span><span class="sxs-lookup"><span data-stu-id="f11de-229">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f11de-230">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f11de-230">Minimum supported client</span></span><br/> | <span data-ttu-id="f11de-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f11de-231">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f11de-232">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f11de-232">Minimum supported server</span></span><br/> | <span data-ttu-id="f11de-233">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f11de-233">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f11de-234">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f11de-234">Namespace</span></span><br/>                | <span data-ttu-id="f11de-235">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f11de-235">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f11de-236">MOF</span><span class="sxs-lookup"><span data-stu-id="f11de-236">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f11de-237"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f11de-237"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f11de-238">DLL</span><span class="sxs-lookup"><span data-stu-id="f11de-238">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f11de-239"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f11de-239"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f11de-240">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f11de-240">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f11de-241">**\_СИСТЕМРЕСАУРЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="f11de-241">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> </dl>

 

