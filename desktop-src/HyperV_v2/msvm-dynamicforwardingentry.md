---
description: Представляет запись в базе данных перенаправления (фильтрации), связанную со службой прозрачного моста.
ms.assetid: 3C9FAE99-9543-4A6A-B578-3F4626598DB3
title: Класс Msvm_DynamicForwardingEntry
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DynamicForwardingEntry
- Msvm_DynamicForwardingEntry.InstanceID
- Msvm_DynamicForwardingEntry.Caption
- Msvm_DynamicForwardingEntry.Description
- Msvm_DynamicForwardingEntry.ElementName
- Msvm_DynamicForwardingEntry.InstallDate
- Msvm_DynamicForwardingEntry.Name
- Msvm_DynamicForwardingEntry.OperationalStatus
- Msvm_DynamicForwardingEntry.StatusDescriptions
- Msvm_DynamicForwardingEntry.Status
- Msvm_DynamicForwardingEntry.HealthState
- Msvm_DynamicForwardingEntry.CommunicationStatus
- Msvm_DynamicForwardingEntry.DetailedStatus
- Msvm_DynamicForwardingEntry.OperatingStatus
- Msvm_DynamicForwardingEntry.PrimaryStatus
- Msvm_DynamicForwardingEntry.SystemCreationClassName
- Msvm_DynamicForwardingEntry.SystemName
- Msvm_DynamicForwardingEntry.ServiceCreationClassName
- Msvm_DynamicForwardingEntry.ServiceName
- Msvm_DynamicForwardingEntry.CreationClassName
- Msvm_DynamicForwardingEntry.MACAddress
- Msvm_DynamicForwardingEntry.DynamicStatus
- Msvm_DynamicForwardingEntry.VlanId
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f14f8b3a8f5f62e1a474b3d7b7f832b6acd530f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683858"
---
# <a name="msvm_dynamicforwardingentry-class"></a><span data-ttu-id="5d15d-103">\_Класс мсвм динамикфорвардинжентри</span><span class="sxs-lookup"><span data-stu-id="5d15d-103">Msvm\_DynamicForwardingEntry class</span></span>

<span data-ttu-id="5d15d-104">Представляет запись в базе данных перенаправления (фильтрации), связанную со службой прозрачного моста.</span><span class="sxs-lookup"><span data-stu-id="5d15d-104">Represents an entry in the forwarding (filtering) database that is associated with the transparent bridging service.</span></span> <span data-ttu-id="5d15d-105">Запись является слабой для службы, как указано в [**мсвм \_ транспарентбридгингдинамикфорвардинг**](msvm-transparentbridgingdynamicforwarding.md).</span><span class="sxs-lookup"><span data-stu-id="5d15d-105">The entry is weak to the service, as specified by [**Msvm\_TransparentBridgingDynamicForwarding**](msvm-transparentbridgingdynamicforwarding.md).</span></span>

<span data-ttu-id="5d15d-106">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5d15d-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d15d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d15d-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DynamicForwardingEntry : CIM_DynamicForwardingEntry
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   SystemCreationClassName;
  string   SystemName;
  string   ServiceCreationClassName;
  string   ServiceName;
  string   CreationClassName;
  string   MACAddress;
  uint16   DynamicStatus;
  uint16   VlanId;
};
```

## <a name="members"></a><span data-ttu-id="5d15d-108">Члены</span><span class="sxs-lookup"><span data-stu-id="5d15d-108">Members</span></span>

<span data-ttu-id="5d15d-109">Класс **мсвм \_ динамикфорвардинжентри** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5d15d-109">The **Msvm\_DynamicForwardingEntry** class has these types of members:</span></span>

-   [<span data-ttu-id="5d15d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d15d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5d15d-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="5d15d-111">Properties</span></span>

<span data-ttu-id="5d15d-112">Класс **мсвм \_ динамикфорвардинжентри** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5d15d-112">The **Msvm\_DynamicForwardingEntry** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5d15d-113">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5d15d-113">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-116">Квалификаторы: **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5d15d-116">Qualifiers: **MaxLen** (64)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-117">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5d15d-117">A short description of the object.</span></span> <span data-ttu-id="5d15d-118">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-118">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-119">**коммуникатионстатус**</span><span class="sxs-lookup"><span data-stu-id="5d15d-119">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-120">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-122">Указывает способность инструментирования взаимодействовать с базовым управляемым элементом.</span><span class="sxs-lookup"><span data-stu-id="5d15d-122">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="5d15d-123">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5d15d-123">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5d15d-124">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-124">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-125">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5d15d-125">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-126">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-127">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-128">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5d15d-128">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-129">Имя класса или подкласса, используемого при создании экземпляра.</span><span class="sxs-lookup"><span data-stu-id="5d15d-129">The name of the class or the subclass used in the creation of an instance.</span></span> <span data-ttu-id="5d15d-130">При использовании с другими ключевыми свойствами этого класса это свойство позволяет однозначно идентифицировать все экземпляры этого класса и его подклассов.</span><span class="sxs-lookup"><span data-stu-id="5d15d-130">When used with the other key properties of this class, this property allows all instances of this class and its subclasses to be uniquely identified.</span></span> <span data-ttu-id="5d15d-131">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-131">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-132">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5d15d-132">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-135">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5d15d-135">A description of the object.</span></span> <span data-ttu-id="5d15d-136">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-136">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-137">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="5d15d-137">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-138">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-138">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-140">Дополняет свойство **примаристатус** дополнительными сведениями о состоянии.</span><span class="sxs-lookup"><span data-stu-id="5d15d-140">Complements the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="5d15d-141">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5d15d-141">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5d15d-142">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-142">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-143">**динамикстатус**</span><span class="sxs-lookup"><span data-stu-id="5d15d-143">**DynamicStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-144">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-146">Состояние записи.</span><span class="sxs-lookup"><span data-stu-id="5d15d-146">The status of the entry.</span></span> <span data-ttu-id="5d15d-147">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-147">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="5d15d-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="5d15d-148"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Недопустимое** (2)</span><span class="sxs-lookup"><span data-stu-id="5d15d-149"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (2)</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Узнали** (3)</span><span class="sxs-lookup"><span data-stu-id="5d15d-150"><span id="Learned"></span><span id="learned"></span><span id="LEARNED"></span>**Learned** (3)</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span><span class="sxs-lookup"><span data-stu-id="5d15d-151"><span id="Self"></span><span id="self"></span><span id="SELF"></span>**Self** (4)</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>Управление **(5** )</span><span class="sxs-lookup"><span data-stu-id="5d15d-152"><span id="Mgmt"></span><span id="mgmt"></span><span id="MGMT"></span>**Mgmt** (5)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5d15d-153">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5d15d-153">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-154">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-155">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-155">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-156">Отображаемое имя элемента.</span><span class="sxs-lookup"><span data-stu-id="5d15d-156">A display name for the element.</span></span> <span data-ttu-id="5d15d-157">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-158">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="5d15d-158">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-159">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-160">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-161">Текущая работоспособность элемента.</span><span class="sxs-lookup"><span data-stu-id="5d15d-161">The current health of the element.</span></span> <span data-ttu-id="5d15d-162">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)и всегда имеет значение 5 ("ОК").</span><span class="sxs-lookup"><span data-stu-id="5d15d-162">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), and it is always set to 5 ("OK").</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-163">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="5d15d-163">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-164">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5d15d-164">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-166">Заполняется автоматически при создании виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="5d15d-166">Automatically populated when the virtual machine is created.</span></span> <span data-ttu-id="5d15d-167">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-167">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-168">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5d15d-168">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-171">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5d15d-171">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-172">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="5d15d-172">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5d15d-173">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-173">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-174">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="5d15d-174">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-177">Квалификаторы: **Key**, **maxlen** (12)</span><span class="sxs-lookup"><span data-stu-id="5d15d-177">Qualifiers: **Key**, **MaxLen** (12)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-178">MAC-адрес одноадресной рассылки, для которого служба прозрачного моста содержит сведения о пересылке и фильтрации.</span><span class="sxs-lookup"><span data-stu-id="5d15d-178">Unicast MAC address for which the transparent bridging service has forwarding and filtering information.</span></span> <span data-ttu-id="5d15d-179">MAC-адрес имеет формат двенадцати шестнадцатеричных цифр (например, "010203040506"), при этом каждая пара представляет один из шести октетов MAC-адреса в "каноническом" битовом порядке согласно RFC 2469.</span><span class="sxs-lookup"><span data-stu-id="5d15d-179">The MAC address is formatted as twelve hexadecimal digits (for example, "010203040506"), with each pair representing one of the six octets of the MAC address in "canonical" bit order according to RFC 2469.</span></span> <span data-ttu-id="5d15d-180">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-180">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-181">**Name**</span><span class="sxs-lookup"><span data-stu-id="5d15d-181">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-182">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-183">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-184">Метка, по которой известен объект.</span><span class="sxs-lookup"><span data-stu-id="5d15d-184">The label by which the object is known.</span></span> <span data-ttu-id="5d15d-185">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-185">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-186">**оператингстатус**</span><span class="sxs-lookup"><span data-stu-id="5d15d-186">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-187">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-187">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-188">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-188">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-189">Предоставляет сведения о текущем состоянии для рабочего условия элемента и может использоваться для предоставления более подробных сведений относительно значения свойства **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="5d15d-189">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="5d15d-190">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5d15d-190">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5d15d-191">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-191">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-192">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="5d15d-192">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-193">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="5d15d-193">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-194">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-195">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5d15d-195">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-196">**примаристатус**</span><span class="sxs-lookup"><span data-stu-id="5d15d-196">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-197">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-197">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-198">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-198">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-199">Предоставляет сведения о состоянии высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="5d15d-199">Provides high level status information.</span></span> <span data-ttu-id="5d15d-200">Это свойство следует использовать вместе со свойством **детаиледстатус** для предоставления высокого уровня и подробных сведений о состоянии работоспособности элемента и его подкомпонентов.</span><span class="sxs-lookup"><span data-stu-id="5d15d-200">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status information for the element and its subcomponents.</span></span> <span data-ttu-id="5d15d-201">Значение **null** указывает, что это свойство не реализовано.</span><span class="sxs-lookup"><span data-stu-id="5d15d-201">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="5d15d-202">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="5d15d-202">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-203">**сервицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="5d15d-203">**ServiceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-204">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-204">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-205">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-205">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-206">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5d15d-206">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-207">**Свойство CreationClassName** службы области.</span><span class="sxs-lookup"><span data-stu-id="5d15d-207">The scoping service's **CreationClassName**.</span></span> <span data-ttu-id="5d15d-208">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-208">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-209">**Служба**</span><span class="sxs-lookup"><span data-stu-id="5d15d-209">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-211">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-212">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5d15d-212">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-213">Имя службы области.</span><span class="sxs-lookup"><span data-stu-id="5d15d-213">The scoping service's name.</span></span> <span data-ttu-id="5d15d-214">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-214">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-215">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="5d15d-215">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-216">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-217">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-217">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-218">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не используется.</span><span class="sxs-lookup"><span data-stu-id="5d15d-218">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-219">**статусдескриптионс**</span><span class="sxs-lookup"><span data-stu-id="5d15d-219">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-220">Тип данных: массив **строк**</span><span class="sxs-lookup"><span data-stu-id="5d15d-220">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-221">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-221">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-222">Это свойство наследуется от [**CIM \_ манажедсистемелемент**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), но не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5d15d-222">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-223">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="5d15d-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-224">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-225">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-226">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5d15d-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-227">**Свойство CreationClassName** системы области.</span><span class="sxs-lookup"><span data-stu-id="5d15d-227">The scoping system's **CreationClassName**.</span></span> <span data-ttu-id="5d15d-228">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-228">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5d15d-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-230">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5d15d-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-231">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5d15d-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-232">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5d15d-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-233">Имя системы области.</span><span class="sxs-lookup"><span data-stu-id="5d15d-233">The scoping system's name.</span></span> <span data-ttu-id="5d15d-234">Это свойство наследуется от [**CIM \_ динамикфорвардинжентри**](/previous-versions//cc136814(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5d15d-234">This property is inherited from [**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="5d15d-235">**VlanId**</span><span class="sxs-lookup"><span data-stu-id="5d15d-235">**VlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5d15d-236">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5d15d-236">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5d15d-237">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5d15d-237">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5d15d-238">Идентификатор виртуальной локальной сети, связанный с этой записью.</span><span class="sxs-lookup"><span data-stu-id="5d15d-238">The virtual LAN identifier associated with this entry.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d15d-239">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d15d-239">Remarks</span></span>

<span data-ttu-id="5d15d-240">Доступ к классу **\_ динамикфорвардинжентри мсвм** может быть ограничен фильтром контроля учетных записей.</span><span class="sxs-lookup"><span data-stu-id="5d15d-240">Access to the **Msvm\_DynamicForwardingEntry** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="5d15d-241">Дополнительные сведения см. в разделе [Управление учетными записями пользователей и инструментарий WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="5d15d-241">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="5d15d-242">Примеры</span><span class="sxs-lookup"><span data-stu-id="5d15d-242">Examples</span></span>

<span data-ttu-id="5d15d-243">См. раздел [запросы к сетевым объектам](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="5d15d-243">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d15d-244">Требования</span><span class="sxs-lookup"><span data-stu-id="5d15d-244">Requirements</span></span>



| <span data-ttu-id="5d15d-245">Требование</span><span class="sxs-lookup"><span data-stu-id="5d15d-245">Requirement</span></span> | <span data-ttu-id="5d15d-246">Значение</span><span class="sxs-lookup"><span data-stu-id="5d15d-246">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d15d-247">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d15d-247">Minimum supported client</span></span><br/> | <span data-ttu-id="5d15d-248">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5d15d-248">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5d15d-249">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d15d-249">Minimum supported server</span></span><br/> | <span data-ttu-id="5d15d-250">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5d15d-250">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5d15d-251">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5d15d-251">Namespace</span></span><br/>                | <span data-ttu-id="5d15d-252">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5d15d-252">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5d15d-253">MOF</span><span class="sxs-lookup"><span data-stu-id="5d15d-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d15d-254"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d15d-254"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d15d-255">DLL</span><span class="sxs-lookup"><span data-stu-id="5d15d-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d15d-256"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5d15d-256"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5d15d-257">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d15d-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d15d-258">**\_ДИНАМИКФОРВАРДИНЖЕНТРИ CIM**</span><span class="sxs-lookup"><span data-stu-id="5d15d-258">**CIM\_DynamicForwardingEntry**</span></span>](cim-dynamicforwardingentry.md)
</dt> <dt>

<span data-ttu-id="5d15d-259">[**\_ДИНАМИКФОРВАРДИНЖЕНТРИ CIM**](/previous-versions//cc136814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d15d-259">[**CIM\_DynamicForwardingEntry**](/previous-versions//cc136814(v=vs.85))</span></span>
</dt> </dl>

 

