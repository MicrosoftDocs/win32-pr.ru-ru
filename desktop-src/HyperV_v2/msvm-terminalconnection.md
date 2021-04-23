---
description: Указывает состояние активного удаленного сеанса, взаимодействующего с виртуальной машиной.
ms.assetid: EAE6082F-A0CB-4E75-8029-51E20649C0A8
title: Класс Msvm_TerminalConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalConnection
- Msvm_TerminalConnection.InstanceID
- Msvm_TerminalConnection.Caption
- Msvm_TerminalConnection.Description
- Msvm_TerminalConnection.ElementName
- Msvm_TerminalConnection.InstallDate
- Msvm_TerminalConnection.Name
- Msvm_TerminalConnection.OperationalStatus
- Msvm_TerminalConnection.StatusDescriptions
- Msvm_TerminalConnection.Status
- Msvm_TerminalConnection.HealthState
- Msvm_TerminalConnection.CommunicationStatus
- Msvm_TerminalConnection.DetailedStatus
- Msvm_TerminalConnection.OperatingStatus
- Msvm_TerminalConnection.PrimaryStatus
- Msvm_TerminalConnection.EnabledState
- Msvm_TerminalConnection.OtherEnabledState
- Msvm_TerminalConnection.RequestedState
- Msvm_TerminalConnection.EnabledDefault
- Msvm_TerminalConnection.TimeOfLastStateChange
- Msvm_TerminalConnection.AvailableRequestedStates
- Msvm_TerminalConnection.TransitioningToState
- Msvm_TerminalConnection.ConnectionID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 66be5000fb7fdd4404e07c87673e3359065af6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817096"
---
# <a name="msvm_terminalconnection-class"></a><span data-ttu-id="ae503-103">\_Класс мсвм терминалконнектион</span><span class="sxs-lookup"><span data-stu-id="ae503-103">Msvm\_TerminalConnection class</span></span>

<span data-ttu-id="ae503-104">Указывает состояние активного удаленного сеанса, взаимодействующего с виртуальной машиной.</span><span class="sxs-lookup"><span data-stu-id="ae503-104">Indicates the state of an active remote session interacting with a virtual machine.</span></span> <span data-ttu-id="ae503-105">В каждый момент времени может быть только одно подключение.</span><span class="sxs-lookup"><span data-stu-id="ae503-105">There can only be one connection at a time.</span></span>

<span data-ttu-id="ae503-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ae503-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae503-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae503-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TerminalConnection : CIM_EnabledLogicalElement
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState = 12;
  string   ConnectionID;
};
```

## <a name="members"></a><span data-ttu-id="ae503-108">Члены</span><span class="sxs-lookup"><span data-stu-id="ae503-108">Members</span></span>

<span data-ttu-id="ae503-109">Класс **мсвм \_ терминалконнектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ae503-109">The **Msvm\_TerminalConnection** class has these types of members:</span></span>

-   [<span data-ttu-id="ae503-110">Методы</span><span class="sxs-lookup"><span data-stu-id="ae503-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="ae503-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae503-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ae503-112">Методы</span><span class="sxs-lookup"><span data-stu-id="ae503-112">Methods</span></span>

<span data-ttu-id="ae503-113">Класс **мсвм \_ терминалконнектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ae503-113">The **Msvm\_TerminalConnection** class has these methods.</span></span>



| <span data-ttu-id="ae503-114">Метод</span><span class="sxs-lookup"><span data-stu-id="ae503-114">Method</span></span>                                                                   | <span data-ttu-id="ae503-115">Описание</span><span class="sxs-lookup"><span data-stu-id="ae503-115">Description</span></span>                         |
|:-------------------------------------------------------------------------|:------------------------------------|
| [<span data-ttu-id="ae503-116">**Равен**</span><span class="sxs-lookup"><span data-stu-id="ae503-116">**RequestStateChange**</span></span>](msvm-terminalconnection-requeststatechange.md) | <span data-ttu-id="ae503-117">Запрашивает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="ae503-117">Requests a state change.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ae503-118">Свойства</span><span class="sxs-lookup"><span data-stu-id="ae503-118">Properties</span></span>

<span data-ttu-id="ae503-119">Класс **мсвм \_ терминалконнектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ae503-119">The **Msvm\_TerminalConnection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ae503-120">**аваилаблерекуестедстатес**</span><span class="sxs-lookup"><span data-stu-id="ae503-120">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-121">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ae503-121">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae503-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-123">Указывает возможные значения для параметра *RequestedState* метода **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="ae503-123">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="ae503-124">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ae503-124">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ae503-125">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="ae503-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-128">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ae503-128">A short description of the object.</span></span> <span data-ttu-id="ae503-129">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-129">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-130">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="ae503-130">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-131">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-131">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-133">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="ae503-133">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="ae503-134">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ae503-134">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae503-135">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-135">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae503-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ae503-136"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ae503-137"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Связь хорошо** (2)</span><span class="sxs-lookup"><span data-stu-id="ae503-138"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Потеря связи** (3)</span><span class="sxs-lookup"><span data-stu-id="ae503-139"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Нет контакта** (4)</span><span class="sxs-lookup"><span data-stu-id="ae503-140"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ae503-141"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ae503-142"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae503-143">)</span><span class="sxs-lookup"><span data-stu-id="ae503-143">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae503-144">**ConnectionID**</span><span class="sxs-lookup"><span data-stu-id="ae503-144">**ConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae503-147">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ae503-147">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ae503-148">Уникальный идентификатор экземпляра объекта подключения терминала.</span><span class="sxs-lookup"><span data-stu-id="ae503-148">The unique identifier for an instance of the terminal connection object.</span></span> <span data-ttu-id="ae503-149">Идентификатор имеет форму "Microsoft:*VMID* \\ *index*".</span><span class="sxs-lookup"><span data-stu-id="ae503-149">The identifier is of the form "Microsoft:*VMID*\\*Index*".</span></span> <span data-ttu-id="ae503-150">Например, "Microsoft: 67A5D397-A02D-11DB-AC13-001676AA34F0 \\ 0".</span><span class="sxs-lookup"><span data-stu-id="ae503-150">For example, "Microsoft:67A5D397-A02D-11DB-AC13-001676AA34F0\\0".</span></span>

</dd> <dt>

<span data-ttu-id="ae503-151">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ae503-151">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-152">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-154">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="ae503-154">A description of the object.</span></span> <span data-ttu-id="ae503-155">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-156">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="ae503-156">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-157">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-157">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-159">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="ae503-159">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="ae503-160">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ae503-160">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae503-161">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-161">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae503-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (0)</span><span class="sxs-lookup"><span data-stu-id="ae503-162"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**Нет дополнительных сведений** (1)</span><span class="sxs-lookup"><span data-stu-id="ae503-163"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Пренапряжении** (2)</span><span class="sxs-lookup"><span data-stu-id="ae503-164"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Прогнозируемый сбой** (3)</span><span class="sxs-lookup"><span data-stu-id="ae503-165"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Неустранимая ошибка** (4)</span><span class="sxs-lookup"><span data-stu-id="ae503-166"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Ошибка вспомогательной сущности** (5)</span><span class="sxs-lookup"><span data-stu-id="ae503-167"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ae503-168"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ae503-169"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae503-170">)</span><span class="sxs-lookup"><span data-stu-id="ae503-170">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae503-171">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ae503-171">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-172">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-174">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="ae503-174">A display name for the object.</span></span> <span data-ttu-id="ae503-175">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-175">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-176">**енабледдефаулт**</span><span class="sxs-lookup"><span data-stu-id="ae503-176">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-177">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-177">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-179">Конфигурация по умолчанию или запуска администратора для включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ae503-179">An administrator's default or startup configuration for the enabled state of an element.</span></span> <span data-ttu-id="ae503-180">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae503-180">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ae503-181">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-181">Value</span></span>                                                                        | <span data-ttu-id="ae503-182">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-182">Meaning</span></span>             |
|------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="ae503-183"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-183"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ae503-184">Активировано</span><span class="sxs-lookup"><span data-stu-id="ae503-184">Enabled</span></span><br/>  |
| <dl> <span data-ttu-id="ae503-185"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-185"><dt>3</dt></span></span> </dl> | <span data-ttu-id="ae503-186">Выключено</span><span class="sxs-lookup"><span data-stu-id="ae503-186">Disabled</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae503-187">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="ae503-187">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-188">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-188">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-189">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-190">Включенные и отключенные состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ae503-190">The enabled and disabled states of an element.</span></span> <span data-ttu-id="ae503-191">Он также может указывать на переходы между этими запрошенными состояниями.</span><span class="sxs-lookup"><span data-stu-id="ae503-191">It can also indicate the transitions between these requested states.</span></span> <span data-ttu-id="ae503-192">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae503-192">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ae503-193">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-193">Value</span></span>                                                                        | <span data-ttu-id="ae503-194">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-194">Meaning</span></span>                   |
|------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae503-195"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-195"><dt>2</dt></span></span> </dl> | <span data-ttu-id="ae503-196">Активировано</span><span class="sxs-lookup"><span data-stu-id="ae503-196">Enabled</span></span><br/>        |
| <dl> <span data-ttu-id="ae503-197"><dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-197"><dt>3</dt></span></span> </dl> | <span data-ttu-id="ae503-198">Выключено</span><span class="sxs-lookup"><span data-stu-id="ae503-198">Disabled</span></span><br/>       |
| <dl> <span data-ttu-id="ae503-199"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-199"><dt>5</dt></span></span> </dl> | <span data-ttu-id="ae503-200">Не применимо</span><span class="sxs-lookup"><span data-stu-id="ae503-200">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae503-201">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="ae503-201">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-202">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-202">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-203">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-204">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="ae503-204">The current health of the element.</span></span> <span data-ttu-id="ae503-205">Этот атрибут выражает работоспособность этого элемента, но не обязательно для его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ae503-205">This attribute expresses the health of this element but not necessarily that of its subcomponents.</span></span> <span data-ttu-id="ae503-206">Возможные значения: от 0 до 30, где 5 означает, что элемент полностью работоспособен, а 30 означает, что элемент полностью нефункциональный.</span><span class="sxs-lookup"><span data-stu-id="ae503-206">The possible values are 0 to 30, where 5 means the element is entirely healthy and 30 means the element is completely nonfunctional.</span></span> <span data-ttu-id="ae503-207">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 (ОК).</span><span class="sxs-lookup"><span data-stu-id="ae503-207">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 (OK).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-208">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="ae503-208">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-209">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae503-209">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-210">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-210">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-211">Дата и время создания конфигурации виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ae503-211">The date and time the virtual machine configuration was created.</span></span> <span data-ttu-id="ae503-212">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-212">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-213">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ae503-213">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-214">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-214">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-215">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-215">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ae503-216">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="ae503-216">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ae503-217">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="ae503-217">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ae503-218">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-218">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-219">**Name**</span><span class="sxs-lookup"><span data-stu-id="ae503-219">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-220">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-220">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-222">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="ae503-222">The label by which the object is known.</span></span> <span data-ttu-id="ae503-223">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и совпадает со свойством **ElementName** .</span><span class="sxs-lookup"><span data-stu-id="ae503-223">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is the same as the **ElementName** property.</span></span>

</dd> <dt>

<span data-ttu-id="ae503-224">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="ae503-224">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-225">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-225">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-226">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-227">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="ae503-227">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="ae503-228">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ae503-228">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae503-229">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-229">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae503-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ae503-230"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Недоступно** (1)</span><span class="sxs-lookup"><span data-stu-id="ae503-231"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Обслуживание** (2)</span><span class="sxs-lookup"><span data-stu-id="ae503-232"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Запуск** (3)</span><span class="sxs-lookup"><span data-stu-id="ae503-233"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Остановка** (4)</span><span class="sxs-lookup"><span data-stu-id="ae503-234"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Остановлено** (5)</span><span class="sxs-lookup"><span data-stu-id="ae503-235"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Прервано** (6)</span><span class="sxs-lookup"><span data-stu-id="ae503-236"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Неактивный** (7)</span><span class="sxs-lookup"><span data-stu-id="ae503-237"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Завершено** (8)</span><span class="sxs-lookup"><span data-stu-id="ae503-238"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Миграция** (9)</span><span class="sxs-lookup"><span data-stu-id="ae503-239"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Емигратинг** (10)</span><span class="sxs-lookup"><span data-stu-id="ae503-240"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Перемиграция** (11)</span><span class="sxs-lookup"><span data-stu-id="ae503-241"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Значит** (12)</span><span class="sxs-lookup"><span data-stu-id="ae503-242"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Завершение работы** (13)</span><span class="sxs-lookup"><span data-stu-id="ae503-243"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**В тесте** (14)</span><span class="sxs-lookup"><span data-stu-id="ae503-244"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Переход** (15)</span><span class="sxs-lookup"><span data-stu-id="ae503-245"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**В службе** (16)</span><span class="sxs-lookup"><span data-stu-id="ae503-246"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ae503-247"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ae503-248"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae503-249">)</span><span class="sxs-lookup"><span data-stu-id="ae503-249">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae503-250">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="ae503-250">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-251">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="ae503-251">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ae503-252">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-252">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-253">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ae503-253">The current statuses of the object.</span></span> <span data-ttu-id="ae503-254">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-254">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-255">**осеренабледстате**</span><span class="sxs-lookup"><span data-stu-id="ae503-255">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-256">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-256">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-257">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-257">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-258">Строка, описывающая включенное или отключенное состояние элемента, если свойство **EnabledState** имеет значение 1 (другое).</span><span class="sxs-lookup"><span data-stu-id="ae503-258">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="ae503-259">Для этого свойства необходимо задать значение **null** , если параметр **EnabledState** имеет любое значение, отличное от 1.</span><span class="sxs-lookup"><span data-stu-id="ae503-259">This property must be set to **Null** when **EnabledState** is any value other than 1.</span></span> <span data-ttu-id="ae503-260">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ae503-260">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ae503-261">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="ae503-261">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-262">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-263">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-264">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="ae503-264">Provides high level status information.</span></span> <span data-ttu-id="ae503-265">Это свойство следует использовать вместе со свойством **детаиледстатус** , чтобы обеспечить высокий уровень и подробные сведения о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="ae503-265">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="ae503-266">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="ae503-266">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="ae503-267">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-267">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="ae503-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="ae503-268"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-269"><span id="OK"></span><span id="ok"></span>**ОК** (1)</span><span class="sxs-lookup"><span data-stu-id="ae503-269"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>С **пониженной производительностью** (2)</span><span class="sxs-lookup"><span data-stu-id="ae503-270"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Ошибка** (3)</span><span class="sxs-lookup"><span data-stu-id="ae503-271"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)</span><span class="sxs-lookup"><span data-stu-id="ae503-272"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ae503-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Поставщик зарезервирован** (0x8000..</span><span class="sxs-lookup"><span data-stu-id="ae503-273"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="ae503-274">)</span><span class="sxs-lookup"><span data-stu-id="ae503-274">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="ae503-275">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="ae503-275">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-276">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-276">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-277">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-277">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-278">Последнее запрошенное или требуемое состояние элемента.</span><span class="sxs-lookup"><span data-stu-id="ae503-278">The last requested or desired state for the element.</span></span> <span data-ttu-id="ae503-279">Фактическое состояние элемента представлено параметром **EnabledState**.</span><span class="sxs-lookup"><span data-stu-id="ae503-279">The actual state of the element is represented by **EnabledState**.</span></span> <span data-ttu-id="ae503-280">Это свойство предназначено для сравнения последнего запрошенного и текущего включенного или отключенного состояния.</span><span class="sxs-lookup"><span data-stu-id="ae503-280">This property is provided to compare the last requested and current enabled or disabled states.</span></span> <span data-ttu-id="ae503-281">Конкретный экземпляр [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)) может не поддерживать **RequestStateChange**.</span><span class="sxs-lookup"><span data-stu-id="ae503-281">A particular instance of [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) might not support **RequestStateChange**.</span></span> <span data-ttu-id="ae503-282">В этом случае используется значение 12.</span><span class="sxs-lookup"><span data-stu-id="ae503-282">If this occurs, the value 12 is used.</span></span> <span data-ttu-id="ae503-283">Это свойство наследуется от **CIM \_ енабледлогикалелемент**.</span><span class="sxs-lookup"><span data-stu-id="ae503-283">This property is inherited from **CIM\_EnabledLogicalElement**.</span></span>



| <span data-ttu-id="ae503-284">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-284">Value</span></span>                                                                         | <span data-ttu-id="ae503-285">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-285">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae503-286"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-286"><dt>12</dt></span></span> </dl> | <span data-ttu-id="ae503-287">Не применимо</span><span class="sxs-lookup"><span data-stu-id="ae503-287">Not Applicable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ae503-288">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="ae503-288">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-289">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ae503-289">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-290">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-290">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-291">Текущее состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="ae503-291">The current status of the object.</span></span> <span data-ttu-id="ae503-292">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="ae503-292">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="ae503-293">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="ae503-293">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-294">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="ae503-294">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ae503-295">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-295">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-296">Строки, описывающие различные значения массива **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="ae503-296">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="ae503-297">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="ae503-297">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="ae503-298">**тимеофластстатечанже**</span><span class="sxs-lookup"><span data-stu-id="ae503-298">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-299">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="ae503-299">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-300">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-300">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-301">Дата или время последнего изменения включенного состояния элемента.</span><span class="sxs-lookup"><span data-stu-id="ae503-301">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="ae503-302">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85))и всегда имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="ae503-302">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="ae503-303">**транситионингтостате**</span><span class="sxs-lookup"><span data-stu-id="ae503-303">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ae503-304">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ae503-304">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="ae503-305">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ae503-305">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ae503-306">Указывает целевое состояние, в которое переходит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ae503-306">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="ae503-307">Это свойство наследуется от [**CIM \_ енабледлогикалелемент**](/previous-versions//cc136818(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ae503-307">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)).</span></span>



| <span data-ttu-id="ae503-308">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-308">Value</span></span>                                                                         | <span data-ttu-id="ae503-309">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-309">Meaning</span></span>                   |
|-------------------------------------------------------------------------------|---------------------------|
| <dl> <span data-ttu-id="ae503-310"><dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-310"><dt>12</dt></span></span> </dl> | <span data-ttu-id="ae503-311">Не применимо</span><span class="sxs-lookup"><span data-stu-id="ae503-311">Not Applicable</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ae503-312">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ae503-312">Remarks</span></span>

<span data-ttu-id="ae503-313">Доступ к классу **\_ терминалконнектион мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="ae503-313">Access to the **Msvm\_TerminalConnection** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ae503-314">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ae503-314">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ae503-315">Требования</span><span class="sxs-lookup"><span data-stu-id="ae503-315">Requirements</span></span>



| <span data-ttu-id="ae503-316">Требование</span><span class="sxs-lookup"><span data-stu-id="ae503-316">Requirement</span></span> | <span data-ttu-id="ae503-317">Значение</span><span class="sxs-lookup"><span data-stu-id="ae503-317">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae503-318">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae503-318">Minimum supported client</span></span><br/> | <span data-ttu-id="ae503-319">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ae503-319">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ae503-320">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae503-320">Minimum supported server</span></span><br/> | <span data-ttu-id="ae503-321">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ae503-321">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ae503-322">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ae503-322">Namespace</span></span><br/>                | <span data-ttu-id="ae503-323">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="ae503-323">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ae503-324">MOF</span><span class="sxs-lookup"><span data-stu-id="ae503-324">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ae503-325"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-325"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ae503-326">DLL</span><span class="sxs-lookup"><span data-stu-id="ae503-326">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae503-327"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ae503-327"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ae503-328">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ae503-328">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae503-329">**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="ae503-329">**CIM\_EnabledLogicalElement**</span></span>](cim-enabledlogicalelement.md)
</dt> <dt>

<span data-ttu-id="ae503-330">[**\_ЕНАБЛЕДЛОГИКАЛЕЛЕМЕНТ CIM**](/previous-versions//cc136818(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ae503-330">[**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="ae503-331">Классы видео</span><span class="sxs-lookup"><span data-stu-id="ae503-331">Video Classes</span></span>](video-classes.md)
</dt> </dl>

 

