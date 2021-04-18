---
description: Представляет список управления доступом (ACL) для параметров порта коммутатора.
ms.assetid: c0d6dfa1-017c-4e66-9ee3-425182d84231
title: Класс Msvm_EthernetSwitchPortAclSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortAclSettingData
- Msvm_EthernetSwitchPortAclSettingData.InstanceID
- Msvm_EthernetSwitchPortAclSettingData.Caption
- Msvm_EthernetSwitchPortAclSettingData.Description
- Msvm_EthernetSwitchPortAclSettingData.ElementName
- Msvm_EthernetSwitchPortAclSettingData.Name
- Msvm_EthernetSwitchPortAclSettingData.Direction
- Msvm_EthernetSwitchPortAclSettingData.Applicability
- Msvm_EthernetSwitchPortAclSettingData.AclType
- Msvm_EthernetSwitchPortAclSettingData.Action
- Msvm_EthernetSwitchPortAclSettingData.LocalAddress
- Msvm_EthernetSwitchPortAclSettingData.LocalAddressPrefixLength
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddress
- Msvm_EthernetSwitchPortAclSettingData.RemoteAddressPrefixLength
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 92735718e339a0caf33910dec703276aea946a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684698"
---
# <a name="msvm_ethernetswitchportaclsettingdata-class"></a><span data-ttu-id="75b39-103">\_Класс мсвм есернетсвитчпортаклсеттингдата</span><span class="sxs-lookup"><span data-stu-id="75b39-103">Msvm\_EthernetSwitchPortAclSettingData class</span></span>

<span data-ttu-id="75b39-104">Представляет список управления доступом (ACL) для параметров порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="75b39-104">Represents the access control list (ACL) for switch port settings.</span></span>

<span data-ttu-id="75b39-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="75b39-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="75b39-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="75b39-106">Syntax</span></span>

``` syntax
[Dynamic, UUID("998BEF4A-5D55-492A-9C43-8B2F5EAE9F2B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), Provider("VmmsWmiInstanceAndMethodProvider"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port ACL Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortAclSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port ACL Settings";
  string Description = "Represents the base class for switch port settings.";
  string ElementName = "Ethernet Switch Port ACL Settings";
  string Name = "";
  uint8  Direction = 0;
  uint8  Applicability = 0;
  uint8  AclType = 0;
  uint8  Action = 0;
  string LocalAddress = "";
  uint8  LocalAddressPrefixLength = 0;
  string RemoteAddress = length = 0;
  uint8  RemoteAddressPrefixLength = 0;
};
```

## <a name="members"></a><span data-ttu-id="75b39-107">Члены</span><span class="sxs-lookup"><span data-stu-id="75b39-107">Members</span></span>

<span data-ttu-id="75b39-108">Класс **мсвм \_ есернетсвитчпортаклсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="75b39-108">The **Msvm\_EthernetSwitchPortAclSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="75b39-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="75b39-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="75b39-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="75b39-110">Properties</span></span>

<span data-ttu-id="75b39-111">Класс **мсвм \_ есернетсвитчпортаклсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="75b39-111">The **Msvm\_EthernetSwitchPortAclSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="75b39-112">**аклтипе**</span><span class="sxs-lookup"><span data-stu-id="75b39-112">**AclType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-113">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="75b39-113">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-115">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-115">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-116">Указывает тип конечной точки ACL.</span><span class="sxs-lookup"><span data-stu-id="75b39-116">This indicates the type of ACL endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="75b39-117">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC_Acl"></span><span id="mac_acl"></span><span id="MAC_ACL"></span>

<span data-ttu-id="75b39-118">**Список ACL Mac** (1)</span><span class="sxs-lookup"><span data-stu-id="75b39-118">**MAC Acl** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_Acl"></span><span id="ipv4_acl"></span><span id="IPV4_ACL"></span>

<span data-ttu-id="75b39-119">**Список ACL IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="75b39-119">**IPv4 Acl** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6_Acl"></span><span id="ipv6_acl"></span><span id="IPV6_ACL"></span>

<span data-ttu-id="75b39-120">**Список ACL IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="75b39-120">**IPv6 Acl** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="75b39-121">**Действие**</span><span class="sxs-lookup"><span data-stu-id="75b39-121">**Action**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-122">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="75b39-122">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-123">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-123">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-124">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-124">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-125">Это указывает на действие списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="75b39-125">This indicates the action of the ACL.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="75b39-126">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-126">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span data-ttu-id="75b39-127">**Разрешить** (1)</span><span class="sxs-lookup"><span data-stu-id="75b39-127">**Allow** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Deny"></span><span id="deny"></span><span id="DENY"></span>

<span data-ttu-id="75b39-128">**Deny** (2)</span><span class="sxs-lookup"><span data-stu-id="75b39-128">**Deny** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Meter"></span><span id="meter"></span><span id="METER"></span>

<span data-ttu-id="75b39-129">**Счетчик** (3)</span><span class="sxs-lookup"><span data-stu-id="75b39-129">**Meter** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="75b39-130">**Квартал**</span><span class="sxs-lookup"><span data-stu-id="75b39-130">**Applicability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-131">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="75b39-131">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-132">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-133">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-133">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-134">Указывает, применяется ли ACL к локальной или удаленной конечной точке.</span><span class="sxs-lookup"><span data-stu-id="75b39-134">This indicates whether the ACL applies to the local or remote endpoint.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="75b39-135">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Local"></span><span id="local"></span><span id="LOCAL"></span>

<span data-ttu-id="75b39-136">**Локальный** (1)</span><span class="sxs-lookup"><span data-stu-id="75b39-136">**Local** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote"></span><span id="remote"></span><span id="REMOTE"></span>

<span data-ttu-id="75b39-137">**Удаленный** (2)</span><span class="sxs-lookup"><span data-stu-id="75b39-137">**Remote** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="75b39-138">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="75b39-138">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-139">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75b39-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75b39-141">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="75b39-141">A short description of the object.</span></span> <span data-ttu-id="75b39-142">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "параметры ACL порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="75b39-142">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="75b39-143">**Описание**</span><span class="sxs-lookup"><span data-stu-id="75b39-143">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75b39-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75b39-146">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="75b39-146">A description of the object.</span></span> <span data-ttu-id="75b39-147">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет базовый класс для параметров порта коммутатора".</span><span class="sxs-lookup"><span data-stu-id="75b39-147">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the base class for switch port settings.".</span></span>

</dd> <dt>

<span data-ttu-id="75b39-148">**Направление**</span><span class="sxs-lookup"><span data-stu-id="75b39-148">**Direction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-149">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="75b39-149">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-150">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-151">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-151">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-152">Указывает, применяется ли ACL к входящим или исходящим направлениям.</span><span class="sxs-lookup"><span data-stu-id="75b39-152">This indicates whether the ACL applies to ingress or egress direction.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="75b39-153">**Неизвестно** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-153">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Incoming"></span><span id="incoming"></span><span id="INCOMING"></span>

<span data-ttu-id="75b39-154">**Входящий** трафик (1)</span><span class="sxs-lookup"><span data-stu-id="75b39-154">**Incoming** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Outgoing"></span><span id="outgoing"></span><span id="OUTGOING"></span>

<span data-ttu-id="75b39-155">**Исходящие** (2)</span><span class="sxs-lookup"><span data-stu-id="75b39-155">**Outgoing** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="75b39-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="75b39-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75b39-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="75b39-159">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="75b39-159">A display name for the object.</span></span> <span data-ttu-id="75b39-160">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "параметры ACL порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="75b39-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port ACL Settings".</span></span>

</dd> <dt>

<span data-ttu-id="75b39-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="75b39-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="75b39-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="75b39-164">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="75b39-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="75b39-165">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="75b39-165">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="75b39-166">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="75b39-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="75b39-167">**LocalAddress**</span><span class="sxs-lookup"><span data-stu-id="75b39-167">**LocalAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-169">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-169">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-170">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **вмидатаид** (6), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-170">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-171">Локальный адрес виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="75b39-171">The local address of the virtual machine.</span></span> <span data-ttu-id="75b39-172">Это может быть IPv4, IPv6 или MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="75b39-172">This can be an IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="75b39-173">**локаладдресспрефиксленгс**</span><span class="sxs-lookup"><span data-stu-id="75b39-173">**LocalAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-174">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="75b39-174">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-175">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-175">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-176">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-176">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-177">Длина префикса локального адреса.</span><span class="sxs-lookup"><span data-stu-id="75b39-177">The local address prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="75b39-178">**Name**</span><span class="sxs-lookup"><span data-stu-id="75b39-178">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-180">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-180">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-181">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **вмидатаид** (1), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-181">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-182">Отображаемое имя списка управления доступом.</span><span class="sxs-lookup"><span data-stu-id="75b39-182">The display name of the ACL.</span></span>

</dd> <dt>

<span data-ttu-id="75b39-183">**RemoteAddress**</span><span class="sxs-lookup"><span data-stu-id="75b39-183">**RemoteAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-184">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="75b39-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-185">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-185">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-186">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **вмидатаид** (8), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-186">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (40), **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-187">Удаленный адрес виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="75b39-187">The remote address of the virtual machine.</span></span> <span data-ttu-id="75b39-188">Это может быть IPv4, IPv6 или MAC-адрес.</span><span class="sxs-lookup"><span data-stu-id="75b39-188">This can be IPv4, IPv6, or a MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="75b39-189">**ремотеаддресспрефиксленгс**</span><span class="sxs-lookup"><span data-stu-id="75b39-189">**RemoteAddressPrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="75b39-190">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="75b39-190">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="75b39-191">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="75b39-191">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="75b39-192">Квалификаторы: **вмидатаид** (9), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="75b39-192">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="75b39-193">Длина префикса удаленного адреса.</span><span class="sxs-lookup"><span data-stu-id="75b39-193">The remote address prefix length.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="75b39-194">Требования</span><span class="sxs-lookup"><span data-stu-id="75b39-194">Requirements</span></span>



| <span data-ttu-id="75b39-195">Требование</span><span class="sxs-lookup"><span data-stu-id="75b39-195">Requirement</span></span> | <span data-ttu-id="75b39-196">Значение</span><span class="sxs-lookup"><span data-stu-id="75b39-196">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75b39-197">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75b39-197">Minimum supported client</span></span><br/> | <span data-ttu-id="75b39-198">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="75b39-198">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="75b39-199">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75b39-199">Minimum supported server</span></span><br/> | <span data-ttu-id="75b39-200">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="75b39-200">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="75b39-201">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="75b39-201">Namespace</span></span><br/>                | <span data-ttu-id="75b39-202">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="75b39-202">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="75b39-203">MOF</span><span class="sxs-lookup"><span data-stu-id="75b39-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75b39-204"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="75b39-204"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="75b39-205">DLL</span><span class="sxs-lookup"><span data-stu-id="75b39-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75b39-206"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="75b39-206"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

