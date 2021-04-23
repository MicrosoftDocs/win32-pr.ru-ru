---
description: Представляет данные о состоянии функции пропускной способности порта.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Класс Msvm_EthernetSwitchPortBandwidthData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662584"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="5fcdc-103">\_Класс мсвм есернетсвитчпортбандвидсдата</span><span class="sxs-lookup"><span data-stu-id="5fcdc-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="5fcdc-104">Представляет данные о состоянии функции пропускной способности порта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="5fcdc-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fcdc-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fcdc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="5fcdc-107">Члены</span><span class="sxs-lookup"><span data-stu-id="5fcdc-107">Members</span></span>

<span data-ttu-id="5fcdc-108">Класс **мсвм \_ есернетсвитчпортбандвидсдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="5fcdc-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="5fcdc-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fcdc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fcdc-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="5fcdc-110">Properties</span></span>

<span data-ttu-id="5fcdc-111">Класс **мсвм \_ есернетсвитчпортбандвидсдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fcdc-112">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-115">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-115">A short description of the object.</span></span> <span data-ttu-id="5fcdc-116">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "состояние функции пропускной способности порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="5fcdc-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-120">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-121">Имя подкласса, используемого при создании этого экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="5fcdc-122">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ есернетсвитчпортбандвидсдата".</span><span class="sxs-lookup"><span data-stu-id="5fcdc-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-123">**куррентбандвидсресерватионперцентаже**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-124">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-125">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="5fcdc-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-126">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-127">Текущий процент пропускной способности, зарезервированный для этого порта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-128">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-131">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-131">A description of the object.</span></span> <span data-ttu-id="5fcdc-132">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные состояния функции пропускной способности порта".</span><span class="sxs-lookup"><span data-stu-id="5fcdc-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-133">**девицекреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-136">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-137">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-137">The scoping system's creation class name.</span></span> <span data-ttu-id="5fcdc-138">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ есернетсвитчпорт".</span><span class="sxs-lookup"><span data-stu-id="5fcdc-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-139">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-142">Квалификаторы: **Key**, **maxlen** (64)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-143">ИДЕНТИФИКАТОР устройства, определяющего область данного экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="5fcdc-144">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="5fcdc-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-148">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-148">A display name for the object.</span></span> <span data-ttu-id="5fcdc-149">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "состояние функции пропускной способности порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="5fcdc-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-153">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-154">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="5fcdc-155">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="5fcdc-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-156">**Name**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-159">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-160">Строка, уникально идентифицирующая этот экземпляр данных порта в области действия коммутатора и порта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="5fcdc-161">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="5fcdc-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-162">**системкреатионкласснаме**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-165">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-166">Имя класса создания системы области.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-166">The scoping system's creation class name.</span></span> <span data-ttu-id="5fcdc-167">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md)и всегда имеет значение "мсвм \_ виртуалесернетсвитч".</span><span class="sxs-lookup"><span data-stu-id="5fcdc-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="5fcdc-168">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fcdc-169">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="5fcdc-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-170">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="5fcdc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fcdc-171">Квалификаторы: **Key**, **maxlen** (256)</span><span class="sxs-lookup"><span data-stu-id="5fcdc-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="5fcdc-172">Имя виртуального коммутатора, который ограничивает область данного экземпляра данных порта.</span><span class="sxs-lookup"><span data-stu-id="5fcdc-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="5fcdc-173">Это свойство наследуется от [**мсвм \_ есернетпортдата**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="5fcdc-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fcdc-174">Требования</span><span class="sxs-lookup"><span data-stu-id="5fcdc-174">Requirements</span></span>



| <span data-ttu-id="5fcdc-175">Требование</span><span class="sxs-lookup"><span data-stu-id="5fcdc-175">Requirement</span></span> | <span data-ttu-id="5fcdc-176">Значение</span><span class="sxs-lookup"><span data-stu-id="5fcdc-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fcdc-177">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5fcdc-177">Minimum supported client</span></span><br/> | <span data-ttu-id="5fcdc-178">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5fcdc-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="5fcdc-179">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5fcdc-179">Minimum supported server</span></span><br/> | <span data-ttu-id="5fcdc-180">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5fcdc-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5fcdc-181">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="5fcdc-181">Namespace</span></span><br/>                | <span data-ttu-id="5fcdc-182">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="5fcdc-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="5fcdc-183">MOF</span><span class="sxs-lookup"><span data-stu-id="5fcdc-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fcdc-184"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fcdc-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fcdc-185">DLL</span><span class="sxs-lookup"><span data-stu-id="5fcdc-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fcdc-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fcdc-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

