---
description: Представляет данные параметра изоляции.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Класс Msvm_EthernetSwitchPortIsolationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3d7761b090cfd3bf2ae6aaaa92e9c5d09d55eae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663589"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a><span data-ttu-id="d25d0-103">\_Класс мсвм есернетсвитчпортисолатионсеттингдата</span><span class="sxs-lookup"><span data-stu-id="d25d0-103">Msvm\_EthernetSwitchPortIsolationSettingData class</span></span>

<span data-ttu-id="d25d0-104">Представляет данные параметра изоляции.</span><span class="sxs-lookup"><span data-stu-id="d25d0-104">Represents the Isolation setting data.</span></span>

<span data-ttu-id="d25d0-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d25d0-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d25d0-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d25d0-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="d25d0-107">Члены</span><span class="sxs-lookup"><span data-stu-id="d25d0-107">Members</span></span>

<span data-ttu-id="d25d0-108">Класс **мсвм \_ есернетсвитчпортисолатионсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d25d0-108">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="d25d0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="d25d0-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d25d0-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="d25d0-110">Properties</span></span>

<span data-ttu-id="d25d0-111">Класс **мсвм \_ есернетсвитчпортисолатионсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d25d0-111">The **Msvm\_EthernetSwitchPortIsolationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d25d0-112">**алловунтагжедтраффик**</span><span class="sxs-lookup"><span data-stu-id="d25d0-112">**AllowUntaggedTraffic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d25d0-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d25d0-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d25d0-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-115">Квалификаторы: **вмидатаид** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d25d0-115">Qualifiers: **WmiDataId** (2), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d25d0-116">Разрешено ли порту отправлять и получать трафик без тегов.</span><span class="sxs-lookup"><span data-stu-id="d25d0-116">Whether the port is allowed to send/receive untagged traffic.</span></span>

</dd> <dt>

<span data-ttu-id="d25d0-117">**дефаултисолатионид**</span><span class="sxs-lookup"><span data-stu-id="d25d0-117">**DefaultIsolationId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d25d0-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d25d0-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d25d0-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-120">Квалификаторы: **вмидатаид** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d25d0-120">Qualifiers: **WmiDataId** (3), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d25d0-121">Значение по умолчанию VirtualSubnetId или VLAN, которое будет задано для всего трафика отправки и получения, если **алловедунтагжедтраффик** имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-121">The default VirtualSubnetId or VLAN that will be set on all send/receive traffic if **AllowedUntaggedTraffic** is **true**.</span></span>

</dd> <dt>

<span data-ttu-id="d25d0-122">**енаблемултитенантстакк**</span><span class="sxs-lookup"><span data-stu-id="d25d0-122">**EnableMultiTenantStack**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d25d0-123">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="d25d0-123">Data type: **Boolean**</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-124">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d25d0-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-125">Квалификаторы: **вмидатаид** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d25d0-125">Qualifiers: **WmiDataId** (4), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d25d0-126">Если **значение — true**, сетевой стек на виртуальной машине сможет получить доступ к конфигурации изоляции.</span><span class="sxs-lookup"><span data-stu-id="d25d0-126">If **true**, the network stack in the VM will be able to access the isolation configuration.</span></span> <span data-ttu-id="d25d0-127">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="d25d0-127">The default value is **false**.</span></span>

</dd> <dt>

<span data-ttu-id="d25d0-128">**IsolationMode**</span><span class="sxs-lookup"><span data-stu-id="d25d0-128">**IsolationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d25d0-129">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d25d0-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-130">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="d25d0-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="d25d0-131">Квалификаторы: **вмидатаид** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Редакция**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="d25d0-131">Qualifiers: **WmiDataId** (1), [**Version**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revision**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="d25d0-132">Использует ли порт **виртуальную ЛС** или **VirtualSubnetId** для изоляции.</span><span class="sxs-lookup"><span data-stu-id="d25d0-132">Whether the port is using **VLAN** or **VirtualSubnetId** for isolation.</span></span> <span data-ttu-id="d25d0-133">**Нативевиртуалсубнетид** используется для сетей на основе WNV VirtualSubnetId.</span><span class="sxs-lookup"><span data-stu-id="d25d0-133">**NativeVirtualSubnetId** is used for WNV VirtualSubnetId-based networks.</span></span>

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="d25d0-134">**Нет** (0)</span><span class="sxs-lookup"><span data-stu-id="d25d0-134">**None** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

<span data-ttu-id="d25d0-135">**Нативевиртуалсубнетид** (1)</span><span class="sxs-lookup"><span data-stu-id="d25d0-135">**NativeVirtualSubnetId** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

<span data-ttu-id="d25d0-136">**Екстерналвиртуалсубнетид** (2)</span><span class="sxs-lookup"><span data-stu-id="d25d0-136">**ExternalVirtualSubnetId** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

<span data-ttu-id="d25d0-137">**Виртуальная ЛС** (3)</span><span class="sxs-lookup"><span data-stu-id="d25d0-137">**VLAN** (3)</span></span>


<span data-ttu-id="d25d0-138"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="d25d0-138"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="d25d0-139">Требования</span><span class="sxs-lookup"><span data-stu-id="d25d0-139">Requirements</span></span>



| <span data-ttu-id="d25d0-140">Требование</span><span class="sxs-lookup"><span data-stu-id="d25d0-140">Requirement</span></span> | <span data-ttu-id="d25d0-141">Значение</span><span class="sxs-lookup"><span data-stu-id="d25d0-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d25d0-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d25d0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="d25d0-143">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d25d0-143">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="d25d0-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d25d0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="d25d0-145">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="d25d0-145">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="d25d0-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d25d0-146">Namespace</span></span><br/>                | <span data-ttu-id="d25d0-147">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="d25d0-147">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d25d0-148">MOF</span><span class="sxs-lookup"><span data-stu-id="d25d0-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d25d0-149"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d25d0-149"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d25d0-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d25d0-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d25d0-151"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d25d0-151"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d25d0-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d25d0-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25d0-153">**Мсвм \_ есернетсвитчпортфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="d25d0-153">**Msvm\_EthernetSwitchPortFeatureSettingData**</span></span>](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

