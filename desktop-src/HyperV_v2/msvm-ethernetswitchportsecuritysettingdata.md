---
description: Представляет данные настройки функции безопасности.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Класс Msvm_EthernetSwitchPortSecuritySettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d37913f015a3ffbfaa751a7bbb10f79cea2fb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913887"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a><span data-ttu-id="46172-103">\_Класс мсвм есернетсвитчпортсекуритисеттингдата</span><span class="sxs-lookup"><span data-stu-id="46172-103">Msvm\_EthernetSwitchPortSecuritySettingData class</span></span>

<span data-ttu-id="46172-104">Представляет данные настройки функции безопасности.</span><span class="sxs-lookup"><span data-stu-id="46172-104">Represents the security feature setting data.</span></span>

<span data-ttu-id="46172-105">Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="46172-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="46172-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="46172-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a><span data-ttu-id="46172-107">Члены</span><span class="sxs-lookup"><span data-stu-id="46172-107">Members</span></span>

<span data-ttu-id="46172-108">Класс **мсвм \_ есернетсвитчпортсекуритисеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="46172-108">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="46172-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="46172-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="46172-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="46172-110">Properties</span></span>

<span data-ttu-id="46172-111">Класс **мсвм \_ есернетсвитчпортсекуритисеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="46172-111">The **Msvm\_EthernetSwitchPortSecuritySettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="46172-112">**алловииеприорититаг**</span><span class="sxs-lookup"><span data-stu-id="46172-112">**AllowIeeePriorityTag**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-115">Квалификаторы: **вмидатаид** (6), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-115">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-116">Указывает, должен ли трафик, переданный через порт, содержать сведения о 802.1 P.</span><span class="sxs-lookup"><span data-stu-id="46172-116">Specifies whether traffic to/from the port retains 802.1P information.</span></span> <span data-ttu-id="46172-117">Содержит **значение true** , если трафик к порту или в него 802.1 сведения о p или **значение false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="46172-117">Contains **True** if traffic to/from the port retains 802.1P information or **False** otherwise.</span></span> <span data-ttu-id="46172-118">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="46172-118">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="46172-119">**алловмакспуфинг**</span><span class="sxs-lookup"><span data-stu-id="46172-119">**AllowMacSpoofing**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-120">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-120">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-121">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-121">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-122">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-122">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-123">Указывает, будет ли порт разрешать подмену MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="46172-123">Indicates whether the port will allow MAC spoofing.</span></span> <span data-ttu-id="46172-124">Если это свойство имеет **значение true**, порт разрешит подмену MAC-адресов.</span><span class="sxs-lookup"><span data-stu-id="46172-124">If this property is **True**, the port will allow MAC addresses to be spoofed.</span></span> <span data-ttu-id="46172-125">Разрешены все допустимые значения MAC-адреса одноадресной рассылки.</span><span class="sxs-lookup"><span data-stu-id="46172-125">All valid unicast MAC address values are allowed.</span></span> <span data-ttu-id="46172-126">Если это свойство имеет **значение false**, порт будет разрешать использование только MAC-адресов, настроенных в управлении Hyper/V.</span><span class="sxs-lookup"><span data-stu-id="46172-126">If this property is **False**, the port will only allow MAC addresses that are configured within Hyper-V management to be used.</span></span> <span data-ttu-id="46172-127">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="46172-127">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="46172-128">**алловтеаминг**</span><span class="sxs-lookup"><span data-stu-id="46172-128">**AllowTeaming**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-129">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-131">Квалификаторы: **вмидатаид** (8), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-131">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-132">Указывает, могут ли сетевые карты, подключенные к порту, быть частью команды.</span><span class="sxs-lookup"><span data-stu-id="46172-132">Indicates whether the NICs connected to the port can be part of a team.</span></span> <span data-ttu-id="46172-133">Это относится только к сетевым адаптерам, подключенным к виртуальным машинам.</span><span class="sxs-lookup"><span data-stu-id="46172-133">This applies only to NICs connected to virtual machines.</span></span> <span data-ttu-id="46172-134">Содержит **значение true** , если объединение сетевых карт разрешено или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="46172-134">Contains **True** if NIC teaming is allowed or **False** otherwise.</span></span> <span data-ttu-id="46172-135">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="46172-135">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="46172-136">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="46172-136">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46172-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46172-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46172-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46172-139">Краткое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="46172-139">A short description of the object.</span></span> <span data-ttu-id="46172-140">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры безопасности порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="46172-140">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="46172-141">**Описание**</span><span class="sxs-lookup"><span data-stu-id="46172-141">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46172-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46172-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46172-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46172-144">Описание объекта.</span><span class="sxs-lookup"><span data-stu-id="46172-144">A description of the object.</span></span> <span data-ttu-id="46172-145">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "представляет данные параметров функции безопасности".</span><span class="sxs-lookup"><span data-stu-id="46172-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the security feature setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="46172-146">**динамиЦипаддресслимит**</span><span class="sxs-lookup"><span data-stu-id="46172-146">**DynamicIPAddressLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46172-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46172-148">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-149">Квалификаторы: **вмидатаид** (12), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-149">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-150">Определяет предельное число полученных динамических IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="46172-150">Defines the limit for number of Dynamic IP addresses learned.</span></span> <span data-ttu-id="46172-151">Значение по умолчанию — none (Отсутствует).</span><span class="sxs-lookup"><span data-stu-id="46172-151">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="46172-152">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="46172-152">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46172-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46172-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46172-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="46172-155">Отображаемое имя объекта.</span><span class="sxs-lookup"><span data-stu-id="46172-155">A display name for the object.</span></span> <span data-ttu-id="46172-156">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "Параметры безопасности порта коммутатора Ethernet".</span><span class="sxs-lookup"><span data-stu-id="46172-156">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Security Settings".</span></span>

</dd> <dt>

<span data-ttu-id="46172-157">**енабледхкпгуард**</span><span class="sxs-lookup"><span data-stu-id="46172-157">**EnableDhcpGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-158">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-159">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-160">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-160">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-161">Указывает, блокируются ли DHCP-предложения от порта.</span><span class="sxs-lookup"><span data-stu-id="46172-161">Specifies whether DHCP offers are blocked from the port.</span></span> <span data-ttu-id="46172-162">Содержит **значение true** , если предложения DHCP заблокированы с помощью порта или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="46172-162">Contains **True** if DHCP offers are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="46172-163">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="46172-163">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="46172-164">**EnableFixSpeed10G**</span><span class="sxs-lookup"><span data-stu-id="46172-164">**EnableFixSpeed10G**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-165">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-165">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-166">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-166">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-167">Квалификаторы: **вмидатаид** (14), **интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-167">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-168">Задайте значение TRUE, если для параметра фиксированная скорость 10G включено значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="46172-168">Set to TRUE if Fixed Speed 10G is enabled else FALSE.</span></span> <span data-ttu-id="46172-169">Значение по умолчанию — FALSE.</span><span class="sxs-lookup"><span data-stu-id="46172-169">Default value is FALSE.</span></span>

> [!Note]  
> <span data-ttu-id="46172-170">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46172-170">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="46172-171">**енаблераутергуард**</span><span class="sxs-lookup"><span data-stu-id="46172-171">**EnableRouterGuard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-172">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-173">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-173">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-174">Квалификаторы: **вмидатаид** (3), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-174">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-175">Указывает, блокируются ли в порте объявления маршрутизатора и перенаправления маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="46172-175">Specifies whether router advertisements and router redirects are blocked from the port.</span></span> <span data-ttu-id="46172-176">Содержит **значение true** , если объявления маршрутизатора и перенаправления маршрутизаторов заблокированы с помощью порта или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="46172-176">Contains **True** if router advertisements and router redirects are blocked from the port or **False** otherwise.</span></span> <span data-ttu-id="46172-177">Значение по умолчанию равно **False**.</span><span class="sxs-lookup"><span data-stu-id="46172-177">The default value is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="46172-178">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="46172-178">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-179">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46172-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46172-180">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="46172-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="46172-181">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="46172-181">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="46172-182">Уникально идентифицирует экземпляр этого класса.</span><span class="sxs-lookup"><span data-stu-id="46172-182">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="46172-183">Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="46172-183">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="46172-184">**монитормоде**</span><span class="sxs-lookup"><span data-stu-id="46172-184">**MonitorMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-185">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="46172-185">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="46172-186">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-186">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-187">Квалификаторы: **вмидатаид** (4), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-187">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-188">Указывает режим монитора для порта.</span><span class="sxs-lookup"><span data-stu-id="46172-188">This indicates the monitor mode of the port.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="46172-189">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-189">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

<span data-ttu-id="46172-190">**Назначение** (1)</span><span class="sxs-lookup"><span data-stu-id="46172-190">**Destination** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

<span data-ttu-id="46172-191">**Источник** (2)</span><span class="sxs-lookup"><span data-stu-id="46172-191">**Source** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="46172-192">**мониторсессион**</span><span class="sxs-lookup"><span data-stu-id="46172-192">**MonitorSession**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-193">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="46172-193">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="46172-194">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-194">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-195">Квалификаторы: **вмидатаид** (5), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-195">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-196">Указывает идентификатор сеанса монитора, к которому принадлежит этот порт.</span><span class="sxs-lookup"><span data-stu-id="46172-196">Specifies the identifier of the monitor session this port belongs to.</span></span>

</dd> <dt>

<span data-ttu-id="46172-197">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="46172-197">**Reserved**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-198">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="46172-198">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="46172-199">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-199">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-200">Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), **вмидатаид** (13), **Интерфацеверсион** (3), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-200">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("No value"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-201">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="46172-201">Reserved</span></span>

> [!Note]  
> <span data-ttu-id="46172-202">Свойство добавлено в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="46172-202">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="46172-203">**стормлимит**</span><span class="sxs-lookup"><span data-stu-id="46172-203">**StormLimit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-204">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46172-204">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46172-205">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-205">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-206">Квалификаторы: **вмидатаид** (11), **интерфацеверсион** (2), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-206">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-207">Определяет ограничение количества пакетов в секунду для широковещательного и многоадресного трафика.</span><span class="sxs-lookup"><span data-stu-id="46172-207">Defines the packets per second limit for broadcast and multicast traffic.</span></span> <span data-ttu-id="46172-208">Значение по умолчанию — none (Отсутствует).</span><span class="sxs-lookup"><span data-stu-id="46172-208">Default is none.</span></span>

</dd> <dt>

<span data-ttu-id="46172-209">**теамнаме**</span><span class="sxs-lookup"><span data-stu-id="46172-209">**TeamName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-210">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="46172-210">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="46172-211">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-211">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-212">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **вмидатаид** (9), **Интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-212">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-213">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="46172-213">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="46172-214">**теамнумбер**</span><span class="sxs-lookup"><span data-stu-id="46172-214">**TeamNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-215">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46172-215">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46172-216">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-216">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-217">Квалификаторы: **вмидатаид** (10), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="46172-217">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="46172-218">Зарезервировано для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="46172-218">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="46172-219">**VirtualSubnetId**</span><span class="sxs-lookup"><span data-stu-id="46172-219">**VirtualSubnetId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="46172-220">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="46172-220">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="46172-221">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="46172-221">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="46172-222">Квалификаторы: **вмидатаид** (7), **интерфацеверсион** (1), **Интерфацеревисион** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span><span class="sxs-lookup"><span data-stu-id="46172-222">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)</span></span>
</dt> </dl>

<span data-ttu-id="46172-223">Указывает идентификатор виртуальной подсети, членом которой является порт.</span><span class="sxs-lookup"><span data-stu-id="46172-223">Specifies the identifier of the virtual subnet that the port is a member of.</span></span> <span data-ttu-id="46172-224">Значение по умолчанию — none.</span><span class="sxs-lookup"><span data-stu-id="46172-224">The default is none.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="46172-225">Требования</span><span class="sxs-lookup"><span data-stu-id="46172-225">Requirements</span></span>



| <span data-ttu-id="46172-226">Требование</span><span class="sxs-lookup"><span data-stu-id="46172-226">Requirement</span></span> | <span data-ttu-id="46172-227">Значение</span><span class="sxs-lookup"><span data-stu-id="46172-227">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46172-228">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46172-228">Minimum supported client</span></span><br/> | <span data-ttu-id="46172-229">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="46172-229">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="46172-230">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46172-230">Minimum supported server</span></span><br/> | <span data-ttu-id="46172-231">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="46172-231">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="46172-232">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="46172-232">Namespace</span></span><br/>                | <span data-ttu-id="46172-233">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="46172-233">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="46172-234">MOF</span><span class="sxs-lookup"><span data-stu-id="46172-234">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46172-235"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="46172-235"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="46172-236">DLL</span><span class="sxs-lookup"><span data-stu-id="46172-236">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46172-237"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="46172-237"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

