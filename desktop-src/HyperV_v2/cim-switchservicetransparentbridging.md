---
description: Представляет ассоциацию, в которой служба моста является компонентом службы коммутатора.
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: Класс CIM_SwitchServiceTransparentBridging
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662818"
---
# <a name="cim_switchservicetransparentbridging-class"></a><span data-ttu-id="0f8e0-103">\_Класс CIM свитчсервицетранспарентбридгинг</span><span class="sxs-lookup"><span data-stu-id="0f8e0-103">CIM\_SwitchServiceTransparentBridging class</span></span>

<span data-ttu-id="0f8e0-104">Представляет ассоциацию, в которой служба моста является компонентом службы коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0f8e0-104">Represents an association in which a bridge service is a component of a switch service.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f8e0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0f8e0-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="0f8e0-106">Члены</span><span class="sxs-lookup"><span data-stu-id="0f8e0-106">Members</span></span>

<span data-ttu-id="0f8e0-107">Класс **CIM \_ свитчсервицетранспарентбридгинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="0f8e0-107">The **CIM\_SwitchServiceTransparentBridging** class has these types of members:</span></span>

-   [<span data-ttu-id="0f8e0-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f8e0-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f8e0-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="0f8e0-109">Properties</span></span>

<span data-ttu-id="0f8e0-110">Класс **CIM \_ свитчсервицетранспарентбридгинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f8e0-110">The **CIM\_SwitchServiceTransparentBridging** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f8e0-111">**Ссылка**</span><span class="sxs-lookup"><span data-stu-id="0f8e0-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f8e0-112">Тип данных: **CIM \_ свитчсервице**</span><span class="sxs-lookup"><span data-stu-id="0f8e0-112">Data type: **CIM\_SwitchService**</span></span>
</dt> <dt>

<span data-ttu-id="0f8e0-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f8e0-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f8e0-114">Квалификаторы: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**reoverride**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0f8e0-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0f8e0-115">Ссылка [**CIM \_ свитчсервице**](cim-switchservice.md) на службу коммутатора.</span><span class="sxs-lookup"><span data-stu-id="0f8e0-115">A [**CIM\_SwitchService**](cim-switchservice.md) reference to the switch service.</span></span>

</dd> <dt>

<span data-ttu-id="0f8e0-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0f8e0-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f8e0-117">Тип данных: **CIM \_ транспарентбридгингсервице**</span><span class="sxs-lookup"><span data-stu-id="0f8e0-117">Data type: **CIM\_TransparentBridgingService**</span></span>
</dt> <dt>

<span data-ttu-id="0f8e0-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="0f8e0-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f8e0-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="0f8e0-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="0f8e0-120">Ссылка [**CIM \_ транспарентбридгингсервице**](cim-transparentbridgingservice.md) на службу моста компонентов.</span><span class="sxs-lookup"><span data-stu-id="0f8e0-120">A [**CIM\_TransparentBridgingService**](cim-transparentbridgingservice.md) reference to the component bridging service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f8e0-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0f8e0-121">Requirements</span></span>



| <span data-ttu-id="0f8e0-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0f8e0-122">Requirement</span></span> | <span data-ttu-id="0f8e0-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0f8e0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8e0-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0f8e0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0f8e0-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="0f8e0-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="0f8e0-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0f8e0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0f8e0-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="0f8e0-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="0f8e0-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0f8e0-128">Namespace</span></span><br/>                | <span data-ttu-id="0f8e0-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="0f8e0-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f8e0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0f8e0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f8e0-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f8e0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f8e0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0f8e0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f8e0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f8e0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f8e0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0f8e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8e0-135">**\_SERVICECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0f8e0-135">**CIM\_ServiceComponent**</span></span>](cim-servicecomponent.md)
</dt> </dl>

 

