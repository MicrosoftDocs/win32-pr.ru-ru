---
title: Интерфейс Инапенфорцементклиенткаллбакк (Напенфорцементклиент. h)
description: Клиенты принудительного применения должны реализовать, чтобы позволить Напажент взаимодействовать с ними.
ms.assetid: d7d63c5b-7952-4f04-9d3d-3f13b0b52d97
keywords:
- Инапенфорцементклиенткаллбакк интерфейса NAP
- Инапенфорцементклиенткаллбакк интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1d5c7e066115a6d51879775d9b8cfab3cbe4888
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672915"
---
# <a name="inapenforcementclientcallback-interface"></a><span data-ttu-id="f4c35-105">Интерфейс Инапенфорцементклиенткаллбакк</span><span class="sxs-lookup"><span data-stu-id="f4c35-105">INapEnforcementClientCallback interface</span></span>

> [!Note]  
> <span data-ttu-id="f4c35-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="f4c35-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f4c35-107">Интерфейс **инапенфорцементклиенткаллбакк** предоставляет методы обратного вызова, которые должны быть реализованы клиентами, чтобы позволить напажент взаимодействовать с ними.</span><span class="sxs-lookup"><span data-stu-id="f4c35-107">The **INapEnforcementClientCallback** interface provides callback methods that enforcement clients must implement to enable the NapAgent to communicate with them.</span></span>

## <a name="members"></a><span data-ttu-id="f4c35-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="f4c35-108">Members</span></span>

<span data-ttu-id="f4c35-109">Интерфейс **инапенфорцементклиенткаллбакк** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f4c35-109">The **INapEnforcementClientCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f4c35-110">**Инапенфорцементклиенткаллбакк** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f4c35-110">**INapEnforcementClientCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="f4c35-111">Методы</span><span class="sxs-lookup"><span data-stu-id="f4c35-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f4c35-112">Методы</span><span class="sxs-lookup"><span data-stu-id="f4c35-112">Methods</span></span>

<span data-ttu-id="f4c35-113">Интерфейс **инапенфорцементклиенткаллбакк** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f4c35-113">The **INapEnforcementClientCallback** interface has these methods.</span></span>



| <span data-ttu-id="f4c35-114">Метод</span><span class="sxs-lookup"><span data-stu-id="f4c35-114">Method</span></span>                                                                                                         | <span data-ttu-id="f4c35-115">Описание</span><span class="sxs-lookup"><span data-stu-id="f4c35-115">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="f4c35-116">**Инапенфорцементклиенткаллбакк:: соединений**</span><span class="sxs-lookup"><span data-stu-id="f4c35-116">**INapEnforcementClientCallback::GetConnections**</span></span>](inapenforcementclientcallback-getconnections-method.md)   | <span data-ttu-id="f4c35-117">Используется Напажент для получения соединений.</span><span class="sxs-lookup"><span data-stu-id="f4c35-117">Used by the NapAgent to retrieve connections.</span></span><br/>                         |
| [<span data-ttu-id="f4c35-118">**Инапенфорцементклиенткаллбакк:: Нотифисохчанже**</span><span class="sxs-lookup"><span data-stu-id="f4c35-118">**INapEnforcementClientCallback::NotifySoHChange**</span></span>](inapenforcementclientcallback-notifysohchange-method.md) | <span data-ttu-id="f4c35-119">Используется Напажент для информирования клиента принудительного применения об изменениях состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f4c35-119">Used by the NapAgent to inform the enforcement client of SoH changes.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f4c35-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f4c35-120">Requirements</span></span>



| <span data-ttu-id="f4c35-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f4c35-121">Requirement</span></span> | <span data-ttu-id="f4c35-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f4c35-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c35-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4c35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c35-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f4c35-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f4c35-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4c35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c35-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f4c35-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f4c35-127">Header</span><span class="sxs-lookup"><span data-stu-id="f4c35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4c35-128"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4c35-128"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="f4c35-129">IDL</span><span class="sxs-lookup"><span data-stu-id="f4c35-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4c35-130"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4c35-130"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



 

