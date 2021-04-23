---
title: Интерфейс Инапсистемхеалсажентбиндинг (Напсистемхеалсажент. h)
description: SHA использует для взаимодействия с Напажент. | Интерфейс Инапсистемхеалсажентбиндинг (Напсистемхеалсажент. h)
ms.assetid: 9366f61f-086a-4f44-900e-9ec3165a35ba
keywords:
- Инапсистемхеалсажентбиндинг интерфейса NAP
- Инапсистемхеалсажентбиндинг интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d38d1331996e34c6879fc2e98ce566ce6802527a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105674665"
---
# <a name="inapsystemhealthagentbinding-interface"></a><span data-ttu-id="56ae0-106">Интерфейс Инапсистемхеалсажентбиндинг</span><span class="sxs-lookup"><span data-stu-id="56ae0-106">INapSystemHealthAgentBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="56ae0-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="56ae0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="56ae0-108">**Инапсистемхеалсажентбиндинг** предоставляет методы, которые SHA использует для взаимодействия с напажент.</span><span class="sxs-lookup"><span data-stu-id="56ae0-108">The **INapSystemHealthAgentBinding** provides methods that the SHAs use to communicate with the NapAgent.</span></span>

> [!Note]  
> <span data-ttu-id="56ae0-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) наследует все методы этого интерфейса, и вместо него следует использовать.</span><span class="sxs-lookup"><span data-stu-id="56ae0-109">[**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="56ae0-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="56ae0-110">Members</span></span>

<span data-ttu-id="56ae0-111">Интерфейс **инапсистемхеалсажентбиндинг** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="56ae0-111">The **INapSystemHealthAgentBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56ae0-112">**Инапсистемхеалсажентбиндинг** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="56ae0-112">**INapSystemHealthAgentBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="56ae0-113">Методы</span><span class="sxs-lookup"><span data-stu-id="56ae0-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56ae0-114">Методы</span><span class="sxs-lookup"><span data-stu-id="56ae0-114">Methods</span></span>

<span data-ttu-id="56ae0-115">Интерфейс **инапсистемхеалсажентбиндинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="56ae0-115">The **INapSystemHealthAgentBinding** interface has these methods.</span></span>



| <span data-ttu-id="56ae0-116">Метод</span><span class="sxs-lookup"><span data-stu-id="56ae0-116">Method</span></span>                                                                                                                     | <span data-ttu-id="56ae0-117">Описание</span><span class="sxs-lookup"><span data-stu-id="56ae0-117">Description</span></span>                                                                                        |
|:---------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56ae0-118">**Инапсистемхеалсажентбиндинг:: Флушкаче**</span><span class="sxs-lookup"><span data-stu-id="56ae0-118">**INapSystemHealthAgentBinding::FlushCache**</span></span>](inapsystemhealthagentbinding-flushcache-method.md)                         | <span data-ttu-id="56ae0-119">Вызывается SHA для сброса кэша SoH.</span><span class="sxs-lookup"><span data-stu-id="56ae0-119">Called by an SHA to flush its SoH cache.</span></span><br/>                                                |
| [<span data-ttu-id="56ae0-120">**Инапсистемхеалсажентбиндинг:: Жетсистемисолатионинфо**</span><span class="sxs-lookup"><span data-stu-id="56ae0-120">**INapSystemHealthAgentBinding::GetSystemIsolationInfo**</span></span>](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) | <span data-ttu-id="56ae0-121">Вызывается SHA для определения состояния изоляции системы.</span><span class="sxs-lookup"><span data-stu-id="56ae0-121">Called by SHAs to determine the system isolation state.</span></span><br/>                                 |
| [<span data-ttu-id="56ae0-122">**Инапсистемхеалсажентбиндинг:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="56ae0-122">**INapSystemHealthAgentBinding::Initialize**</span></span>](inapsystemhealthagentbinding-initialize-method.md)                         | <span data-ttu-id="56ae0-123">Инициализирует SHA и привязывает SHA к службе Напажент.</span><span class="sxs-lookup"><span data-stu-id="56ae0-123">Initializes the SHA and binds the SHA to the NapAgent service.</span></span> <br/>                         |
| [<span data-ttu-id="56ae0-124">**Инапсистемхеалсажентбиндинг:: Нотифисохчанже**</span><span class="sxs-lookup"><span data-stu-id="56ae0-124">**INapSystemHealthAgentBinding::NotifySoHChange**</span></span>](inapsystemhealthagentbinding-notifysohchange-method.md)               | <span data-ttu-id="56ae0-125">Вызывается SHA при изменении состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="56ae0-125">Called by SHAs when their SoH changes.</span></span><br/>                                                  |
| [<span data-ttu-id="56ae0-126">**Инапсистемхеалсажентбиндинг:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="56ae0-126">**INapSystemHealthAgentBinding::Uninitialize**</span></span>](inapsystemhealthagentbinding-uninitialize-method.md)                     | <span data-ttu-id="56ae0-127">Вызывается SHA для того, чтобы Напажент освободил все ссылки на указатели SHA COM.</span><span class="sxs-lookup"><span data-stu-id="56ae0-127">Called by SHAs to cause the NapAgent to release all its references to SHA COM pointers.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="56ae0-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56ae0-128">Remarks</span></span>

<span data-ttu-id="56ae0-129">Все API-интерфейсы в этом интерфейсе будут возвращать **RPC \_ E \_ disconnected** , если напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="56ae0-129">All the APIs in this interface will return **RPC\_E\_DISCONNECTED** if the NapAgent is stopped.</span></span> <span data-ttu-id="56ae0-130">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="56ae0-130">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ae0-131">Требования</span><span class="sxs-lookup"><span data-stu-id="56ae0-131">Requirements</span></span>



| <span data-ttu-id="56ae0-132">Требование</span><span class="sxs-lookup"><span data-stu-id="56ae0-132">Requirement</span></span> | <span data-ttu-id="56ae0-133">Значение</span><span class="sxs-lookup"><span data-stu-id="56ae0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56ae0-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56ae0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="56ae0-135">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56ae0-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56ae0-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56ae0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="56ae0-137">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56ae0-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56ae0-138">Header</span><span class="sxs-lookup"><span data-stu-id="56ae0-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ae0-139"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ae0-139"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="56ae0-140">IDL</span><span class="sxs-lookup"><span data-stu-id="56ae0-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56ae0-141"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56ae0-141"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="56ae0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="56ae0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56ae0-143"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56ae0-143"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="56ae0-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56ae0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ae0-145">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="56ae0-145">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="56ae0-146">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="56ae0-146">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

