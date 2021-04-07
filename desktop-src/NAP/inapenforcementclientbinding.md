---
title: Интерфейс Инапенфорцементклиентбиндинг (Напенфорцементклиент. h)
description: Клиенты принудительного применения используют для взаимодействия с Напажент.
ms.assetid: 73c5c9ad-f213-4d34-9262-996acb570a55
keywords:
- Инапенфорцементклиентбиндинг интерфейса NAP
- Инапенфорцементклиентбиндинг интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23db912c08e68adb1411527c90580a5620601752
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892709"
---
# <a name="inapenforcementclientbinding-interface"></a><span data-ttu-id="56d61-105">Интерфейс Инапенфорцементклиентбиндинг</span><span class="sxs-lookup"><span data-stu-id="56d61-105">INapEnforcementClientBinding interface</span></span>

> [!Note]  
> <span data-ttu-id="56d61-106">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="56d61-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="56d61-107">**Инапенфорцементклиентбиндинг** предоставляет методы, используемые клиентами для взаимодействия с напажент.</span><span class="sxs-lookup"><span data-stu-id="56d61-107">The **INapEnforcementClientBinding** provides methods that enforcement clients use to communicate with the NapAgent.</span></span>

## <a name="members"></a><span data-ttu-id="56d61-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="56d61-108">Members</span></span>

<span data-ttu-id="56d61-109">Интерфейс **инапенфорцементклиентбиндинг** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="56d61-109">The **INapEnforcementClientBinding** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56d61-110">**Инапенфорцементклиентбиндинг** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="56d61-110">**INapEnforcementClientBinding** also has these types of members:</span></span>

-   [<span data-ttu-id="56d61-111">Методы</span><span class="sxs-lookup"><span data-stu-id="56d61-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56d61-112">Методы</span><span class="sxs-lookup"><span data-stu-id="56d61-112">Methods</span></span>

<span data-ttu-id="56d61-113">Интерфейс **инапенфорцементклиентбиндинг** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="56d61-113">The **INapEnforcementClientBinding** interface has these methods.</span></span>



| <span data-ttu-id="56d61-114">Метод</span><span class="sxs-lookup"><span data-stu-id="56d61-114">Method</span></span>                                                                                                                           | <span data-ttu-id="56d61-115">Описание</span><span class="sxs-lookup"><span data-stu-id="56d61-115">Description</span></span>                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="56d61-116">**Инапенфорцементклиентбиндинг:: CreateConnection**</span><span class="sxs-lookup"><span data-stu-id="56d61-116">**INapEnforcementClientBinding::CreateConnection**</span></span>](inapenforcementclientbinding-createconnection-method.md)                   | <span data-ttu-id="56d61-117">Используется принудительными триггерами для создания объектов подключения.</span><span class="sxs-lookup"><span data-stu-id="56d61-117">Used by enforcers to create connection objects.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="56d61-118">**Инапенфорцементклиентбиндинг:: Жетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="56d61-118">**INapEnforcementClientBinding::GetSoHRequest**</span></span>](inapenforcementclientbinding-getsohrequest-method.md)                         | <span data-ttu-id="56d61-119">Используется клиентом принудительного применения, когда ему требуется запрос SoH для определенного соединения.</span><span class="sxs-lookup"><span data-stu-id="56d61-119">Used by the enforcement client when it needs an SoH-request for a particular connection.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="56d61-120">**Инапенфорцементклиентбиндинг:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="56d61-120">**INapEnforcementClientBinding::Initialize**</span></span>](inapenforcementclientbinding-initialize-method.md)                               | <span data-ttu-id="56d61-121">Запускает службу Напажент.</span><span class="sxs-lookup"><span data-stu-id="56d61-121">Starts up the NapAgent service.</span></span> <span data-ttu-id="56d61-122">Клиент принудительного применения должен вызвать этот метод перед вызовом любого другого метода этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="56d61-122">The enforcement client must call this method before calling any other method of this interface.</span></span><br/>                                                                            |
| [<span data-ttu-id="56d61-123">**Инапенфорцементклиентбиндинг:: Нотификоннектионстатедовн**</span><span class="sxs-lookup"><span data-stu-id="56d61-123">**INapEnforcementClientBinding::NotifyConnectionStateDown**</span></span>](inapenforcementclientbinding-notifyconnectionstatedown-method.md) | <span data-ttu-id="56d61-124">Используется для информирования Напажент о том, что подключение к клиенту принудительного применения было прервано.</span><span class="sxs-lookup"><span data-stu-id="56d61-124">Used to inform the NapAgent that a connection to an enforcement client has gone down.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="56d61-125">**Инапенфорцементклиентбиндинг:: Нотифисохчанжефаилуре**</span><span class="sxs-lookup"><span data-stu-id="56d61-125">**INapEnforcementClientBinding::NotifySoHChangeFailure**</span></span>](inapenforcementclientbinding-notifysohchangefailure-method.md)       | <span data-ttu-id="56d61-126">Используется клиентом принудительного применения для информирования Напажент о том, что ему не удалось обработать предыдущий [**инапенфорцементклиенткаллбакк:: нотифисохчанже**](inapenforcementclientcallback-notifysohchange-method.md).</span><span class="sxs-lookup"><span data-stu-id="56d61-126">Used by the enforcement client to inform the NapAgent that it could not process a previous [**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md).</span></span><br/> |
| [<span data-ttu-id="56d61-127">**Инапенфорцементклиентбиндинг::P Роцесссохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="56d61-127">**INapEnforcementClientBinding::ProcessSoHResponse**</span></span>](inapenforcementclientbinding-processsohresponse-method.md)               | <span data-ttu-id="56d61-128">Используется клиентами принудительного применения при получении SoH-Responseного большого двоичного объекта данных с сервера принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="56d61-128">Used by enforcement clients whenever they get an SoH-Response data blob from the enforcement server.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="56d61-129">**Инапенфорцементклиентбиндинг:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="56d61-129">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)                           | <span data-ttu-id="56d61-130">Завершает службу Напажент для этого клиентского подключения.</span><span class="sxs-lookup"><span data-stu-id="56d61-130">Concludes the NapAgent service for this client connection.</span></span><br/>                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="56d61-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56d61-131">Remarks</span></span>

<span data-ttu-id="56d61-132">Все API-интерфейсы в этом интерфейсе будут возвращать RPC \_ E \_ Disconnected, если напажент остановлен.</span><span class="sxs-lookup"><span data-stu-id="56d61-132">All the APIs in this interface will return RPC\_E\_DISCONNECTED if the NapAgent is stopped.</span></span> <span data-ttu-id="56d61-133">После перезапуска этот объект будет автоматически восстановлен и повторно привязан к Напажент.</span><span class="sxs-lookup"><span data-stu-id="56d61-133">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span>

## <a name="requirements"></a><span data-ttu-id="56d61-134">Требования</span><span class="sxs-lookup"><span data-stu-id="56d61-134">Requirements</span></span>



| <span data-ttu-id="56d61-135">Требование</span><span class="sxs-lookup"><span data-stu-id="56d61-135">Requirement</span></span> | <span data-ttu-id="56d61-136">Значение</span><span class="sxs-lookup"><span data-stu-id="56d61-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56d61-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56d61-137">Minimum supported client</span></span><br/> | <span data-ttu-id="56d61-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="56d61-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="56d61-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56d61-139">Minimum supported server</span></span><br/> | <span data-ttu-id="56d61-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="56d61-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="56d61-141">Header</span><span class="sxs-lookup"><span data-stu-id="56d61-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="56d61-142"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="56d61-142"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="56d61-143">IDL</span><span class="sxs-lookup"><span data-stu-id="56d61-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56d61-144"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56d61-144"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="56d61-145">DLL</span><span class="sxs-lookup"><span data-stu-id="56d61-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d61-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d61-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="56d61-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56d61-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56d61-148">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="56d61-148">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="56d61-149">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="56d61-149">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

