---
description: Представляет параметры объединения сетевых карт.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Класс Msvm_VirtualEthernetSwitchNicTeamingSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819489"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a><span data-ttu-id="1a77d-103">\_Класс мсвм виртуалесернетсвитчниктеамингсеттингдата</span><span class="sxs-lookup"><span data-stu-id="1a77d-103">Msvm\_VirtualEthernetSwitchNicTeamingSettingData class</span></span>

<span data-ttu-id="1a77d-104">Представляет параметры объединения сетевых карт.</span><span class="sxs-lookup"><span data-stu-id="1a77d-104">Represents the switch nic teaming settings.</span></span>

<span data-ttu-id="1a77d-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="1a77d-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a77d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a77d-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a><span data-ttu-id="1a77d-107">Члены</span><span class="sxs-lookup"><span data-stu-id="1a77d-107">Members</span></span>

<span data-ttu-id="1a77d-108">Класс **мсвм \_ виртуалесернетсвитчниктеамингсеттингдата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1a77d-108">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="1a77d-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a77d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1a77d-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="1a77d-110">Properties</span></span>

<span data-ttu-id="1a77d-111">Класс **мсвм \_ виртуалесернетсвитчниктеамингсеттингдата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="1a77d-111">The **Msvm\_VirtualEthernetSwitchNicTeamingSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1a77d-112">**лоадбаланЦингалгорисм**</span><span class="sxs-lookup"><span data-stu-id="1a77d-112">**LoadBalancingAlgorithm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a77d-113">Тип данных: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1a77d-113">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="1a77d-114">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1a77d-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1a77d-115">Квалификаторы: **вмидатаид** (2), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="1a77d-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1a77d-116">Алгоритм балансировки нагрузки.</span><span class="sxs-lookup"><span data-stu-id="1a77d-116">The load balancing algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="1a77d-117">**теамингмоде**</span><span class="sxs-lookup"><span data-stu-id="1a77d-117">**TeamingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1a77d-118">Тип данных: **UINT32**</span><span class="sxs-lookup"><span data-stu-id="1a77d-118">Data type: **UINT32**</span></span>
</dt> <dt>

<span data-ttu-id="1a77d-119">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="1a77d-119">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1a77d-120">Квалификаторы: **вмидатаид** (1), **интерфацеверсион** (1), **интерфацеревисион** (0)</span><span class="sxs-lookup"><span data-stu-id="1a77d-120">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="1a77d-121">Режим объединения.</span><span class="sxs-lookup"><span data-stu-id="1a77d-121">The teaming mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a77d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="1a77d-122">Requirements</span></span>



| <span data-ttu-id="1a77d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="1a77d-123">Requirement</span></span> | <span data-ttu-id="1a77d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="1a77d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a77d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a77d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="1a77d-126">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1a77d-126">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="1a77d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a77d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="1a77d-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1a77d-128">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="1a77d-129">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1a77d-129">Namespace</span></span><br/>                | <span data-ttu-id="1a77d-130">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="1a77d-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="1a77d-131">MOF</span><span class="sxs-lookup"><span data-stu-id="1a77d-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a77d-132"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a77d-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a77d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1a77d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a77d-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1a77d-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="1a77d-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a77d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a77d-136">**Мсвм \_ есернетсвитчфеатуресеттингдата**</span><span class="sxs-lookup"><span data-stu-id="1a77d-136">**Msvm\_EthernetSwitchFeatureSettingData**</span></span>](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




