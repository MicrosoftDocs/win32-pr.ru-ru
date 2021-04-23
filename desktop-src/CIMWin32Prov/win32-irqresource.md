---
description: '&Win32 \_ иркресаурце \# 160; Класс WMI представляет номер линии запроса прерывания (IRQ) в компьютерной системе под Windows.'
ms.assetid: bae0c28e-2b66-40ac-9679-b2dfe9269306
ms.tgt_platform: multiple
title: Класс Win32_IRQResource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_IRQResource
- Win32_IRQResource.Availability
- Win32_IRQResource.Caption
- Win32_IRQResource.CreationClassName
- Win32_IRQResource.CSCreationClassName
- Win32_IRQResource.CSName
- Win32_IRQResource.Description
- Win32_IRQResource.Hardware
- Win32_IRQResource.InstallDate
- Win32_IRQResource.IRQNumber
- Win32_IRQResource.Name
- Win32_IRQResource.Shareable
- Win32_IRQResource.Status
- Win32_IRQResource.TriggerLevel
- Win32_IRQResource.TriggerType
- Win32_IRQResource.Vector
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: cd02487fe166cd7ce55482eaca1339c8701f2b62
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141155"
---
# <a name="win32_irqresource-class"></a><span data-ttu-id="87872-103">\_Класс Win32 иркресаурце</span><span class="sxs-lookup"><span data-stu-id="87872-103">Win32\_IRQResource class</span></span>

<span data-ttu-id="87872-104">[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ иркресаурце для Win32** представляет номер линии запроса прерывания (IRQ) в компьютерной системе под Windows.  </span><span class="sxs-lookup"><span data-stu-id="87872-104">The **Win32\_IRQResource**  [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an interrupt request line (IRQ) number on a computer system running Windows.</span></span> <span data-ttu-id="87872-105">Запрос на прерывание — это сигнал, который устройство или программа отправляет в ЦП для выполнения критических событий.</span><span class="sxs-lookup"><span data-stu-id="87872-105">An interrupt request is a signal sent to the CPU by a device or program for time critical events.</span></span> <span data-ttu-id="87872-106">IRQ может основываться на оборудовании или программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="87872-106">IRQ can be hardware-based or software-based.</span></span>

<span data-ttu-id="87872-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="87872-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="87872-108">Свойства перечислены в алфавитном порядке, а не в MOF.</span><span class="sxs-lookup"><span data-stu-id="87872-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="87872-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87872-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4D3-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_IRQResource : CIM_IRQ
{
  uint16   Availability;
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  boolean  Hardware;
  datetime InstallDate;
  uint32   IRQNumber;
  string   Name;
  boolean  Shareable;
  string   Status;
  uint16   TriggerLevel;
  uint16   TriggerType;
  uint32   Vector;
};
```

## <a name="members"></a><span data-ttu-id="87872-110">Члены</span><span class="sxs-lookup"><span data-stu-id="87872-110">Members</span></span>

<span data-ttu-id="87872-111">Класс **Win32 \_ иркресаурце** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="87872-111">The **Win32\_IRQResource** class has these types of members:</span></span>

-   [<span data-ttu-id="87872-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="87872-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87872-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="87872-113">Properties</span></span>

<span data-ttu-id="87872-114">Класс **Win32 \_ иркресаурце** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="87872-114">The **Win32\_IRQResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87872-115">**Доступность**</span><span class="sxs-lookup"><span data-stu-id="87872-115">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-116">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87872-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87872-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-118">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ 001,2 (DMTF \| )</span><span class="sxs-lookup"><span data-stu-id="87872-118">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="87872-119">Доступность IRQ.</span><span class="sxs-lookup"><span data-stu-id="87872-119">Availability of the IRQ.</span></span>

<span data-ttu-id="87872-120">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-120">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="87872-121"><span id="0"></span>**0,0**</span><span class="sxs-lookup"><span data-stu-id="87872-121"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="87872-122">Другое</span><span class="sxs-lookup"><span data-stu-id="87872-122">Other</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="87872-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="87872-123"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="87872-124">Неизвестно</span><span class="sxs-lookup"><span data-stu-id="87872-124">Unknown</span></span>

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87872-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="87872-125"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd>

<span data-ttu-id="87872-126">Доступно</span><span class="sxs-lookup"><span data-stu-id="87872-126">Available</span></span>

</dd> <dt>

<span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>

<span data-ttu-id="87872-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Доступно** (3)</span><span class="sxs-lookup"><span data-stu-id="87872-127"><span id="Available"></span><span id="available"></span><span id="AVAILABLE"></span>**Available** (3)</span></span>


</dt> <dd>

<span data-ttu-id="87872-128">Используется или недоступно</span><span class="sxs-lookup"><span data-stu-id="87872-128">In Use or Not Available</span></span>

</dd> <dt>

<span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>

<span data-ttu-id="87872-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**Используется/недоступно** (4)</span><span class="sxs-lookup"><span data-stu-id="87872-129"><span id="In_Use_Not_Available"></span><span id="in_use_not_available"></span><span id="IN_USE_NOT_AVAILABLE"></span>**In Use/Not Available** (4)</span></span>


</dt> <dd>

<span data-ttu-id="87872-130">Используется и доступно, или совместное использование</span><span class="sxs-lookup"><span data-stu-id="87872-130">In Use and Available or Sharable</span></span>

</dd> <dt>

<span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>

<span data-ttu-id="87872-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**Используется и доступно, а совместное использование** (5)</span><span class="sxs-lookup"><span data-stu-id="87872-131"><span id="In_Use_and_Available_Shareable"></span><span id="in_use_and_available_shareable"></span><span id="IN_USE_AND_AVAILABLE_SHAREABLE"></span>**In Use and Available/Shareable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="87872-132">Используется и доступно, а совместное использование</span><span class="sxs-lookup"><span data-stu-id="87872-132">In use and available/sharable</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="87872-133">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="87872-133">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-136">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="87872-136">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="87872-137">Краткое описание объекта — однострочная строка.</span><span class="sxs-lookup"><span data-stu-id="87872-137">Short description of the object a one-line string.</span></span>

<span data-ttu-id="87872-138">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87872-138">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-139">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="87872-139">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-142">Квалификаторы: [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="87872-142">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="87872-143">Имя первого конкретного класса, который будет отображаться в цепочке наследования, используемой при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="87872-143">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="87872-144">При использовании с другими ключевыми свойствами класса свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="87872-144">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="87872-145">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-145">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-146">**кскреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="87872-146">**CSCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-147">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-149">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="87872-149">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**CreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="87872-150">Имя класса создания системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="87872-150">Name of the scoping computer system creation class.</span></span>

<span data-ttu-id="87872-151">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-151">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-152">**CSName**</span><span class="sxs-lookup"><span data-stu-id="87872-152">**CSName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-155">Квалификаторы: [**распространяются**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ComputerSystem**](cim-computersystem.md).**Name**"), [**\_ ключ CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="87872-155">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ComputerSystem**](cim-computersystem.md).**Name**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="87872-156">Имя системы области компьютера.</span><span class="sxs-lookup"><span data-stu-id="87872-156">Name of the scoping computer system.</span></span>

<span data-ttu-id="87872-157">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-157">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-158">**Описание**</span><span class="sxs-lookup"><span data-stu-id="87872-158">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-161">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Описание")</span><span class="sxs-lookup"><span data-stu-id="87872-161">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="87872-162">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="87872-162">Textual description of the object.</span></span>

<span data-ttu-id="87872-163">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87872-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-164">**Оборудование**</span><span class="sxs-lookup"><span data-stu-id="87872-164">**Hardware**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-165">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="87872-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87872-166">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-167">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| системных структур \| ресурсов \_ \| InterfaceType")</span><span class="sxs-lookup"><span data-stu-id="87872-167">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|RESOURCE\_DESCRIPTOR\|InterfaceType")</span></span>
</dt> </dl>

<span data-ttu-id="87872-168">Если **значение равно true**, то прерывание зависит от оборудования или программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="87872-168">If **TRUE**, the interrupt is hardware or software based.</span></span> <span data-ttu-id="87872-169">Аппаратный IRQ — это физическое соединение между периферийным устройством и программируемым микросхемами контроллера прерываний (PIC), с помощью которых ЦП может получать уведомления о критических для времени событиях.</span><span class="sxs-lookup"><span data-stu-id="87872-169">A hardware IRQ is a physical wire from the peripheral to the programmable interrupt controller (PIC) chip through which the CPU can be notified of time-critical events.</span></span> <span data-ttu-id="87872-170">Некоторые линии IRQ зарезервированы для стандартных устройств, таких как клавиатура, дисководы гибких дисков и системные часы.</span><span class="sxs-lookup"><span data-stu-id="87872-170">Some IRQ lines are reserved for standard devices, such as the keyboard, floppy disk drives, and the system clock.</span></span> <span data-ttu-id="87872-171">Программное прерывание позволяет приложениям извлекать внимание на процессор.</span><span class="sxs-lookup"><span data-stu-id="87872-171">A software interrupt allows applications to get the attention of the processor.</span></span>

</dd> <dt>

<span data-ttu-id="87872-172">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="87872-172">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-173">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="87872-173">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="87872-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-175">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" Дата установки ")</span><span class="sxs-lookup"><span data-stu-id="87872-175">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="87872-176">Дата и время установки объекта.</span><span class="sxs-lookup"><span data-stu-id="87872-176">Date and time the object was installed.</span></span> <span data-ttu-id="87872-177">Для этого свойства не требуется значение, указывающее, что объект установлен.</span><span class="sxs-lookup"><span data-stu-id="87872-177">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="87872-178">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87872-178">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-179">**Номер запроса прерывания**</span><span class="sxs-lookup"><span data-stu-id="87872-179">**IRQNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-180">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87872-180">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87872-181">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-182">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ \| 001,1 "), [**ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="87872-182">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.1"), [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="87872-183">Часть значения ключа объекта.</span><span class="sxs-lookup"><span data-stu-id="87872-183">Part of the object's key value.</span></span>

<span data-ttu-id="87872-184">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-184">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-185">**Name**</span><span class="sxs-lookup"><span data-stu-id="87872-185">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-186">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-187">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-187">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-188">Квалификаторы: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("имя")</span><span class="sxs-lookup"><span data-stu-id="87872-188">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="87872-189">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="87872-189">Label by which the object is known.</span></span> <span data-ttu-id="87872-190">При создании подклассов свойство может быть переопределено как ключевое свойство.</span><span class="sxs-lookup"><span data-stu-id="87872-190">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="87872-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87872-191">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-192">**Возможностью общего доступа**</span><span class="sxs-lookup"><span data-stu-id="87872-192">**Shareable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-193">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="87872-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="87872-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-195">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ 001,4 (DMTF \| )</span><span class="sxs-lookup"><span data-stu-id="87872-195">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="87872-196">**Значение true** показывает, что IRQ можно совместно использовать.</span><span class="sxs-lookup"><span data-stu-id="87872-196">If **TRUE**, the IRQ can be shared.</span></span>

<span data-ttu-id="87872-197">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-197">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

</dd> <dt>

<span data-ttu-id="87872-198">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="87872-198">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-199">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="87872-199">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87872-200">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-200">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-201">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("состояние")</span><span class="sxs-lookup"><span data-stu-id="87872-201">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="87872-202">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="87872-202">Current status of the object.</span></span> <span data-ttu-id="87872-203">Можно определить различные операционные и неоперационные состояния.</span><span class="sxs-lookup"><span data-stu-id="87872-203">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="87872-204">Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем).</span><span class="sxs-lookup"><span data-stu-id="87872-204">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="87872-205">Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба".</span><span class="sxs-lookup"><span data-stu-id="87872-205">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="87872-206">Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы.</span><span class="sxs-lookup"><span data-stu-id="87872-206">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="87872-207">Не вся такая работа находится в оперативном режиме, но управляемый элемент не является ни "ОК", ни одним из других состояний.</span><span class="sxs-lookup"><span data-stu-id="87872-207">Not all such work is online, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="87872-208">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="87872-208">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="87872-209">В эти значения входят:</span><span class="sxs-lookup"><span data-stu-id="87872-209">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="87872-210">**ОК** ("ОК")</span><span class="sxs-lookup"><span data-stu-id="87872-210">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="87872-211">**Ошибка** ("ошибка")</span><span class="sxs-lookup"><span data-stu-id="87872-211">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="87872-212">**Пониженная работоспособность** (пониженная работоспособность)</span><span class="sxs-lookup"><span data-stu-id="87872-212">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87872-213">**Неизвестно** ("неизвестно")</span><span class="sxs-lookup"><span data-stu-id="87872-213">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="87872-214">**Пред-ошибка** ("пред Fail")</span><span class="sxs-lookup"><span data-stu-id="87872-214">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="87872-215">**Запуск** ("Запуск")</span><span class="sxs-lookup"><span data-stu-id="87872-215">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="87872-216">**Остановка** ("остановка")</span><span class="sxs-lookup"><span data-stu-id="87872-216">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="87872-217">**Служба** ("служба")</span><span class="sxs-lookup"><span data-stu-id="87872-217">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="87872-218">**Пренапряжению** ("напряжению")</span><span class="sxs-lookup"><span data-stu-id="87872-218">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="87872-219">**Невосстановление** ("невосстановление")</span><span class="sxs-lookup"><span data-stu-id="87872-219">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="87872-220">**Нет контакта** ("нет контакта")</span><span class="sxs-lookup"><span data-stu-id="87872-220">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="87872-221">**Потеря** связи ("потеря связи")</span><span class="sxs-lookup"><span data-stu-id="87872-221">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87872-222">**тригжерлевел**</span><span class="sxs-lookup"><span data-stu-id="87872-222">**TriggerLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-223">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87872-223">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87872-224">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-224">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-225">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Сведения о IRQ для системных ресурсов DMTF \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="87872-225">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|System Resource IRQ Info\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="87872-226">Уровень активации IRQ, указывающий, инициируется ли прерывание аппаратным сигналом (4) или низким (3).</span><span class="sxs-lookup"><span data-stu-id="87872-226">IRQ trigger level indicating whether the interrupt is triggered by the hardware signal going high (4) or low (3).</span></span>

<span data-ttu-id="87872-227">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-227">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="87872-228">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="87872-228">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87872-229">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="87872-229">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_Low"></span><span id="active_low"></span><span id="ACTIVE_LOW"></span>

<span data-ttu-id="87872-230">**Активный низкий** (3)</span><span class="sxs-lookup"><span data-stu-id="87872-230">**Active Low** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Active_High"></span><span id="active_high"></span><span id="ACTIVE_HIGH"></span>

<span data-ttu-id="87872-231">**Активный высокий** (4)</span><span class="sxs-lookup"><span data-stu-id="87872-231">**Active High** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87872-232">**TriggerType может принимать**</span><span class="sxs-lookup"><span data-stu-id="87872-232">**TriggerType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-233">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="87872-233">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="87872-234">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-234">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-235">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|IRQ \| 001,3 "," DMTF. \|Сведения о IRQ для системных ресурсов DMTF \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="87872-235">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|IRQ\|001.3", "MIF.DMTF\|System Resource IRQ Info\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="87872-236">Тип триггера IRQ, указывающий, выполняются ли прерывания с пограничным запуском (4) или с срабатыванием уровня (3).</span><span class="sxs-lookup"><span data-stu-id="87872-236">IRQ trigger type indicating whether edge-triggered (4) or level-triggered (3) interrupts occur.</span></span>

<span data-ttu-id="87872-237">Это свойство наследуется [**от \_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-237">This property is inherited from [**CIM\_IRQ**](cim-irq.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="87872-238">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="87872-238">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="87872-239">**Неизвестно** (2)</span><span class="sxs-lookup"><span data-stu-id="87872-239">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>

<span data-ttu-id="87872-240">**Уровень** (3)</span><span class="sxs-lookup"><span data-stu-id="87872-240">**Level** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Edge"></span><span id="edge"></span><span id="EDGE"></span>

<span data-ttu-id="87872-241">**Ребро** (4)</span><span class="sxs-lookup"><span data-stu-id="87872-241">**Edge** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="87872-242">**Вектор**</span><span class="sxs-lookup"><span data-stu-id="87872-242">**Vector**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87872-243">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87872-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87872-244">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="87872-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87872-245">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| системные структуры \| cm: уровень прерываний [**\_ частичного \_ ресурса \_**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor) \| \| ")</span><span class="sxs-lookup"><span data-stu-id="87872-245">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API\|System Structures\|[**CM\_PARTIAL\_RESOURCE\_DESCRIPTOR**](/windows-hardware/drivers/ddi/content/wdm/ns-wdm-_cm_partial_resource_descriptor)\|Interrupt\|Level")</span></span>
</dt> </dl>

<span data-ttu-id="87872-246">Вектор ресурса IRQ Windows.</span><span class="sxs-lookup"><span data-stu-id="87872-246">Vector of the Windows IRQ resource.</span></span> <span data-ttu-id="87872-247">Вектор содержит адрес памяти для функции, которая будет выполняться после того, как запрос на прерывание подтверждается ЦП.</span><span class="sxs-lookup"><span data-stu-id="87872-247">A vector contains the memory address to the function that will execute once the interrupt request is acknowledged by the CPU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87872-248">Комментарии</span><span class="sxs-lookup"><span data-stu-id="87872-248">Remarks</span></span>

<span data-ttu-id="87872-249">Класс **Win32 \_ иркресаурце** является производным от [**\_ IRQ CIM**](cim-irq.md).</span><span class="sxs-lookup"><span data-stu-id="87872-249">The **Win32\_IRQResource** class is derived from [**CIM\_IRQ**](cim-irq.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="87872-250">Требования</span><span class="sxs-lookup"><span data-stu-id="87872-250">Requirements</span></span>



| <span data-ttu-id="87872-251">Требование</span><span class="sxs-lookup"><span data-stu-id="87872-251">Requirement</span></span> | <span data-ttu-id="87872-252">Значение</span><span class="sxs-lookup"><span data-stu-id="87872-252">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="87872-253">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="87872-253">Minimum supported client</span></span><br/> | <span data-ttu-id="87872-254">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="87872-254">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="87872-255">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="87872-255">Minimum supported server</span></span><br/> | <span data-ttu-id="87872-256">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="87872-256">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="87872-257">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="87872-257">Namespace</span></span><br/>                | <span data-ttu-id="87872-258">Корневой \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="87872-258">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="87872-259">MOF</span><span class="sxs-lookup"><span data-stu-id="87872-259">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87872-260"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87872-260"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="87872-261">DLL</span><span class="sxs-lookup"><span data-stu-id="87872-261">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87872-262"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87872-262"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87872-263">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="87872-263">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87872-264">**\_IRQ CIM**</span><span class="sxs-lookup"><span data-stu-id="87872-264">**CIM\_IRQ**</span></span>](cim-irq.md)
</dt> <dt>

[<span data-ttu-id="87872-265">Аппаратные классы системы компьютера</span><span class="sxs-lookup"><span data-stu-id="87872-265">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

