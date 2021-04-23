---
title: Интерфейс Инапклиентманажемент (Напманажемент. h)
description: Предоставляет методы для управления клиентами NAP. | Интерфейс Инапклиентманажемент (Напманажемент. h)
ms.assetid: 9c5724db-1e85-4da5-92b7-9ff6579f9cfb
keywords:
- Инапклиентманажемент интерфейса NAP
- Инапклиентманажемент интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapClientManagement
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe90158d6f1e9a864f7d19448a412d70890133d2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000206"
---
# <a name="inapclientmanagement-interface"></a><span data-ttu-id="bd767-106">Интерфейс Инапклиентманажемент</span><span class="sxs-lookup"><span data-stu-id="bd767-106">INapClientManagement interface</span></span>

> [!Note]  
> <span data-ttu-id="bd767-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="bd767-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="bd767-108">Интерфейс **инапклиентманажемент** предоставляет методы для управления клиентами NAP.</span><span class="sxs-lookup"><span data-stu-id="bd767-108">The **INapClientManagement** interface provides methods for NAP client management.</span></span>

> [!Note]  
> <span data-ttu-id="bd767-109">[**INapClientManagement2**](inapclientmanagement2.md) наследует все методы этого интерфейса, и вместо него следует использовать.</span><span class="sxs-lookup"><span data-stu-id="bd767-109">[**INapClientManagement2**](inapclientmanagement2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="bd767-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="bd767-110">Members</span></span>

<span data-ttu-id="bd767-111">Интерфейс **инапклиентманажемент** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bd767-111">The **INapClientManagement** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bd767-112">**Инапклиентманажемент** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bd767-112">**INapClientManagement** also has these types of members:</span></span>

-   [<span data-ttu-id="bd767-113">Методы</span><span class="sxs-lookup"><span data-stu-id="bd767-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bd767-114">Методы</span><span class="sxs-lookup"><span data-stu-id="bd767-114">Methods</span></span>

<span data-ttu-id="bd767-115">Интерфейс **инапклиентманажемент** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bd767-115">The **INapClientManagement** interface has these methods.</span></span>



| <span data-ttu-id="bd767-116">Метод</span><span class="sxs-lookup"><span data-stu-id="bd767-116">Method</span></span>                                                                                                                | <span data-ttu-id="bd767-117">Описание</span><span class="sxs-lookup"><span data-stu-id="bd767-117">Description</span></span>                                                                   |
|:----------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="bd767-118">**Инапклиентманажемент:: Жетнапклиентинфо**</span><span class="sxs-lookup"><span data-stu-id="bd767-118">**INapClientManagement::GetNapClientInfo**</span></span>](inapclientmanagement-getnapclientinfo.md)                               | <span data-ttu-id="bd767-119">Извлекает сведения о клиенте NAP.</span><span class="sxs-lookup"><span data-stu-id="bd767-119">Retrieves information about a NAP client.</span></span><br/>                          |
| [<span data-ttu-id="bd767-120">**Инапклиентманажемент:: Жетрегистереденфорцементклиентс**</span><span class="sxs-lookup"><span data-stu-id="bd767-120">**INapClientManagement::GetRegisteredEnforcementClients**</span></span>](inapclientmanagement-getregisteredenforcementclients.md) | <span data-ttu-id="bd767-121">Извлекает сведения о зарегистрированных клиентах принудительной установки.</span><span class="sxs-lookup"><span data-stu-id="bd767-121">Retrieves information about the registered enforcement clients.</span></span><br/>    |
| [<span data-ttu-id="bd767-122">**Инапклиентманажемент:: Жетрегистередсистемхеалсажентс**</span><span class="sxs-lookup"><span data-stu-id="bd767-122">**INapClientManagement::GetRegisteredSystemHealthAgents**</span></span>](inapclientmanagement-getregisteredsystemhealthagents.md) | <span data-ttu-id="bd767-123">Получение сведений о зарегистрированном SHA.</span><span class="sxs-lookup"><span data-stu-id="bd767-123">Retrieve information about a registered SHA.</span></span><br/>                       |
| [<span data-ttu-id="bd767-124">**Инапклиентманажемент:: Жетсистемисолатионинфо**</span><span class="sxs-lookup"><span data-stu-id="bd767-124">**INapClientManagement::GetSystemIsolationInfo**</span></span>](inapclientmanagement-getsystemisolationinfo.md)                   | <span data-ttu-id="bd767-125">Извлекает сведения о состоянии изоляции клиента NAP.</span><span class="sxs-lookup"><span data-stu-id="bd767-125">Retrieves information about the isolation state of the Nap client.</span></span><br/> |
| [<span data-ttu-id="bd767-126">**Инапклиентманажемент:: Регистеренфорцементклиент**</span><span class="sxs-lookup"><span data-stu-id="bd767-126">**INapClientManagement::RegisterEnforcementClient**</span></span>](inapclientmanagement-registerenforcementclient.md)             | <span data-ttu-id="bd767-127">Регистрирует клиент принудительного применения в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="bd767-127">Registers an enforcement client with the NAP system.</span></span><br/>               |
| [<span data-ttu-id="bd767-128">**Инапклиентманажемент:: Регистерсистемхеалсажент**</span><span class="sxs-lookup"><span data-stu-id="bd767-128">**INapClientManagement::RegisterSystemHealthAgent**</span></span>](inapclientmanagement-registersystemhealthagent.md)             | <span data-ttu-id="bd767-129">Регистрирует SHA в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="bd767-129">Registers an SHA with the NAP system.</span></span><br/>                              |
| [<span data-ttu-id="bd767-130">**Инапклиентманажемент:: Унрегистеренфорцементклиент**</span><span class="sxs-lookup"><span data-stu-id="bd767-130">**INapClientManagement::UnregisterEnforcementClient**</span></span>](inapclientmanagement-unregisterenforcementclient.md)         | <span data-ttu-id="bd767-131">Отменяет регистрацию клиента принудительного применения в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="bd767-131">Unregisters an enforcement client with the NAP system.</span></span><br/>             |
| [<span data-ttu-id="bd767-132">**Инапклиентманажемент:: Унрегистерсистемхеалсажент**</span><span class="sxs-lookup"><span data-stu-id="bd767-132">**INapClientManagement::UnregisterSystemHealthAgent**</span></span>](inapclientmanagement-unregistersystemhealthagent.md)         | <span data-ttu-id="bd767-133">Отменяет регистрацию SHA в системе защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="bd767-133">Unregisters an SHA with the NAP system.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="bd767-134">Требования</span><span class="sxs-lookup"><span data-stu-id="bd767-134">Requirements</span></span>



| <span data-ttu-id="bd767-135">Требование</span><span class="sxs-lookup"><span data-stu-id="bd767-135">Requirement</span></span> | <span data-ttu-id="bd767-136">Значение</span><span class="sxs-lookup"><span data-stu-id="bd767-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd767-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bd767-137">Minimum supported client</span></span><br/> | <span data-ttu-id="bd767-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bd767-138">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="bd767-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bd767-139">Minimum supported server</span></span><br/> | <span data-ttu-id="bd767-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bd767-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="bd767-141">Header</span><span class="sxs-lookup"><span data-stu-id="bd767-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd767-142"><dt>Напманажемент. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd767-142"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd767-143">IDL</span><span class="sxs-lookup"><span data-stu-id="bd767-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd767-144"><dt>Напманажемент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd767-144"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd767-145">DLL</span><span class="sxs-lookup"><span data-stu-id="bd767-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd767-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd767-146"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="bd767-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bd767-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd767-148">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="bd767-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="bd767-149">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="bd767-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

