---
description: Представляет данные параметра виртуальной локальной сети (VLAN).
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Класс Msvm_EthernetSwitchPortVlanSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664761"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="74b7d-103">\_Класс мсвм есернетсвитчпортвлансеттингдата</span><span class="sxs-lookup"><span data-stu-id="74b7d-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="74b7d-104">Представляет данные параметра виртуальной локальной сети (VLAN).</span><span class="sxs-lookup"><span data-stu-id="74b7d-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="74b7d-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="74b7d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74b7d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74b7d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="74b7d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="74b7d-107">Members</span></span>

<span data-ttu-id="74b7d-108">Класс **мсвм \_ есернетсвитчпортвлансеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74b7d-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="74b7d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="74b7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74b7d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="74b7d-110">Properties</span></span>

<span data-ttu-id="74b7d-111">Класс **мсвм \_ есернетсвитчпортвлансеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74b7d-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74b7d-112">**акцессвланид**</span><span class="sxs-lookup"><span data-stu-id="74b7d-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-113">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74b7d-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-115">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-116">Указывает идентификатор виртуальной ЛС в режиме доступа.</span><span class="sxs-lookup"><span data-stu-id="74b7d-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="74b7d-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-118">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74b7d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74b7d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-120">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="74b7d-120">A short description of the object.</span></span> <span data-ttu-id="74b7d-121">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры VLAN порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="74b7d-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-122">**Описание**</span><span class="sxs-lookup"><span data-stu-id="74b7d-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-123">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74b7d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-124">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74b7d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-125">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="74b7d-125">A description of the object.</span></span> <span data-ttu-id="74b7d-126">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные настройки виртуальной ЛС".</span><span class="sxs-lookup"><span data-stu-id="74b7d-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="74b7d-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74b7d-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74b7d-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-130">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="74b7d-130">A display name for the object.</span></span> <span data-ttu-id="74b7d-131">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры VLAN порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="74b7d-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="74b7d-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74b7d-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74b7d-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-135">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="74b7d-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-136">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="74b7d-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="74b7d-137">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="74b7d-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-138">**нативевланид**</span><span class="sxs-lookup"><span data-stu-id="74b7d-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-139">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74b7d-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-140">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-141">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-142">Указывает идентификатор виртуальной ЛС в режиме магистрали.</span><span class="sxs-lookup"><span data-stu-id="74b7d-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="74b7d-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-144">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74b7d-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-145">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-146">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-147">Указывает режим работы виртуальной ЛС.</span><span class="sxs-lookup"><span data-stu-id="74b7d-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="74b7d-148">**Доступ** (1)</span><span class="sxs-lookup"><span data-stu-id="74b7d-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="74b7d-149">**Магистраль** (2)</span><span class="sxs-lookup"><span data-stu-id="74b7d-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="74b7d-150">**Частный** (3)</span><span class="sxs-lookup"><span data-stu-id="74b7d-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74b7d-151">**примаривланид**</span><span class="sxs-lookup"><span data-stu-id="74b7d-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-152">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74b7d-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-153">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-154">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-155">Указывает основной идентификатор виртуальной ЛС в частном режиме.</span><span class="sxs-lookup"><span data-stu-id="74b7d-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-156">**пруневланидаррай**</span><span class="sxs-lookup"><span data-stu-id="74b7d-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-157">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="74b7d-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-158">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-159">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-160">Указывает битовую карту очистки идентификатора виртуальной ЛС в режиме магистрали.</span><span class="sxs-lookup"><span data-stu-id="74b7d-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-161">**пвланмоде**</span><span class="sxs-lookup"><span data-stu-id="74b7d-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-162">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="74b7d-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-163">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-164">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-165">Указывает частный режим виртуальной ЛС.</span><span class="sxs-lookup"><span data-stu-id="74b7d-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="74b7d-166">**Изолированный** (1)</span><span class="sxs-lookup"><span data-stu-id="74b7d-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="74b7d-167">**Сообщество** (2)</span><span class="sxs-lookup"><span data-stu-id="74b7d-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="74b7d-168">**Неизбирательные** (3)</span><span class="sxs-lookup"><span data-stu-id="74b7d-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="74b7d-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="74b7d-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-170">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="74b7d-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-171">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-172">Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-173">Указывает дополнительный идентификатор виртуальной ЛС в частном режиме.</span><span class="sxs-lookup"><span data-stu-id="74b7d-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-174">**секондаривланидаррай**</span><span class="sxs-lookup"><span data-stu-id="74b7d-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-175">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="74b7d-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-176">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-177">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-178">Указывает битовую карту дополнительного идентификатора виртуальной ЛС в частном режиме.</span><span class="sxs-lookup"><span data-stu-id="74b7d-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="74b7d-179">**трунквланидаррай**</span><span class="sxs-lookup"><span data-stu-id="74b7d-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74b7d-180">Тип данных: **UInt16** , массив</span><span class="sxs-lookup"><span data-stu-id="74b7d-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-181">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="74b7d-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="74b7d-182">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="74b7d-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="74b7d-183">Указывает точечный рисунок идентификатора виртуальной ЛС для магистрали в режиме магистрали.</span><span class="sxs-lookup"><span data-stu-id="74b7d-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74b7d-184">Требования</span><span class="sxs-lookup"><span data-stu-id="74b7d-184">Requirements</span></span>



| <span data-ttu-id="74b7d-185">Требование</span><span class="sxs-lookup"><span data-stu-id="74b7d-185">Requirement</span></span> | <span data-ttu-id="74b7d-186">Значение</span><span class="sxs-lookup"><span data-stu-id="74b7d-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74b7d-187">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74b7d-187">Minimum supported client</span></span><br/> | <span data-ttu-id="74b7d-188">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="74b7d-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="74b7d-189">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74b7d-189">Minimum supported server</span></span><br/> | <span data-ttu-id="74b7d-190">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="74b7d-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74b7d-191">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74b7d-191">Namespace</span></span><br/>                | <span data-ttu-id="74b7d-192">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="74b7d-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="74b7d-193">MOF</span><span class="sxs-lookup"><span data-stu-id="74b7d-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74b7d-194"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74b7d-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="74b7d-195">DLL</span><span class="sxs-lookup"><span data-stu-id="74b7d-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74b7d-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74b7d-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

