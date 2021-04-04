---
description: Представляет прозрачный аспект моста для \_ объекта СВИТЧСЕРВИЦЕ CIM.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: Класс CIM_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908731"
---
# <a name="cim_transparentbridgingservice-class"></a><span data-ttu-id="be2ed-103">\_Класс CIM транспарентбридгингсервице</span><span class="sxs-lookup"><span data-stu-id="be2ed-103">CIM\_TransparentBridgingService class</span></span>

<span data-ttu-id="be2ed-104">Представляет прозрачный аспект моста для объекта [**\_ свитчсервице CIM**](cim-switchservice.md) .</span><span class="sxs-lookup"><span data-stu-id="be2ed-104">Represents the transparent bridging aspect of a [**CIM\_SwitchService**](cim-switchservice.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="be2ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be2ed-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a><span data-ttu-id="be2ed-106">Члены</span><span class="sxs-lookup"><span data-stu-id="be2ed-106">Members</span></span>

<span data-ttu-id="be2ed-107">Класс **CIM \_ транспарентбридгингсервице** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="be2ed-107">The **CIM\_TransparentBridgingService** class has these types of members:</span></span>

-   [<span data-ttu-id="be2ed-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="be2ed-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be2ed-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="be2ed-109">Properties</span></span>

<span data-ttu-id="be2ed-110">Класс **CIM \_ транспарентбридгингсервице** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="be2ed-110">The **CIM\_TransparentBridgingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be2ed-111">**агингтиме**</span><span class="sxs-lookup"><span data-stu-id="be2ed-111">**AgingTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be2ed-112">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be2ed-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be2ed-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be2ed-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="be2ed-114">Квалификаторы: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**Маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dTpAgingTime ")</span><span class="sxs-lookup"><span data-stu-id="be2ed-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Seconds"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpAgingTime")</span></span>
</dt> </dl>

<span data-ttu-id="be2ed-115">Период времени ожидания (в секундах), в течение которого динамически изучена информация о пересылке.</span><span class="sxs-lookup"><span data-stu-id="be2ed-115">The timeout period, in seconds, for aging out dynamically learned forwarding information.</span></span> <span data-ttu-id="be2ed-116">Стандарт 802.1 D-1990 рекомендует значение по умолчанию, равное 300 секундам.</span><span class="sxs-lookup"><span data-stu-id="be2ed-116">The 802.1D-1990 standard recommends a default of 300 seconds.</span></span>

</dd> <dt>

<span data-ttu-id="be2ed-117">**FID**</span><span class="sxs-lookup"><span data-stu-id="be2ed-117">**FID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be2ed-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="be2ed-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="be2ed-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="be2ed-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be2ed-120">Фильтрация идентификатора базы данных, используемого коммутаторами с поддержкой VLAN, которые имеют более одной фильтрации базы данных.</span><span class="sxs-lookup"><span data-stu-id="be2ed-120">Filtering Database Identifier used by VLAN-aware switches that have more than one filtering database.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be2ed-121">Требования</span><span class="sxs-lookup"><span data-stu-id="be2ed-121">Requirements</span></span>



| <span data-ttu-id="be2ed-122">Требование</span><span class="sxs-lookup"><span data-stu-id="be2ed-122">Requirement</span></span> | <span data-ttu-id="be2ed-123">Значение</span><span class="sxs-lookup"><span data-stu-id="be2ed-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be2ed-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be2ed-124">Minimum supported client</span></span><br/> | <span data-ttu-id="be2ed-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="be2ed-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="be2ed-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be2ed-126">Minimum supported server</span></span><br/> | <span data-ttu-id="be2ed-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="be2ed-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="be2ed-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="be2ed-128">Namespace</span></span><br/>                | <span data-ttu-id="be2ed-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="be2ed-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="be2ed-130">MOF</span><span class="sxs-lookup"><span data-stu-id="be2ed-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be2ed-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be2ed-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="be2ed-132">DLL</span><span class="sxs-lookup"><span data-stu-id="be2ed-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be2ed-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="be2ed-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="be2ed-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be2ed-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be2ed-135">**\_ФОРВАРДИНГСЕРВИЦЕ CIM**</span><span class="sxs-lookup"><span data-stu-id="be2ed-135">**CIM\_ForwardingService**</span></span>](cim-forwardingservice.md)
</dt> </dl>

 

