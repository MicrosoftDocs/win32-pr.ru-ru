---
description: Представляет ассоциацию, в которой конечные точки протокола зависят от службы пересылки для пересылки данных.
ms.assetid: b63dbd2c-2842-498a-a352-b7ab7f7c841a
title: Класс CIM_ForwardsAmong
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardsAmong
- CIM_ForwardsAmong.Antecedent
- CIM_ForwardsAmong.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2b584f6472d8fbe3eb738d87652b796d9bb617f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682419"
---
# <a name="cim_forwardsamong-class"></a><span data-ttu-id="330b2-103">\_Класс CIM форвардсамонг</span><span class="sxs-lookup"><span data-stu-id="330b2-103">CIM\_ForwardsAmong class</span></span>

<span data-ttu-id="330b2-104">Представляет ассоциацию, в которой конечные точки протокола зависят от службы пересылки для пересылки данных.</span><span class="sxs-lookup"><span data-stu-id="330b2-104">Represents an association in which protocol endpoints depend on a forwarding service to forward data.</span></span>

## <a name="syntax"></a><span data-ttu-id="330b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="330b2-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::RoutingForwarding")]
class CIM_ForwardsAmong : CIM_ServiceSAPDependency
{
  CIM_ProtocolEndpoint  REF Antecedent;
  CIM_ForwardingService REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="330b2-106">Члены</span><span class="sxs-lookup"><span data-stu-id="330b2-106">Members</span></span>

<span data-ttu-id="330b2-107">Класс **CIM \_ форвардсамонг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="330b2-107">The **CIM\_ForwardsAmong** class has these types of members:</span></span>

-   [<span data-ttu-id="330b2-108">Свойства</span><span class="sxs-lookup"><span data-stu-id="330b2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="330b2-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="330b2-109">Properties</span></span>

<span data-ttu-id="330b2-110">Класс **CIM \_ форвардсамонг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="330b2-110">The **CIM\_ForwardsAmong** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="330b2-111">**Завершил**</span><span class="sxs-lookup"><span data-stu-id="330b2-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="330b2-112">Тип данных: **CIM \_ протоколендпоинт**</span><span class="sxs-lookup"><span data-stu-id="330b2-112">Data type: **CIM\_ProtocolEndpoint**</span></span>
</dt> <dt>

<span data-ttu-id="330b2-113">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="330b2-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="330b2-114">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="330b2-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="330b2-115">Конечные точки протокола отправляют и получают перенаправленные данные.</span><span class="sxs-lookup"><span data-stu-id="330b2-115">The protocol endpoints send and receive the forwarded data.</span></span>

</dd> <dt>

<span data-ttu-id="330b2-116">**Него**</span><span class="sxs-lookup"><span data-stu-id="330b2-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="330b2-117">Тип данных: **CIM \_ форвардингсервице**</span><span class="sxs-lookup"><span data-stu-id="330b2-117">Data type: **CIM\_ForwardingService**</span></span>
</dt> <dt>

<span data-ttu-id="330b2-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="330b2-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="330b2-119">Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")</span><span class="sxs-lookup"><span data-stu-id="330b2-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="330b2-120">Служба пересылки, которая перенаправляет данные.</span><span class="sxs-lookup"><span data-stu-id="330b2-120">The forwarding service that forwards the data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="330b2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="330b2-121">Requirements</span></span>



| <span data-ttu-id="330b2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="330b2-122">Requirement</span></span> | <span data-ttu-id="330b2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="330b2-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="330b2-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="330b2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="330b2-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="330b2-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="330b2-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="330b2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="330b2-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="330b2-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="330b2-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="330b2-128">Namespace</span></span><br/>                | <span data-ttu-id="330b2-129">Корневая \\ виртуализация \\ версии 2</span><span class="sxs-lookup"><span data-stu-id="330b2-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="330b2-130">MOF</span><span class="sxs-lookup"><span data-stu-id="330b2-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="330b2-131"><dt>Виндовсвиртуализатион. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="330b2-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="330b2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="330b2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="330b2-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="330b2-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="330b2-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="330b2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="330b2-135">**\_СЕРВИЦЕСАПДЕПЕНДЕНЦИ CIM**</span><span class="sxs-lookup"><span data-stu-id="330b2-135">**CIM\_ServiceSAPDependency**</span></span>](cim-servicesapdependency.md)
</dt> </dl>

 

