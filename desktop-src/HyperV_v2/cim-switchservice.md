---
description: Представляет службу коммутатора.
ms.assetid: cf6319fa-7d69-4820-b0e0-775aad8b190c
title: Класс CIM_SwitchService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchService
- CIM_SwitchService.BridgeAddress
- CIM_SwitchService.NumPorts
- CIM_SwitchService.BridgeType
- CIM_SwitchService.BridgeAddressType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9abe6869c5b8ac61630091315e476ae232630717
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662820"
---
# <a name="cim_switchservice-class"></a><span data-ttu-id="02f07-103">\_Класс CIM свитчсервице</span><span class="sxs-lookup"><span data-stu-id="02f07-103">CIM\_SwitchService class</span></span>

<span data-ttu-id="02f07-104">Представляет службу коммутатора.</span><span class="sxs-lookup"><span data-stu-id="02f07-104">Represents a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="02f07-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02f07-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchService : CIM_ForwardingService
{
  string BridgeAddress;
  uint16 NumPorts;
  uint8  BridgeType;
  uint16 BridgeAddressType;
};
```

## <a name="members"></a><span data-ttu-id="02f07-106">Члены</span><span class="sxs-lookup"><span data-stu-id="02f07-106">Members</span></span>

<span data-ttu-id="02f07-107">Класс **CIM \_ свитчсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="02f07-107">The **CIM\_SwitchService** class has these types of members:</span></span>

-   [<span data-ttu-id="02f07-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="02f07-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="02f07-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="02f07-109">Properties</span></span>

<span data-ttu-id="02f07-110">Класс **CIM \_ свитчсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="02f07-110">The **CIM\_SwitchService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="02f07-111">**бриджеаддресс**</span><span class="sxs-lookup"><span data-stu-id="02f07-111">**BridgeAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02f07-112">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="02f07-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="02f07-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02f07-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02f07-114">Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dBaseBridgeAddress "), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ свитчсервице**.**Бриджеаддресстипе**")</span><span class="sxs-lookup"><span data-stu-id="02f07-114">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseBridgeAddress"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddressType**")</span></span>
</dt> </dl>

<span data-ttu-id="02f07-115">Адрес службы коммутатора, которая является частью уникального идентификатора службы.</span><span class="sxs-lookup"><span data-stu-id="02f07-115">The address of the switch service, which is a portion of the unique identifier of the service.</span></span>

</dd> <dt>

<span data-ttu-id="02f07-116">**бриджеаддресстипе**</span><span class="sxs-lookup"><span data-stu-id="02f07-116">**BridgeAddressType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02f07-117">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02f07-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="02f07-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02f07-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02f07-119">Квалификаторы: [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ свитчсервице**.**Бриджеаддресс**")</span><span class="sxs-lookup"><span data-stu-id="02f07-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SwitchService**.**BridgeAddress**")</span></span>
</dt> </dl>

<span data-ttu-id="02f07-120">Формат адресации, используемый для моста, и свойство **бриджеаддресс** .</span><span class="sxs-lookup"><span data-stu-id="02f07-120">The addressing format used for the bridge and the **BridgeAddress** property.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="02f07-121">**Другое** (1)</span><span class="sxs-lookup"><span data-stu-id="02f07-121">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="02f07-122">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="02f07-122">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="02f07-123">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="02f07-123">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC"></span><span id="mac"></span>

<span data-ttu-id="02f07-124">**Mac** (4)</span><span class="sxs-lookup"><span data-stu-id="02f07-124">**MAC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="MAC___Spanning_Tree_Priority"></span><span id="mac___spanning_tree_priority"></span><span id="MAC___SPANNING_TREE_PRIORITY"></span>

<span data-ttu-id="02f07-125">**Приоритет дерева Mac + с охватом** (5)</span><span class="sxs-lookup"><span data-stu-id="02f07-125">**MAC + Spanning Tree Priority** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02f07-126">**бриджетипе**</span><span class="sxs-lookup"><span data-stu-id="02f07-126">**BridgeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02f07-127">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="02f07-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="02f07-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02f07-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02f07-129">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dBaseType ")</span><span class="sxs-lookup"><span data-stu-id="02f07-129">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseType")</span></span>
</dt> </dl>

<span data-ttu-id="02f07-130">Тип выполняемой службы коммутации.</span><span class="sxs-lookup"><span data-stu-id="02f07-130">The type of switching service to perform.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="02f07-131">**Неизвестно** (1)</span><span class="sxs-lookup"><span data-stu-id="02f07-131">**Unknown** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Transparent-only"></span><span id="transparent-only"></span><span id="TRANSPARENT-ONLY"></span>

<span data-ttu-id="02f07-132">**Только прозрачный** (2)</span><span class="sxs-lookup"><span data-stu-id="02f07-132">**Transparent-only** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="SourceRoute-only"></span><span id="sourceroute-only"></span><span id="SOURCEROUTE-ONLY"></span>

<span data-ttu-id="02f07-133">**Только SourceRoute** (3)</span><span class="sxs-lookup"><span data-stu-id="02f07-133">**SourceRoute-only** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="SRT"></span><span id="srt"></span>

<span data-ttu-id="02f07-134">**SRT** (4)</span><span class="sxs-lookup"><span data-stu-id="02f07-134">**SRT** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="02f07-135">**нумпортс**</span><span class="sxs-lookup"><span data-stu-id="02f07-135">**NumPorts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="02f07-136">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="02f07-136">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="02f07-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="02f07-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="02f07-138">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dBaseNumPorts ")</span><span class="sxs-lookup"><span data-stu-id="02f07-138">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dBaseNumPorts")</span></span>
</dt> </dl>

<span data-ttu-id="02f07-139">Число портов коммутатора, управляемых этой службой коммутации.</span><span class="sxs-lookup"><span data-stu-id="02f07-139">The number of switch ports controlled by this switching service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="02f07-140">Требования</span><span class="sxs-lookup"><span data-stu-id="02f07-140">Requirements</span></span>



| <span data-ttu-id="02f07-141">Требование</span><span class="sxs-lookup"><span data-stu-id="02f07-141">Requirement</span></span> | <span data-ttu-id="02f07-142">Значение</span><span class="sxs-lookup"><span data-stu-id="02f07-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02f07-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="02f07-143">Minimum supported client</span></span><br/> | <span data-ttu-id="02f07-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="02f07-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="02f07-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="02f07-145">Minimum supported server</span></span><br/> | <span data-ttu-id="02f07-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="02f07-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="02f07-147">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="02f07-147">Namespace</span></span><br/>                | <span data-ttu-id="02f07-148">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="02f07-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="02f07-149">MOF</span><span class="sxs-lookup"><span data-stu-id="02f07-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="02f07-150"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="02f07-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="02f07-151">DLL</span><span class="sxs-lookup"><span data-stu-id="02f07-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02f07-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="02f07-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="02f07-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="02f07-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02f07-154">**\_ФОРВАРДИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="02f07-154">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

