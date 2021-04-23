---
description: Представляет запланированную виртуальную машину.
ms.assetid: 4ce6d34c-66fb-4f4f-bf52-26d19bab6d4a
title: Класс Msvm_PlannedComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PlannedComputerSystem
- Msvm_PlannedComputerSystem.SetPowerState
- Msvm_PlannedComputerSystem.InstanceID
- Msvm_PlannedComputerSystem.Caption
- Msvm_PlannedComputerSystem.Description
- Msvm_PlannedComputerSystem.ElementName
- Msvm_PlannedComputerSystem.InstallDate
- Msvm_PlannedComputerSystem.OperationalStatus
- Msvm_PlannedComputerSystem.StatusDescriptions
- Msvm_PlannedComputerSystem.Status
- Msvm_PlannedComputerSystem.HealthState
- Msvm_PlannedComputerSystem.CommunicationStatus
- Msvm_PlannedComputerSystem.DetailedStatus
- Msvm_PlannedComputerSystem.OperatingStatus
- Msvm_PlannedComputerSystem.PrimaryStatus
- Msvm_PlannedComputerSystem.EnabledState
- Msvm_PlannedComputerSystem.OtherEnabledState
- Msvm_PlannedComputerSystem.RequestedState
- Msvm_PlannedComputerSystem.EnabledDefault
- Msvm_PlannedComputerSystem.TimeOfLastStateChange
- Msvm_PlannedComputerSystem.AvailableRequestedStates
- Msvm_PlannedComputerSystem.TransitioningToState
- Msvm_PlannedComputerSystem.CreationClassName
- Msvm_PlannedComputerSystem.Name
- Msvm_PlannedComputerSystem.NameFormat
- Msvm_PlannedComputerSystem.PrimaryOwnerName
- Msvm_PlannedComputerSystem.PrimaryOwnerContact
- Msvm_PlannedComputerSystem.Roles
- Msvm_PlannedComputerSystem.OtherIdentifyingInfo
- Msvm_PlannedComputerSystem.IdentifyingDescriptions
- Msvm_PlannedComputerSystem.Dedicated
- Msvm_PlannedComputerSystem.OtherDedicatedDescriptions
- Msvm_PlannedComputerSystem.ResetCapability
- Msvm_PlannedComputerSystem.PowerManagementCapabilities
- Msvm_PlannedComputerSystem.AssignedNumaNodeList
- Msvm_PlannedComputerSystem.OnTimeInMilliseconds
- Msvm_PlannedComputerSystem.ProcessID
- Msvm_PlannedComputerSystem.TimeOfLastConfigurationChange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54bd72567880e97ece02936348d5a091a11d8ef3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684459"
---
# <a name="msvm_plannedcomputersystem-class"></a><span data-ttu-id="fcafa-103">\_Класс мсвм планнедкомпутерсистем</span><span class="sxs-lookup"><span data-stu-id="fcafa-103">Msvm\_PlannedComputerSystem class</span></span>

<span data-ttu-id="fcafa-104">Представляет запланированную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="fcafa-104">Represents a planned virtual machine.</span></span>

<span data-ttu-id="fcafa-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="fcafa-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fcafa-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fcafa-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PlannedComputerSystem : CIM_ComputerSystem
{
  string   InstanceID;
  string   Caption = "Planned Virtual Machine";
  string   Description = "Microsoft Planned Virtual Machine";
  string   ElementName;
  datetime InstallDate;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "The service is running normally" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   CreationClassName;
  string   Name;
  string   NameFormat;
  string   PrimaryOwnerName;
  string   PrimaryOwnerContact;
  string   Roles[];
  string   OtherIdentifyingInfo[];
  string   IdentifyingDescriptions[];
  uint16   Dedicated[];
  string   OtherDedicatedDescriptions[];
  uint16   ResetCapability;
  uint16   PowerManagementCapabilities[];
  uint16   AssignedNumaNodeList[];
  uint64   OnTimeInMilliseconds;
  uint32   ProcessID;
  datetime TimeOfLastConfigurationChange;
};
```

## <a name="members"></a><span data-ttu-id="fcafa-107">Члены</span><span class="sxs-lookup"><span data-stu-id="fcafa-107">Members</span></span>

<span data-ttu-id="fcafa-108">Класс **мсвм \_ планнедкомпутерсистем** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="fcafa-108">The **Msvm\_PlannedComputerSystem** class has these types of members:</span></span>

-   [<span data-ttu-id="fcafa-109">Методы</span><span class="sxs-lookup"><span data-stu-id="fcafa-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="fcafa-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcafa-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fcafa-111">Методы</span><span class="sxs-lookup"><span data-stu-id="fcafa-111">Methods</span></span>

<span data-ttu-id="fcafa-112">Класс **мсвм \_ планнедкомпутерсистем** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="fcafa-112">The **Msvm\_PlannedComputerSystem** class has these methods.</span></span>



| <span data-ttu-id="fcafa-113">Метод</span><span class="sxs-lookup"><span data-stu-id="fcafa-113">Method</span></span>                                                                      | <span data-ttu-id="fcafa-114">Описание</span><span class="sxs-lookup"><span data-stu-id="fcafa-114">Description</span></span>                                                                                 |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcafa-115">**Равен**</span><span class="sxs-lookup"><span data-stu-id="fcafa-115">**RequestStateChange**</span></span>](requeststatechange-msvm-plannedcomputersystem.md) | <span data-ttu-id="fcafa-116">Запрашивает изменение состояния запланированной системы на указанное значение.</span><span class="sxs-lookup"><span data-stu-id="fcafa-116">Requests that the state of the planned system be changed to the value specified.</span></span><br/> |
| <span data-ttu-id="fcafa-117">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fcafa-117">**SetPowerState**</span></span>                                                           | <span data-ttu-id="fcafa-118">Этот метод не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fcafa-118">This method is not supported.</span></span><br/>                                                    |



 

### <a name="properties"></a><span data-ttu-id="fcafa-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="fcafa-119">Properties</span></span>

<span data-ttu-id="fcafa-120">Класс **мсвм \_ планнедкомпутерсистем** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="fcafa-120">The **Msvm\_PlannedComputerSystem** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fcafa-121">**ассигнеднуманоделист**</span><span class="sxs-lookup"><span data-stu-id="fcafa-121">**AssignedNumaNodeList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-122">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="fcafa-122">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-124">Квалификаторы: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("индексированный")</span><span class="sxs-lookup"><span data-stu-id="fcafa-124">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-125">Массив узлов неоднородным доступом для доступа к памяти (NUMA), которые в настоящее время назначены виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="fcafa-125">An array of nonuniform memory access (NUMA) nodes that are currently assigned to the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-126">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="fcafa-126">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-127">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="fcafa-127">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-129">Указывает возможные значения для параметра *RequestedState* метода [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) , используемого для инициации изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="fcafa-129">Indicates the possible values for the *RequestedState* parameter of the [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) method used to initiate a state change.</span></span> <span data-ttu-id="fcafa-130">Перечисленные значения будут представлять собой подмножество значений, содержащихся в свойстве **рекуестедстатессуппортед** связанного экземпляра **CIM \_ енабледлогикалелементкапабилитиес**, где выбранные значения являются функцией текущего состояния объекта [**\_ енабледлогикалелемент CIM**](/previous-versions//cc136818(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-130">The values listed will be a subset of the values contained in the **RequestedStatesSupported** property of the associated instance of **CIM\_EnabledLogicalElementCapabilities**, where the values selected are a function of the current state of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) object.</span></span> <span data-ttu-id="fcafa-131">Это свойство может иметь значение, отличное от **null** , если реализация может объявить набор возможных значений как функцию текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="fcafa-131">This property can be non-**Null** if an implementation is able to advertise the set of possible values as a function of the current state.</span></span> <span data-ttu-id="fcafa-132">Это свойство будет иметь **значение NULL** , если реализация не может определить набор возможных значений в качестве функции текущего состояния.</span><span class="sxs-lookup"><span data-stu-id="fcafa-132">This property will be **Null** if an implementation is unable to determine the set of possible values as a function of the current state.</span></span>

<span data-ttu-id="fcafa-133">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fcafa-133">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fcafa-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Включено** (2)</span><span class="sxs-lookup"><span data-stu-id="fcafa-134"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** (3)</span><span class="sxs-lookup"><span data-stu-id="fcafa-135"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Завершение работы** (4)</span><span class="sxs-lookup"><span data-stu-id="fcafa-136"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Вне сети** (6)</span><span class="sxs-lookup"><span data-stu-id="fcafa-137"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Тест** (7)</span><span class="sxs-lookup"><span data-stu-id="fcafa-138"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Отложить** (8)</span><span class="sxs-lookup"><span data-stu-id="fcafa-139"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Замораживание** (9)</span><span class="sxs-lookup"><span data-stu-id="fcafa-140"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Перезагрузка** (10)</span><span class="sxs-lookup"><span data-stu-id="fcafa-141"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (11)</span><span class="sxs-lookup"><span data-stu-id="fcafa-142"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**Зарезервировано DMTF** (..</span><span class="sxs-lookup"><span data-stu-id="fcafa-143"><span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF Reserved** (..</span></span> <span data-ttu-id="fcafa-144">)</span><span class="sxs-lookup"><span data-stu-id="fcafa-144">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fcafa-145">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="fcafa-145">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-148">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fcafa-148">A short description of the object.</span></span> <span data-ttu-id="fcafa-149">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "запланированная виртуальная машина".</span><span class="sxs-lookup"><span data-stu-id="fcafa-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-150">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="fcafa-150">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-151">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-151">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-153">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="fcafa-153">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="fcafa-154">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="fcafa-154">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fcafa-155">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-155">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-156">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fcafa-156">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-159">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="fcafa-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-160">Указывает имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="fcafa-160">Indicates the name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="fcafa-161">При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="fcafa-161">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="fcafa-162">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-162">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-163">**Выделенные**</span><span class="sxs-lookup"><span data-stu-id="fcafa-163">**Dedicated**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-164">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="fcafa-164">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-166">Массив значений, указывающий цели, в которых запланированная система выделяется, если таковая имеется, и какие функциональные возможности предоставляются.</span><span class="sxs-lookup"><span data-stu-id="fcafa-166">An array of values that indicate the purposes to which the planned system is dedicated, if any, and what functionality is provided.</span></span> <span data-ttu-id="fcafa-167">Например, можно указать, что система предназначена для печати (значение = 11) или выступает в качестве "концентратора" (значение = 8).</span><span class="sxs-lookup"><span data-stu-id="fcafa-167">For example, one could specify that the System is dedicated to "Print" (value=11) or acts as a "Hub" (value=8).</span></span> <span data-ttu-id="fcafa-168">Также может быть указано несколько целей.</span><span class="sxs-lookup"><span data-stu-id="fcafa-168">Multiple purposes can also be indicated.</span></span> <span data-ttu-id="fcafa-169">Например, это система общего назначения, указывающая "не выделенное" (значение = 0), но на нем также размещены службы "Print" (значение = 11) или "мобильное устройство пользователя" (Value = 17).</span><span class="sxs-lookup"><span data-stu-id="fcafa-169">For example, this is a general purpose system indicating "Not Dedicated" (value=0) but that it also hosts "Print" (value=11) or "Mobile User Device" (value=17) services.</span></span>

<span data-ttu-id="fcafa-170">Это свойство наследуется от класса [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-170">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="fcafa-171">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-171">Value</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="fcafa-172">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-172">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span><dl> <span data-ttu-id="fcafa-173"><dt>**Не выделен**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-173"><dt>**Not Dedicated**</dt> <dt>0</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fcafa-174"><dt>**Неизвестно**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-174"><dt>**Unknown**</dt> <dt>1</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="fcafa-175"><dt>**Другие**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-175"><dt>**Other**</dt> <dt>2</dt></span></span> </dl>                                                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span><dl> <span data-ttu-id="fcafa-176"><dt>**Хранилище**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-176"><dt>**Storage**</dt> <dt>3</dt></span></span> </dl>                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Router"></span><span id="router"></span><span id="ROUTER"></span><dl> <span data-ttu-id="fcafa-177"><dt>**Маршрутизатор**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-177"><dt>**Router**</dt> <dt>4</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span><dl> <span data-ttu-id="fcafa-178"><dt>**Коммутатор**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-178"><dt>**Switch**</dt> <dt>5</dt></span></span> </dl>                                                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span><dl> <span data-ttu-id="fcafa-179"><dt>**Коммутатор 3 уровня**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-179"><dt>**Layer 3 Switch**</dt> <dt>6</dt></span></span> </dl>                                                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span><dl> <span data-ttu-id="fcafa-180"><dt>**Центральный офисный коммутатор**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-180"><dt>**Central Office Switch**</dt> <dt>7</dt></span></span> </dl>                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Hub"></span><span id="hub"></span><span id="HUB"></span><dl> <span data-ttu-id="fcafa-181"><dt>**Концентратор**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-181"><dt>**Hub**</dt> <dt>8</dt></span></span> </dl>                                                                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span><dl> <span data-ttu-id="fcafa-182"><dt>**Доступ к серверу**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-182"><dt>**Access Server**</dt> <dt>9</dt></span></span> </dl>                                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span><dl> <span data-ttu-id="fcafa-183"><dt>**Брандмауэр**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-183"><dt>**Firewall**</dt> <dt>10</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Print"></span><span id="print"></span><span id="PRINT"></span><dl> <span data-ttu-id="fcafa-184"><dt>**Печать**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-184"><dt>**Print**</dt> <dt>11</dt></span></span> </dl>                                                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="I_O"></span><span id="i_o"></span><dl> <span data-ttu-id="fcafa-185"><dt>**Ввод-вывод**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-185"><dt>**I/O**</dt> <dt>12</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span><dl> <span data-ttu-id="fcafa-186"><dt>**Веб-кэширование**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-186"><dt>**Web Caching**</dt> <dt>13</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span><dl> <span data-ttu-id="fcafa-187"><dt>**Управление**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-187"><dt>**Management**</dt> <dt>14</dt></span></span> </dl>                                                                 | <span data-ttu-id="fcafa-188">Указывает, что этот экземпляр выделен для размещения программного обеспечения управления системой.</span><span class="sxs-lookup"><span data-stu-id="fcafa-188">Indicates this instance is dedicated to hosting system management software.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span><dl> <span data-ttu-id="fcafa-189"><dt>**Блокировка сервера**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-189"><dt>**Block Server**</dt> <dt>15</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span><dl> <span data-ttu-id="fcafa-190"><dt>**Файловый сервер**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-190"><dt>**File Server**</dt> <dt>16</dt></span></span> </dl>                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span><dl> <span data-ttu-id="fcafa-191"><dt>**Мобильное устройство пользователя**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-191"><dt>**Mobile User Device**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="fcafa-192">Примером выделенного мобильного устройства пользователя является мобильный телефон или сканер штрих-кода в магазине, который взаимодействует через радиочастоту.</span><span class="sxs-lookup"><span data-stu-id="fcafa-192">An example of a dedicated mobile user device is a mobile phone or a bar code scanner in a store that communicates through radio frequency.</span></span> <span data-ttu-id="fcafa-193">Эти системы весьма ограничены функциональными возможностями и программируемостью и не считаются универсальными вычислительными платформами.</span><span class="sxs-lookup"><span data-stu-id="fcafa-193">These systems are quite limited in functionality and programmability, and are not considered general purpose computing platforms.</span></span> <span data-ttu-id="fcafa-194">В качестве альтернативы, пример мобильной системы, которая является общим намерением (то есть невыделенной), — это компьютер, удерживаемый вручную.</span><span class="sxs-lookup"><span data-stu-id="fcafa-194">Alternately, an example of a mobile system that is general purpose (that is, is NOT dedicated) is a hand-held computer.</span></span> <span data-ttu-id="fcafa-195">Хотя это и ограничено программируемостью, можно скачать новое программное обеспечение и его функциональность, развернутую пользователем.</span><span class="sxs-lookup"><span data-stu-id="fcafa-195">Although limited in its programmability, new software can be downloaded and its functionality expanded by the user.</span></span> <br/> |
| <span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span><dl> <span data-ttu-id="fcafa-196"><dt>**Повторитель**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-196"><dt>**Repeater**</dt> <dt>18</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span><dl> <span data-ttu-id="fcafa-197"><dt>**Мост/расширитель**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-197"><dt>**Bridge/Extender**</dt> <dt>19</dt></span></span> </dl>                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span><dl> <span data-ttu-id="fcafa-198"><dt>**Шлюз**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-198"><dt>**Gateway**</dt> <dt>20</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span><dl> <span data-ttu-id="fcafa-199"><dt>**Виртуализация хранилища**</dt> <dt>21</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-199"><dt>**Storage Virtualizer**</dt> <dt>21</dt></span></span> </dl>                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span><dl> <span data-ttu-id="fcafa-200"><dt>**Библиотека мультимедиа**</dt> <dt>22</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-200"><dt>**Media Library**</dt> <dt>22</dt></span></span> </dl>                                                     |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span><dl> <span data-ttu-id="fcafa-201"><dt>**Екстендерноде**</dt> <dt>23</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-201"><dt>**ExtenderNode**</dt> <dt>23</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span><dl> <span data-ttu-id="fcafa-202"><dt>**Головка NAS**</dt> <dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-202"><dt>**NAS Head**</dt> <dt>24</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span><dl> <span data-ttu-id="fcafa-203"><dt>**Автономный сервер NAS**</dt> <dt>25</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-203"><dt>**Self-contained NAS**</dt> <dt>25</dt></span></span> </dl>                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="UPS"></span><span id="ups"></span><dl> <span data-ttu-id="fcafa-204"><dt>**ИБП**</dt> <dt>26</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-204"><dt>**UPS**</dt> <dt>26</dt></span></span> </dl>                                                                                                                   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span><dl> <span data-ttu-id="fcafa-205"><dt>**IP Phone**</dt> <dt>27</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-205"><dt>**IP Phone**</dt> <dt>27</dt></span></span> </dl>                                                                         |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span><dl> <span data-ttu-id="fcafa-206"><dt>**Контроллер управления**</dt> <dt>28</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-206"><dt>**Management Controller**</dt> <dt>28</dt></span></span> </dl>                     | <span data-ttu-id="fcafa-207">Указывает, что этот экземпляр представляет специализированное оборудование, предназначенное для управления системами (то есть контроллера управления основной платой (BMC) или процессора служб).</span><span class="sxs-lookup"><span data-stu-id="fcafa-207">Indicates this instance represents specialized hardware dedicated to systems management (that is, a Baseboard Management Controller (BMC) or service processor).</span></span> <span data-ttu-id="fcafa-208">Областью управления контроллера управления обычно является единая управляемая система, в которой она содержится.</span><span class="sxs-lookup"><span data-stu-id="fcafa-208">The management scope of a Management Controller is typically a single managed system in which it is contained.</span></span><br/>                                                                                                                                                                                                                                           |
| <span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span><dl> <span data-ttu-id="fcafa-209"><dt>**Диспетчер корпусов**</dt> <dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-209"><dt>**Chassis Manager**</dt> <dt>29</dt></span></span> </dl>                                             | <span data-ttu-id="fcafa-210">Указывает, что этот экземпляр представляет систему, предназначенную для управления блейд-корпусом и содержащимися в нем устройствами.</span><span class="sxs-lookup"><span data-stu-id="fcafa-210">Indicates this instance represents a system dedicated to management of a blade chassis and its contained devices.</span></span> <span data-ttu-id="fcafa-211">Это значение будет использоваться для представления контроллера полки.</span><span class="sxs-lookup"><span data-stu-id="fcafa-211">This value would be used to represent a Shelf Controller.</span></span> <span data-ttu-id="fcafa-212">Диспетчер корпусов — это точка статистической обработки для управления, которая может полагаться на подчиненные контроллеры управления для управления составными частями.</span><span class="sxs-lookup"><span data-stu-id="fcafa-212">A Chassis Manager is an aggregation point for management and may rely on subordinate management controllers for the management of constituent parts.</span></span> <br/>                                                                                                                                                                                         |
| <span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span><dl> <span data-ttu-id="fcafa-213"><dt>**RAID-контроллер на основе узла**</dt> <dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-213"><dt>**Host-based RAID controller**</dt> <dt>30</dt></span></span> </dl> | <span data-ttu-id="fcafa-214">Указывает, что этот экземпляр представляет контроллер хранилища RAID, содержащийся на главном компьютере.</span><span class="sxs-lookup"><span data-stu-id="fcafa-214">Indicates this instance represents a RAID storage controller contained within a host computer.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span><dl> <span data-ttu-id="fcafa-215"><dt>**Корпус устройства хранения**</dt> <dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-215"><dt>**Storage Device Enclosure**</dt> <dt>31</dt></span></span> </dl>         | <span data-ttu-id="fcafa-216">Указывает, что этот экземпляр представляет собой корпус, содержащий устройства хранения.</span><span class="sxs-lookup"><span data-stu-id="fcafa-216">Indicates this instance represents an enclosure that contains storage devices.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span><dl> <span data-ttu-id="fcafa-217"><dt>**Desktop**</dt> <dt>32</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-217"><dt>**Desktop**</dt> <dt>32</dt></span></span> </dl>                                                                             |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span><dl> <span data-ttu-id="fcafa-218"><dt>**Портативный компьютер**</dt> <dt>33</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-218"><dt>**Laptop**</dt> <dt>33</dt></span></span> </dl>                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span><dl> <span data-ttu-id="fcafa-219"><dt>**Виртуальная ленточная библиотека**</dt> <dt>34</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-219"><dt>**Virtual Tape Library**</dt> <dt>34</dt></span></span> </dl>                         | <span data-ttu-id="fcafa-220">Эмуляция ленточной библиотеки с помощью виртуальной системы библиотеки.</span><span class="sxs-lookup"><span data-stu-id="fcafa-220">The emulation of a tape library by a Virtual Library System.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span><dl> <span data-ttu-id="fcafa-221"><dt>**Виртуальная система библиотеки**</dt> <dt>35</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-221"><dt>**Virtual Library System**</dt> <dt>35</dt></span></span> </dl>                 | <span data-ttu-id="fcafa-222">Использует дисковый накопитель для эмуляции ленточных библиотек.</span><span class="sxs-lookup"><span data-stu-id="fcafa-222">Uses disk storage to emulate tape libraries.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span><dl> <span data-ttu-id="fcafa-223"><dt>**Сетевой компьютер или тонкий клиент**</dt> <dt>36</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-223"><dt>**Network PC/Thin Client**</dt> <dt>36</dt></span></span> </dl>                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span><dl> <span data-ttu-id="fcafa-224"><dt>**Коммутатор FC**</dt> <dt>37</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-224"><dt>**FC Switch**</dt> <dt>37</dt></span></span> </dl>                                                                     | <span data-ttu-id="fcafa-225">Указывает, что этот экземпляр выделен для переключения кадров уровня 2 Fibre Channel.</span><span class="sxs-lookup"><span data-stu-id="fcafa-225">Indicates this instance is dedicated to switching layer 2 Fibre Channel frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span><dl> <span data-ttu-id="fcafa-226"><dt>**Коммутатор Ethernet**</dt> <dt>38</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-226"><dt>**Ethernet Switch**</dt> <dt>38</dt></span></span> </dl>                                             | <span data-ttu-id="fcafa-227">Указывает, что этот экземпляр предназначен для переключения кадров Ethernet уровня 2.</span><span class="sxs-lookup"><span data-stu-id="fcafa-227">Indicates this instance is dedicated to switching layer 2 Ethernet frames.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="fcafa-228"><dt>**Зарезервированный DMTF**</dt> <dt>39.. 32567</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-228"><dt>**DMTF Reserved**</dt> <dt>39..32567</dt></span></span> </dl>                                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="fcafa-229"><dt> **Поставщик зарезервированных**</dt> <dt>32568.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-229"><dt>**Vendor Reserved** </dt> <dt>32568..65535</dt></span></span> </dl>                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="fcafa-230">**Описание**</span><span class="sxs-lookup"><span data-stu-id="fcafa-230">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-231">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-231">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-232">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-232">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-233">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="fcafa-233">A description of the object.</span></span> <span data-ttu-id="fcafa-234">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "плановая виртуальная машина Майкрософт".</span><span class="sxs-lookup"><span data-stu-id="fcafa-234">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Microsoft Planned Virtual Machine".</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-235">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="fcafa-235">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-236">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-237">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-238">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="fcafa-238">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="fcafa-239">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="fcafa-239">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fcafa-240">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-240">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-241">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fcafa-241">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-242">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-243">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-244">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="fcafa-244">A display name for the object.</span></span> <span data-ttu-id="fcafa-245">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-245">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-246">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="fcafa-246">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-247">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-248">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-249">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="fcafa-249">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="fcafa-250">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fcafa-250">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and can be one of the following values.</span></span>



| <span data-ttu-id="fcafa-251">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="fcafa-252">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-252">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fcafa-253"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-253"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="fcafa-254">Система отключена.</span><span class="sxs-lookup"><span data-stu-id="fcafa-254">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="fcafa-255"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-255"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="fcafa-256">Система включена, но в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="fcafa-256">The system is enabled, but offline.</span></span> <span data-ttu-id="fcafa-257">Все новые запросы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="fcafa-257">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fcafa-258">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fcafa-258">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-259">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-259">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-260">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-260">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-261">Указывает включенное состояние запланированной системы.</span><span class="sxs-lookup"><span data-stu-id="fcafa-261">Specifies the enabled state of the planned system.</span></span> <span data-ttu-id="fcafa-262">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fcafa-262">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it can be one of the following values.</span></span>



| <span data-ttu-id="fcafa-263">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-263">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="fcafa-264">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-264">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fcafa-265"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-265"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="fcafa-266">Система отключена.</span><span class="sxs-lookup"><span data-stu-id="fcafa-266">The system is turned off.</span></span><br/>                                             |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="fcafa-267"><dt>**Включено, но отключено**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-267"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="fcafa-268">Система включена, но в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="fcafa-268">The system is enabled, but offline.</span></span> <span data-ttu-id="fcafa-269">Все новые запросы будут удалены.</span><span class="sxs-lookup"><span data-stu-id="fcafa-269">Any new requests will be dropped.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fcafa-270">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="fcafa-270">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-271">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-271">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-272">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-272">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-273">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="fcafa-273">The current health of the element.</span></span> <span data-ttu-id="fcafa-274">Это свойство выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="fcafa-274">This property expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="fcafa-275">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="fcafa-275">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="fcafa-276">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="fcafa-276">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>



| <span data-ttu-id="fcafa-277">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-277">Value</span></span>                                                                        | <span data-ttu-id="fcafa-278">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-278">Meaning</span></span>                                 |
|------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="fcafa-279"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-279"><dt>5</dt></span></span> </dl> | <span data-ttu-id="fcafa-280">Состояние работоспособности — нормальное.</span><span class="sxs-lookup"><span data-stu-id="fcafa-280">The health status is normal.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fcafa-281">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fcafa-281">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-282">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fcafa-282">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-283">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-283">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-284">Массив строк, предоставляющий объяснения и подробные сведения, лежащие в основе записей в массиве **осеридентифингинфо** .</span><span class="sxs-lookup"><span data-stu-id="fcafa-284">An array of strings providing explanations and details behind the entries in the **OtherIdentifyingInfo** array.</span></span> <span data-ttu-id="fcafa-285">Каждая запись этого массива связана с записью в **осеридентифингинфо** , расположенной в том же индексе.</span><span class="sxs-lookup"><span data-stu-id="fcafa-285">Each entry of this array is related to the entry in **OtherIdentifyingInfo** that is located at the same index.</span></span> <span data-ttu-id="fcafa-286">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-286">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-287">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fcafa-287">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-288">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fcafa-288">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-289">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-289">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-290">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fcafa-290">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="fcafa-291">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-291">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-292">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fcafa-292">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-293">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-293">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-294">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-294">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-295">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="fcafa-295">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-296">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="fcafa-296">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fcafa-297">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-297">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-298">**Name**</span><span class="sxs-lookup"><span data-stu-id="fcafa-298">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-299">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-299">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-300">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-301">Квалификаторы: **ключ**, **Переопределение**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="fcafa-301">Qualifiers: **Key**, **Override**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-302">Унаследованное имя выступает в качестве ключа экземпляра системы в среде предприятия.</span><span class="sxs-lookup"><span data-stu-id="fcafa-302">The inherited name serves as the key of a system instance in an enterprise environment.</span></span> <span data-ttu-id="fcafa-303">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-303">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-304">**намеформат**</span><span class="sxs-lookup"><span data-stu-id="fcafa-304">**NameFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-305">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-305">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-306">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-306">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-307">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="fcafa-307">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-308">Определяет, каким способом было создано системное имя, с помощью эвристики подкласса.</span><span class="sxs-lookup"><span data-stu-id="fcafa-308">Identifies how the system name was generated, using the heuristic of the subclass.</span></span> <span data-ttu-id="fcafa-309">Системный объект и его производные являются объектами верхнего уровня CIM.</span><span class="sxs-lookup"><span data-stu-id="fcafa-309">The system object and its derivatives are top-level objects of CIM.</span></span> <span data-ttu-id="fcafa-310">Они предоставляют область для множества компонентов.</span><span class="sxs-lookup"><span data-stu-id="fcafa-310">They provide the scope for numerous components.</span></span> <span data-ttu-id="fcafa-311">Требуются уникальные системные ключи.</span><span class="sxs-lookup"><span data-stu-id="fcafa-311">Having unique system keys is required.</span></span> <span data-ttu-id="fcafa-312">Эвристику можно определить в отдельных подклассах системы, чтобы попытаться всегда создавать один и тот же ключ системного имени.</span><span class="sxs-lookup"><span data-stu-id="fcafa-312">A heuristic can be defined in individual system subclasses to attempt to always generate the same system name key.</span></span> <span data-ttu-id="fcafa-313">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-313">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-314">**онтимеинмиллисекондс**</span><span class="sxs-lookup"><span data-stu-id="fcafa-314">**OnTimeInMilliseconds**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-315">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fcafa-315">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-316">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-316">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-317">Квалификаторы: [**единицы**](/windows/desktop/WmiSdk/standard-qualifiers) ("миллисекунды")</span><span class="sxs-lookup"><span data-stu-id="fcafa-317">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("MilliSeconds")</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-318">Общее время в миллисекундах с момента последнего включения, сброса или восстановления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fcafa-318">The total time, in milliseconds, since the virtual machine was last turned on, reset, or restored.</span></span> <span data-ttu-id="fcafa-319">В этот раз исключается время, в течение которого виртуальная машина находилась в приостановленном состоянии.</span><span class="sxs-lookup"><span data-stu-id="fcafa-319">This time excludes the time the virtual machine was in the paused state.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-320">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="fcafa-320">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-321">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-321">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-322">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-322">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-323">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="fcafa-323">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="fcafa-324">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="fcafa-324">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fcafa-325">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-325">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-326">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="fcafa-326">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-327">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="fcafa-327">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-328">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-328">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-329">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="fcafa-329">The current statuses of the object.</span></span> <span data-ttu-id="fcafa-330">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение 2 (ОК).</span><span class="sxs-lookup"><span data-stu-id="fcafa-330">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to 2 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-331">**OtherDedicatedDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fcafa-331">**OtherDedicatedDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-332">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fcafa-332">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-333">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-333">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-334">Строка, описывающая, как или почему система выделяется, когда выделенный массив включает значение 2, "Other".</span><span class="sxs-lookup"><span data-stu-id="fcafa-334">A string describing how or why the system is dedicated when the Dedicated array includes the value 2, "Other".</span></span> <span data-ttu-id="fcafa-335">Это свойство наследуется от класса [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-335">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-336">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="fcafa-336">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-337">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-337">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-338">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-338">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-339">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 ("другое").</span><span class="sxs-lookup"><span data-stu-id="fcafa-339">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 ("Other").</span></span> <span data-ttu-id="fcafa-340">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="fcafa-340">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="fcafa-341">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="fcafa-341">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-342">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="fcafa-342">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-343">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fcafa-343">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-344">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-345">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="fcafa-345">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-346">Содержит дополнительные данные, помимо сведений о системных именах, которые можно использовать для обнаружения компьютерной системы.</span><span class="sxs-lookup"><span data-stu-id="fcafa-346">Contains additional data, beyond system name information, that can be used to identify a ComputerSystem.</span></span> <span data-ttu-id="fcafa-347">В качестве примера можно привести Fibre Channel WWN-имени узла.</span><span class="sxs-lookup"><span data-stu-id="fcafa-347">One example would be to hold the Fibre Channel World-Wide Name (WWN) of a node.</span></span> <span data-ttu-id="fcafa-348">Если доступно только имя Fibre Channel и оно является уникальным (его можно использовать в качестве системного ключа), то это свойство будет иметь **значение NULL** , а WWN станет системным ключом, его данные помещаются в свойство **Name** .</span><span class="sxs-lookup"><span data-stu-id="fcafa-348">If only the Fibre Channel name is available and is unique (able to be used as the system key), then this property would be **Null** and the WWN would become the system key, its data placed in the **Name** property.</span></span> <span data-ttu-id="fcafa-349">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-349">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-350">**поверманажементкапабилитиес**</span><span class="sxs-lookup"><span data-stu-id="fcafa-350">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-351">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="fcafa-351">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-352">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-352">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-353">Это свойство наследуется от класса [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , но не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fcafa-353">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class, but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-354">**примарйовнерконтакт**</span><span class="sxs-lookup"><span data-stu-id="fcafa-354">**PrimaryOwnerContact**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-355">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-355">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-356">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcafa-356">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-357">Квалификаторы: **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="fcafa-357">Qualifiers: **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-358">Строка, которая предоставляет сведения о том, как может быть достигнут первичный владелец системы (например, номер телефона, адрес электронной почты и т. д.).</span><span class="sxs-lookup"><span data-stu-id="fcafa-358">A string that provides information on how the primary system owner can be reached (for example, phone number, email address, and so on).</span></span> <span data-ttu-id="fcafa-359">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-359">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-360">**примарйовнернаме**</span><span class="sxs-lookup"><span data-stu-id="fcafa-360">**PrimaryOwnerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-361">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-362">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcafa-362">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-363">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="fcafa-363">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-364">Имя основного владельца системы.</span><span class="sxs-lookup"><span data-stu-id="fcafa-364">The name of the primary system owner.</span></span> <span data-ttu-id="fcafa-365">Владельцем системы является основной пользователь системы.</span><span class="sxs-lookup"><span data-stu-id="fcafa-365">The system owner is the primary user of the system.</span></span> <span data-ttu-id="fcafa-366">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-366">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-367">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="fcafa-367">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-368">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-368">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-369">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-369">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-370">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="fcafa-370">Provides high level status information.</span></span> <span data-ttu-id="fcafa-371">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="fcafa-371">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="fcafa-372">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="fcafa-372">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fcafa-373">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fcafa-373">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-374">**ProcessID**</span><span class="sxs-lookup"><span data-stu-id="fcafa-374">**ProcessID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-375">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fcafa-375">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-376">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-376">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-377">Идентификатор процесса, в котором выполняется эта виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="fcafa-377">The identifier of the process under which this virtual machine is running.</span></span> <span data-ttu-id="fcafa-378">Это значение можно использовать для уникальной идентификации экземпляра Vmwp.exe в системе, где работает виртуальная машина.</span><span class="sxs-lookup"><span data-stu-id="fcafa-378">This value can be used to uniquely identify the instance of Vmwp.exe on the system that is running the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-379">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="fcafa-379">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-380">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-381">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-382">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="fcafa-382">The last requested or desired state for the element.</span></span> <span data-ttu-id="fcafa-383">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="fcafa-383">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="fcafa-384">Это свойство предназначено для сравнения последнего запрошенного и текущего состояний элемента.</span><span class="sxs-lookup"><span data-stu-id="fcafa-384">This property is provided to compare the last requested and current states for an element.</span></span> <span data-ttu-id="fcafa-385">Конкретный экземпляр класса [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать свойство **RequestedState** .</span><span class="sxs-lookup"><span data-stu-id="fcafa-385">A particular instance of the [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) class might not support the **RequestedState** property.</span></span> <span data-ttu-id="fcafa-386">В этом случае используется значение 12 ("неприменимо").</span><span class="sxs-lookup"><span data-stu-id="fcafa-386">If this occurs, the value 12 ("Not Applicable") is used.</span></span> <span data-ttu-id="fcafa-387">Это свойство наследуется от **CIM \_ енабледлогикалелемент** и всегда имеет значение 12 (неприменимо).</span><span class="sxs-lookup"><span data-stu-id="fcafa-387">This property is inherited from **CIM\_EnabledLogicalElement**, and it is always set to 12 (Not Applicable).</span></span>



| <span data-ttu-id="fcafa-388">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-388">Value</span></span>                                                                         | <span data-ttu-id="fcafa-389">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-389">Meaning</span></span>                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="fcafa-390"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-390"><dt>12</dt></span></span> </dl> | <span data-ttu-id="fcafa-391">Не применяется</span><span class="sxs-lookup"><span data-stu-id="fcafa-391">Not applicable.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fcafa-392">**ресеткапабилити**</span><span class="sxs-lookup"><span data-stu-id="fcafa-392">**ResetCapability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-393">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-393">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-394">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-394">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-395">Указывает возможности сброса системы компьютера.</span><span class="sxs-lookup"><span data-stu-id="fcafa-395">Specifies the reset capabilities of the computer system.</span></span> <span data-ttu-id="fcafa-396">Это свойство наследуется от класса [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-396">This property is inherited from the [**CIM\_ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) class.</span></span>



| <span data-ttu-id="fcafa-397">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-397">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="fcafa-398">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-398">Meaning</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="fcafa-399"><dt>**Другое**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-399"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                              |                                                                                                            |
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fcafa-400"><dt>**Неизвестно**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-400"><dt>**Unknown**</dt> <dt>2</dt></span></span> </dl>                                      |                                                                                                            |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fcafa-401"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-401"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                  | <span data-ttu-id="fcafa-402">Аппаратный сброс не разрешен.</span><span class="sxs-lookup"><span data-stu-id="fcafa-402">Hardware reset is not allowed.</span></span> <br/>                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="fcafa-403"><dt>**Включено**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-403"><dt>**Enabled**</dt> <dt>4</dt></span></span> </dl>                                      | <span data-ttu-id="fcafa-404">Компьютерную систему можно сбросить с помощью оборудования (например, кнопки питания и сброса).</span><span class="sxs-lookup"><span data-stu-id="fcafa-404">The computer system can be reset by using hardware (for example, the power and reset buttons).</span></span> <br/> |
| <span id="Not_Implemented_"></span><span id="not_implemented_"></span><span id="NOT_IMPLEMENTED_"></span><dl> <span data-ttu-id="fcafa-405"><dt> **Не реализовано**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-405"><dt>**Not Implemented** </dt> <dt>5 </dt></span></span> </dl> |                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="fcafa-406">**Роли**</span><span class="sxs-lookup"><span data-stu-id="fcafa-406">**Roles**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-407">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fcafa-407">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-408">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="fcafa-408">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-409">Массив строк, указывающий определяемые администратором роли, которые эта система играет в управляемой среде.</span><span class="sxs-lookup"><span data-stu-id="fcafa-409">An array of strings that specifies the administrator-defined roles this system plays in the managed environment.</span></span> <span data-ttu-id="fcafa-410">Примерами могут быть "создание 8 сервера печати" или "Боисе User Directory".</span><span class="sxs-lookup"><span data-stu-id="fcafa-410">Examples might be "Building 8 print server" or "Boise user directories".</span></span> <span data-ttu-id="fcafa-411">Одна система может выполнять несколько ролей.</span><span class="sxs-lookup"><span data-stu-id="fcafa-411">A single system may perform multiple roles.</span></span> <span data-ttu-id="fcafa-412">Представление инструментирования ролей системы определяется путем создания экземпляра определенного подкласса System, свойств в подклассе или и того и другого.</span><span class="sxs-lookup"><span data-stu-id="fcafa-412">The instrumentation view of the roles of a system is defined by instantiating a specific subclass of system, or by properties in a subclass, or both.</span></span> <span data-ttu-id="fcafa-413">Например, назначение ComputerSystem определяется с помощью **выделенных** свойств и **осердедикатеддескриптион** .</span><span class="sxs-lookup"><span data-stu-id="fcafa-413">For example, the purpose of a ComputerSystem is defined using the **Dedicated** and **OtherDedicatedDescription** properties.</span></span> <span data-ttu-id="fcafa-414">Это свойство наследуется от [**класса \_ системы CIM**](/windows/desktop/CIMWin32Prov/cim-system) .</span><span class="sxs-lookup"><span data-stu-id="fcafa-414">This property is inherited from the [**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system) class.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-415">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="fcafa-415">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-416">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="fcafa-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-417">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-418">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="fcafa-418">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-419">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="fcafa-419">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-420">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="fcafa-420">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-421">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-421">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-422">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="fcafa-422">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="fcafa-423">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), и каждый элемент массива всегда имеет значение "служба работает нормально".</span><span class="sxs-lookup"><span data-stu-id="fcafa-423">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and each array element is always set to "The service is running normally".</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-424">**тимеофластконфигуратиончанже**</span><span class="sxs-lookup"><span data-stu-id="fcafa-424">**TimeOfLastConfigurationChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-425">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fcafa-425">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-426">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-426">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-427">Дата и время последнего изменения файла конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fcafa-427">The date and time when the virtual machine configuration file was last modified.</span></span> <span data-ttu-id="fcafa-428">Файл конфигурации изменяется во время определенных операций виртуальной машины, а также при добавлении, изменении или удалении любой из параметров виртуальной машины или устройства.</span><span class="sxs-lookup"><span data-stu-id="fcafa-428">The configuration file is modified during certain virtual machine operations, as well as when any of the virtual machine or device settings are added, modified, or removed.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-429">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="fcafa-429">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-430">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fcafa-430">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-431">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-431">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-432">Дата и время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="fcafa-432">The date and time when the enabled state of the element last changed.</span></span> <span data-ttu-id="fcafa-433">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)), но не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="fcafa-433">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="fcafa-434">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="fcafa-434">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fcafa-435">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fcafa-435">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fcafa-436">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="fcafa-436">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fcafa-437">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="fcafa-437">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="fcafa-438">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fcafa-438">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="fcafa-439">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-439">Value</span></span>                                                                                                                                                                                                                                                     | <span data-ttu-id="fcafa-440">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-440">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fcafa-441"><dt>**Неизвестно**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-441"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                               |                                                                                  |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="fcafa-442"><dt>**Включено**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-442"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                               |                                                                                  |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fcafa-443"><dt>**Отключено**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-443"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                           |                                                                                  |
| <span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span><dl> <span data-ttu-id="fcafa-444"><dt>**Завершение работы**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-444"><dt>**Shut Down**</dt> <dt>4</dt></span></span> </dl>                       |                                                                                  |
| <span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span><dl> <span data-ttu-id="fcafa-445"><dt>**Нет изменений**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-445"><dt>**No Change**</dt> <dt>5</dt></span></span> </dl>                       | <span data-ttu-id="fcafa-446">Переход не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fcafa-446">No transition is in progress.</span></span><br/>                                         |
| <span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span><dl> <span data-ttu-id="fcafa-447"><dt>**Автономный режим**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-447"><dt>**Offline**</dt> <dt>6</dt></span></span> </dl>                               |                                                                                  |
| <span id="Test"></span><span id="test"></span><span id="TEST"></span><dl> <span data-ttu-id="fcafa-448"><dt>**Тест**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-448"><dt>**Test**</dt> <dt>7</dt></span></span> </dl>                                           |                                                                                  |
| <span id="Defer"></span><span id="defer"></span><span id="DEFER"></span><dl> <span data-ttu-id="fcafa-449"><dt>**Отложить**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-449"><dt>**Defer**</dt> <dt>8</dt></span></span> </dl>                                       |                                                                                  |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="fcafa-450"><dt>**Замораживание**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-450"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                               |                                                                                  |
| <span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span><dl> <span data-ttu-id="fcafa-451"><dt>**Перезагрузка**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-451"><dt>**Reboot**</dt> <dt>10</dt></span></span> </dl>                                  |                                                                                  |
| <span id="Reset"></span><span id="reset"></span><span id="RESET"></span><dl> <span data-ttu-id="fcafa-452"><dt>**Сброс**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-452"><dt>**Reset**</dt> <dt>11</dt></span></span> </dl>                                      |                                                                                  |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="fcafa-453"><dt>**Не применимо**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-453"><dt>**Not Applicable**</dt> <dt>12</dt></span></span> </dl>  | <span data-ttu-id="fcafa-454">Реализация не поддерживает представление текущих переходов.</span><span class="sxs-lookup"><span data-stu-id="fcafa-454">The implementation does not support representing ongoing transitions.</span></span><br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="fcafa-455"><dt> **Зарезервировано DMTF**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-455"><dt>**DMTF Reserved** </dt> <dt>.. </dt></span></span> </dl> |                                                                                  |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fcafa-456">Требования</span><span class="sxs-lookup"><span data-stu-id="fcafa-456">Requirements</span></span>



| <span data-ttu-id="fcafa-457">Требование</span><span class="sxs-lookup"><span data-stu-id="fcafa-457">Requirement</span></span> | <span data-ttu-id="fcafa-458">Значение</span><span class="sxs-lookup"><span data-stu-id="fcafa-458">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcafa-459">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fcafa-459">Minimum supported client</span></span><br/> | <span data-ttu-id="fcafa-460">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="fcafa-460">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fcafa-461">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fcafa-461">Minimum supported server</span></span><br/> | <span data-ttu-id="fcafa-462">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="fcafa-462">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fcafa-463">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="fcafa-463">Namespace</span></span><br/>                | <span data-ttu-id="fcafa-464">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="fcafa-464">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fcafa-465">MOF</span><span class="sxs-lookup"><span data-stu-id="fcafa-465">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fcafa-466"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-466"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fcafa-467">DLL</span><span class="sxs-lookup"><span data-stu-id="fcafa-467">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcafa-468"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fcafa-468"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fcafa-469">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fcafa-469">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fcafa-470">**CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="fcafa-470">**CIM\_ComputerSystem**</span></span>](cim-computersystem.md)
</dt> <dt>

[<span data-ttu-id="fcafa-471">**Мсвм \_ виртуалсистемманажементсервице. Метод Импортсистемдефинитион**</span><span class="sxs-lookup"><span data-stu-id="fcafa-471">**Msvm\_VirtualSystemManagementService .ImportSystemDefinition method**</span></span>](importsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

