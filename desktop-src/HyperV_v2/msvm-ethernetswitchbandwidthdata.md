---
description: Представляет состояние ресурса пропускной способности коммутатора.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Класс Msvm_EthernetSwitchBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682648"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="af42c-103">\_Класс мсвм есернетсвитчбандвидсдата</span><span class="sxs-lookup"><span data-stu-id="af42c-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="af42c-104">Представляет состояние ресурса пропускной способности коммутатора.</span><span class="sxs-lookup"><span data-stu-id="af42c-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="af42c-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="af42c-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="af42c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af42c-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="af42c-107">Члены</span><span class="sxs-lookup"><span data-stu-id="af42c-107">Members</span></span>

<span data-ttu-id="af42c-108">Класс **мсвм \_ есернетсвитчбандвидсдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="af42c-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="af42c-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="af42c-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="af42c-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="af42c-110">Properties</span></span>

<span data-ttu-id="af42c-111">Класс **мсвм \_ есернетсвитчбандвидсдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="af42c-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="af42c-112">**Производительность**</span><span class="sxs-lookup"><span data-stu-id="af42c-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-113">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af42c-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-115">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="af42c-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-116">Максимальная пропускная способность, доступная на коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="af42c-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="af42c-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af42c-120">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="af42c-120">A short description of the object.</span></span> <span data-ttu-id="af42c-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="af42c-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af42c-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="af42c-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-125">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="af42c-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-126">Имя класса или подкласса, используемого при создании этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="af42c-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-127">**дефаултфловресерватион**</span><span class="sxs-lookup"><span data-stu-id="af42c-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-128">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af42c-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-130">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="af42c-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-131">Текущая абсолютная пропускная способность, зарезервированная для параметра потока по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af42c-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-132">**дефаултфловресерватионперцентаже**</span><span class="sxs-lookup"><span data-stu-id="af42c-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-133">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="af42c-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-135">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="af42c-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-136">Текущий процент пропускной способности, зарезервированный для параметра потока по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="af42c-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-137">**дефаултфловвеигхт**</span><span class="sxs-lookup"><span data-stu-id="af42c-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-138">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af42c-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-140">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="af42c-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-141">Текущий вес для потока по умолчанию на коммутаторе.</span><span class="sxs-lookup"><span data-stu-id="af42c-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-142">**Описание**</span><span class="sxs-lookup"><span data-stu-id="af42c-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af42c-145">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="af42c-145">A description of the object.</span></span> <span data-ttu-id="af42c-146">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="af42c-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af42c-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="af42c-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-148">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="af42c-150">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="af42c-150">A display name for the object.</span></span> <span data-ttu-id="af42c-151">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="af42c-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af42c-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="af42c-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-155">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="af42c-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="af42c-156">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="af42c-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="af42c-157">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="af42c-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="af42c-158">**Name**</span><span class="sxs-lookup"><span data-stu-id="af42c-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-159">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-160">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-161">Квалификаторы: **ключ**, **Переопределение**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="af42c-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-162">Уникальное имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="af42c-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-163">**Резервирование**</span><span class="sxs-lookup"><span data-stu-id="af42c-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-164">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="af42c-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-165">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-166">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="af42c-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-167">Текущая пропускная способность, зарезервированная для коммутатора.</span><span class="sxs-lookup"><span data-stu-id="af42c-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="af42c-168">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="af42c-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-171">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="af42c-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-172">Имя класса создания системы размещения.</span><span class="sxs-lookup"><span data-stu-id="af42c-172">The hosting system's creation class name.</span></span> <span data-ttu-id="af42c-173">Это свойство наследуется [**от \_ службы CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="af42c-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="af42c-174">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="af42c-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="af42c-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="af42c-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="af42c-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="af42c-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="af42c-177">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="af42c-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="af42c-178">Имя виртуального коммутатора, к которому привязан связанный экземпляр ресурса.</span><span class="sxs-lookup"><span data-stu-id="af42c-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="af42c-179">Требования</span><span class="sxs-lookup"><span data-stu-id="af42c-179">Requirements</span></span>



| <span data-ttu-id="af42c-180">Требование</span><span class="sxs-lookup"><span data-stu-id="af42c-180">Requirement</span></span> | <span data-ttu-id="af42c-181">Значение</span><span class="sxs-lookup"><span data-stu-id="af42c-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af42c-182">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="af42c-182">Minimum supported client</span></span><br/> | <span data-ttu-id="af42c-183">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="af42c-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="af42c-184">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="af42c-184">Minimum supported server</span></span><br/> | <span data-ttu-id="af42c-185">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="af42c-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="af42c-186">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="af42c-186">Namespace</span></span><br/>                | <span data-ttu-id="af42c-187">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="af42c-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="af42c-188">MOF</span><span class="sxs-lookup"><span data-stu-id="af42c-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="af42c-189"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="af42c-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="af42c-190">DLL</span><span class="sxs-lookup"><span data-stu-id="af42c-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="af42c-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="af42c-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

