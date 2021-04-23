---
description: Представляет порт коммутатора, который отправляет и получает кадры данных.
ms.assetid: 015eed2a-1393-40ef-a190-832ab48766f9
title: Класс CIM_SwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchPort
- CIM_SwitchPort.PortNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf63843fc5a246012d3af6a059c897956d6f19b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998562"
---
# <a name="cim_switchport-class"></a><span data-ttu-id="479ac-103">\_Класс CIM свитчпорт</span><span class="sxs-lookup"><span data-stu-id="479ac-103">CIM\_SwitchPort class</span></span>

<span data-ttu-id="479ac-104">Представляет порт коммутатора, который отправляет и получает кадры данных.</span><span class="sxs-lookup"><span data-stu-id="479ac-104">Represents a switch port that sends and receives data frames.</span></span>

## <a name="syntax"></a><span data-ttu-id="479ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="479ac-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints")]
class CIM_SwitchPort : CIM_ProtocolEndpoint
{
  uint16 PortNumber;
};
```

## <a name="members"></a><span data-ttu-id="479ac-106">Члены</span><span class="sxs-lookup"><span data-stu-id="479ac-106">Members</span></span>

<span data-ttu-id="479ac-107">Класс **CIM \_ свитчпорт** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="479ac-107">The **CIM\_SwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="479ac-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="479ac-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="479ac-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="479ac-109">Properties</span></span>

<span data-ttu-id="479ac-110">Класс **CIM \_ свитчпорт** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="479ac-110">The **CIM\_SwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="479ac-111">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="479ac-111">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="479ac-112">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="479ac-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="479ac-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="479ac-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="479ac-114">Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. \|Мост IETF — MIB. dot1dPort ")</span><span class="sxs-lookup"><span data-stu-id="479ac-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dPort")</span></span>
</dt> </dl>

<span data-ttu-id="479ac-115">Числовой идентификатор порта коммутатора.</span><span class="sxs-lookup"><span data-stu-id="479ac-115">The numeric identifier of the switch port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="479ac-116">Требования</span><span class="sxs-lookup"><span data-stu-id="479ac-116">Requirements</span></span>



| <span data-ttu-id="479ac-117">Требование</span><span class="sxs-lookup"><span data-stu-id="479ac-117">Requirement</span></span> | <span data-ttu-id="479ac-118">Значение</span><span class="sxs-lookup"><span data-stu-id="479ac-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="479ac-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="479ac-119">Minimum supported client</span></span><br/> | <span data-ttu-id="479ac-120">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="479ac-120">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="479ac-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="479ac-121">Minimum supported server</span></span><br/> | <span data-ttu-id="479ac-122">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="479ac-122">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="479ac-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="479ac-123">Namespace</span></span><br/>                | <span data-ttu-id="479ac-124">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="479ac-124">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="479ac-125">MOF</span><span class="sxs-lookup"><span data-stu-id="479ac-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="479ac-126"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="479ac-126"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="479ac-127">DLL</span><span class="sxs-lookup"><span data-stu-id="479ac-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="479ac-128"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="479ac-128"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="479ac-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="479ac-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="479ac-130">**\_ПРОТОКОЛЕНДПОИНТ CIM**</span><span class="sxs-lookup"><span data-stu-id="479ac-130">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

