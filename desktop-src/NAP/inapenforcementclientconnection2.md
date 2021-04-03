---
title: Интерфейс INapEnforcementClientConnection2 (Напенфорцементклиент. h)
description: Разрешить управление клиентскими подключениями. | Интерфейс INapEnforcementClientConnection2 (Напенфорцементклиент. h)
ms.assetid: f7b5d8cc-6a91-4e49-8957-cf67d1001089
keywords:
- INapEnforcementClientConnection2 интерфейса NAP
- INapEnforcementClientConnection2 интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3503e1bf6db01920e814b96e3daf5fe04eabc6b9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914360"
---
# <a name="inapenforcementclientconnection2-interface"></a><span data-ttu-id="4308a-106">Интерфейс INapEnforcementClientConnection2</span><span class="sxs-lookup"><span data-stu-id="4308a-106">INapEnforcementClientConnection2 interface</span></span>

> [!Note]  
> <span data-ttu-id="4308a-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="4308a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4308a-108">**INapEnforcementClientConnection2** предоставляет методы, позволяющие управлять подключениями клиентов.</span><span class="sxs-lookup"><span data-stu-id="4308a-108">The **INapEnforcementClientConnection2** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="4308a-109">Этот интерфейс наследует все методы [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) и использовать вместо него.</span><span class="sxs-lookup"><span data-stu-id="4308a-109">This interface inherits all the methods of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="4308a-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="4308a-110">Members</span></span>

<span data-ttu-id="4308a-111">Интерфейс **INapEnforcementClientConnection2** наследует от [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md).</span><span class="sxs-lookup"><span data-stu-id="4308a-111">The **INapEnforcementClientConnection2** interface inherits from [**INapEnforcementClientConnection**](inapenforcementclientconnection.md).</span></span> <span data-ttu-id="4308a-112">**INapEnforcementClientConnection2** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4308a-112">**INapEnforcementClientConnection2** also has these types of members:</span></span>

-   [<span data-ttu-id="4308a-113">Методы</span><span class="sxs-lookup"><span data-stu-id="4308a-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="4308a-114">Методы</span><span class="sxs-lookup"><span data-stu-id="4308a-114">Methods</span></span>

<span data-ttu-id="4308a-115">Интерфейс **INapEnforcementClientConnection2** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="4308a-115">The **INapEnforcementClientConnection2** interface has these methods.</span></span>



| <span data-ttu-id="4308a-116">Метод</span><span class="sxs-lookup"><span data-stu-id="4308a-116">Method</span></span>                                                                                                              | <span data-ttu-id="4308a-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4308a-117">Description</span></span>                                                                      |
|:--------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [<span data-ttu-id="4308a-118">**INapEnforcementClientConnection2:: Жетинсталледшвс**</span><span class="sxs-lookup"><span data-stu-id="4308a-118">**INapEnforcementClientConnection2::GetInstalledShvs**</span></span>](inapenforcementclientconnection2-getinstalledshvs.md)     | <span data-ttu-id="4308a-119">Используется для получения идентификаторов установленных SHV для клиента.</span><span class="sxs-lookup"><span data-stu-id="4308a-119">Used to get the IDs of the installed SHVs for the client.</span></span><br/>             |
| [<span data-ttu-id="4308a-120">**INapEnforcementClientConnection2:: Жетисолатионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="4308a-120">**INapEnforcementClientConnection2::GetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-getisolationinfoex.md) | <span data-ttu-id="4308a-121">Используется для получения сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="4308a-121">Used to get the isolation information for the client.</span></span><br/>                 |
| [<span data-ttu-id="4308a-122">**INapEnforcementClientConnection2:: Сетинсталледшвс**</span><span class="sxs-lookup"><span data-stu-id="4308a-122">**INapEnforcementClientConnection2::SetInstalledShvs**</span></span>](inapenforcementclientconnection2-setinstalledshvs.md)     | <span data-ttu-id="4308a-123">Используется Напажент для установки установленных идентификаторов SHV для клиента.</span><span class="sxs-lookup"><span data-stu-id="4308a-123">Used by the NapAgent to set the installed SHV IDs for the client.</span></span><br/>     |
| [<span data-ttu-id="4308a-124">**INapEnforcementClientConnection2:: Сетисолатионинфоекс**</span><span class="sxs-lookup"><span data-stu-id="4308a-124">**INapEnforcementClientConnection2::SetIsolationInfoEx**</span></span>](inapenforcementclientconnection2-setisolationinfoex.md) | <span data-ttu-id="4308a-125">Используется Напажент для установки сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="4308a-125">Used by the NapAgent to set the isolation information for the client.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4308a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="4308a-126">Requirements</span></span>



| <span data-ttu-id="4308a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="4308a-127">Requirement</span></span> | <span data-ttu-id="4308a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="4308a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4308a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4308a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4308a-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4308a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4308a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4308a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4308a-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4308a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4308a-133">Header</span><span class="sxs-lookup"><span data-stu-id="4308a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="4308a-134"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="4308a-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="4308a-135">IDL</span><span class="sxs-lookup"><span data-stu-id="4308a-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4308a-136"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4308a-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="4308a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="4308a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4308a-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4308a-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4308a-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4308a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4308a-140">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="4308a-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> <dt>

[<span data-ttu-id="4308a-141">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="4308a-141">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="4308a-142">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="4308a-142">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

 





