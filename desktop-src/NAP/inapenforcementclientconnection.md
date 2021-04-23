---
title: Интерфейс Инапенфорцементклиентконнектион (Напенфорцементклиент. h)
description: Разрешить управление клиентскими подключениями. | Интерфейс Инапенфорцементклиентконнектион (Напенфорцементклиент. h)
ms.assetid: 96b94995-24b8-47ed-880e-6182d1bfe925
keywords:
- Инапенфорцементклиентконнектион интерфейса NAP
- Инапенфорцементклиентконнектион интерфейс NAP, описание
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5f132da021e7970ec2f15a872091c101cd5c42
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273448"
---
# <a name="inapenforcementclientconnection-interface"></a><span data-ttu-id="3a394-106">Интерфейс Инапенфорцементклиентконнектион</span><span class="sxs-lookup"><span data-stu-id="3a394-106">INapEnforcementClientConnection interface</span></span>

> [!Note]  
> <span data-ttu-id="3a394-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="3a394-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3a394-108">**Инапенфорцементклиентконнектион** предоставляет методы, позволяющие управлять подключениями клиентов.</span><span class="sxs-lookup"><span data-stu-id="3a394-108">The **INapEnforcementClientConnection** provides methods that allow for client connection management.</span></span>

> [!Note]  
> <span data-ttu-id="3a394-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) наследует все методы этого интерфейса, и вместо него следует использовать.</span><span class="sxs-lookup"><span data-stu-id="3a394-109">[**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md) inherits all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="3a394-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="3a394-110">Members</span></span>

<span data-ttu-id="3a394-111">Интерфейс **инапенфорцементклиентконнектион** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="3a394-111">The **INapEnforcementClientConnection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="3a394-112">**Инапенфорцементклиентконнектион** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3a394-112">**INapEnforcementClientConnection** also has these types of members:</span></span>

-   [<span data-ttu-id="3a394-113">Методы</span><span class="sxs-lookup"><span data-stu-id="3a394-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3a394-114">Методы</span><span class="sxs-lookup"><span data-stu-id="3a394-114">Methods</span></span>

<span data-ttu-id="3a394-115">Интерфейс **инапенфорцементклиентконнектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="3a394-115">The **INapEnforcementClientConnection** interface has these methods.</span></span>



| <span data-ttu-id="3a394-116">Метод</span><span class="sxs-lookup"><span data-stu-id="3a394-116">Method</span></span>                                                                                                                           | <span data-ttu-id="3a394-117">Описание</span><span class="sxs-lookup"><span data-stu-id="3a394-117">Description</span></span>                                                                                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3a394-118">**Инапенфорцементклиентконнектион:: Жетконнектионид**</span><span class="sxs-lookup"><span data-stu-id="3a394-118">**INapEnforcementClientConnection::GetConnectionId**</span></span>](inapenforcementclientconnection-getconnectionid-method.md)               | <span data-ttu-id="3a394-119">Возвращает идентификатор соединения клиента.</span><span class="sxs-lookup"><span data-stu-id="3a394-119">Gets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3a394-120">**Инапенфорцементклиентконнектион:: Жеткоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="3a394-120">**INapEnforcementClientConnection::GetCorrelationId**</span></span>](inapenforcementclientconnection-getcorrelationid-method.md)             | <span data-ttu-id="3a394-121">Возвращает идентификатор, используемый для корреляции запросов SoH и состояний работоспособности.</span><span class="sxs-lookup"><span data-stu-id="3a394-121">Gets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="3a394-122">**Инапенфорцементклиентконнектион:: Жетенфорцерприватедата**</span><span class="sxs-lookup"><span data-stu-id="3a394-122">**INapEnforcementClientConnection::GetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-getenforcerprivatedata-method.md) | <span data-ttu-id="3a394-123">Используется средством применения для получения закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="3a394-123">Used by the enforcer to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3a394-124">**Флаги Инапенфорцементклиентконнектион:: "**</span><span class="sxs-lookup"><span data-stu-id="3a394-124">**INapEnforcementClientConnection::GetFlags**</span></span>](inapenforcementclientconnection-getflags-method.md)                             | <span data-ttu-id="3a394-125">Возвращает значение флага, которое отличает ответы первого времени от ответов, из-за кэширования Сохрекуестс с помощью триггеров.</span><span class="sxs-lookup"><span data-stu-id="3a394-125">Gets the value of the flag that differentiates first-time responses from responses due to SoHRequests cached by the enforcers.</span></span><br/> |
| [<span data-ttu-id="3a394-126">**Инапенфорцементклиентконнектион:: Жетисолатионинфо**</span><span class="sxs-lookup"><span data-stu-id="3a394-126">**INapEnforcementClientConnection::GetIsolationInfo**</span></span>](inapenforcementclientconnection-getisolationinfo-method.md)             | <span data-ttu-id="3a394-127">Используется для получения сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="3a394-127">Used get the isolation information of the client.</span></span><br/>                                                                              |
| [<span data-ttu-id="3a394-128">**Инапенфорцементклиентконнектион:: Жетмакссизе**</span><span class="sxs-lookup"><span data-stu-id="3a394-128">**INapEnforcementClientConnection::GetMaxSize**</span></span>](inapenforcementclientconnection-getmaxsize-method.md)                         | <span data-ttu-id="3a394-129">Возвращает максимальный размер пакета SoH для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3a394-129">Gets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="3a394-130">**Инапенфорцементклиентконнектион:: Жетприватедата**</span><span class="sxs-lookup"><span data-stu-id="3a394-130">**INapEnforcementClientConnection::GetPrivateData**</span></span>](inapenforcementclientconnection-getprivatedata-method.md)                 | <span data-ttu-id="3a394-131">Используется Напажент для получения закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="3a394-131">Used by the NapAgent to get private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3a394-132">**Инапенфорцементклиентконнектион:: Жетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="3a394-132">**INapEnforcementClientConnection::GetSoHRequest**</span></span>](inapenforcementclientconnection-getsohrequest-method.md)                   | <span data-ttu-id="3a394-133">Возвращает запрос SoH.</span><span class="sxs-lookup"><span data-stu-id="3a394-133">Gets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="3a394-134">**Инапенфорцементклиентконнектион:: Жетсохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="3a394-134">**INapEnforcementClientConnection::GetSoHResponse**</span></span>](inapenforcementclientconnection-getsohresponse-method.md)                 | <span data-ttu-id="3a394-135">Возвращает SoH-Response, полученную клиентом принудительного применения.</span><span class="sxs-lookup"><span data-stu-id="3a394-135">Gets the SoH-Response received by the enforcement client.</span></span><br/>                                                                      |
| [<span data-ttu-id="3a394-136">**Инапенфорцементклиентконнектион:: Жетстрингкоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="3a394-136">**INapEnforcementClientConnection::GetStringCorrelationId**</span></span>](inapenforcementclientconnection-getstringcorrelationid-method.md) | <span data-ttu-id="3a394-137">Возвращает строку версии CorrelationId.</span><span class="sxs-lookup"><span data-stu-id="3a394-137">Gets the string version of the CorrelationId.</span></span> <span data-ttu-id="3a394-138">Используется в основном для ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="3a394-138">Used primarily for logging purposes.</span></span><br/>                                             |
| [<span data-ttu-id="3a394-139">**Инапенфорцементклиентконнектион:: Initialize**</span><span class="sxs-lookup"><span data-stu-id="3a394-139">**INapEnforcementClientConnection::Initialize**</span></span>](inapenforcementclientconnection-initialize-method.md)                         | <span data-ttu-id="3a394-140">Инициализирует подключение.</span><span class="sxs-lookup"><span data-stu-id="3a394-140">Initializes the connection.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="3a394-141">**Инапенфорцементклиентконнектион:: Сетконнектионид**</span><span class="sxs-lookup"><span data-stu-id="3a394-141">**INapEnforcementClientConnection::SetConnectionId**</span></span>](inapenforcementclientconnection-setconnectionid-method.md)               | <span data-ttu-id="3a394-142">Задает идентификатор соединения клиента.</span><span class="sxs-lookup"><span data-stu-id="3a394-142">Sets the connection ID of the client.</span></span><br/>                                                                                          |
| [<span data-ttu-id="3a394-143">**Инапенфорцементклиентконнектион:: Сеткоррелатионид**</span><span class="sxs-lookup"><span data-stu-id="3a394-143">**INapEnforcementClientConnection::SetCorrelationId**</span></span>](inapenforcementclientconnection-setcorrelationid-method.md)             | <span data-ttu-id="3a394-144">Задает идентификатор, используемый для корреляции запросов SoH и ответов о состоянии работоспособности.</span><span class="sxs-lookup"><span data-stu-id="3a394-144">Sets the ID used to correlate SoH-requests and SoH-responses.</span></span><br/>                                                                  |
| [<span data-ttu-id="3a394-145">**Инапенфорцементклиентконнектион:: Сетенфорцерприватедата**</span><span class="sxs-lookup"><span data-stu-id="3a394-145">**INapEnforcementClientConnection::SetEnforcerPrivateData**</span></span>](inapenforcementclientconnection-setenforcerprivatedata-method.md) | <span data-ttu-id="3a394-146">Используется в принудительном применении для установки закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="3a394-146">Used by the enforcer to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3a394-147">**Инапенфорцементклиентконнектион:: Сетфлагс**</span><span class="sxs-lookup"><span data-stu-id="3a394-147">**INapEnforcementClientConnection::SetFlags**</span></span>](inapenforcementclientconnection-setflags-method.md)                             | <span data-ttu-id="3a394-148">Устанавливает флаг, который отличает отклики первого времени от ответов из-за того, что Сохрекуестс кэшируется принудительно.</span><span class="sxs-lookup"><span data-stu-id="3a394-148">Sets the flag that differentiates first-time responses from responses due to SoHRequests cached by enforcers.</span></span><br/>                  |
| [<span data-ttu-id="3a394-149">**Инапенфорцементклиентконнектион:: Сетисолатионинфо**</span><span class="sxs-lookup"><span data-stu-id="3a394-149">**INapEnforcementClientConnection::SetIsolationInfo**</span></span>](inapenforcementclientconnection-setisolationinfo-method.md)             | <span data-ttu-id="3a394-150">Используется Напажент для установки сведений о изоляции клиента.</span><span class="sxs-lookup"><span data-stu-id="3a394-150">Used by the NapAgent to set the isolation information of the client.</span></span><br/>                                                           |
| [<span data-ttu-id="3a394-151">**Инапенфорцементклиентконнектион:: Сетмакссизе**</span><span class="sxs-lookup"><span data-stu-id="3a394-151">**INapEnforcementClientConnection::SetMaxSize**</span></span>](inapenforcementclientconnection-setmaxsize-method.md)                         | <span data-ttu-id="3a394-152">Задает максимальный размер пакета SoH для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="3a394-152">Sets the maximum size of the SoH packet for this client.</span></span><br/>                                                                       |
| [<span data-ttu-id="3a394-153">**Инапенфорцементклиентконнектион:: Сетприватедата**</span><span class="sxs-lookup"><span data-stu-id="3a394-153">**INapEnforcementClientConnection::SetPrivateData**</span></span>](inapenforcementclientconnection-setprivatedata-method.md)                 | <span data-ttu-id="3a394-154">Используется Напажент для установки частных данных.</span><span class="sxs-lookup"><span data-stu-id="3a394-154">Used by the NapAgent to set private data.</span></span><br/>                                                                                      |
| [<span data-ttu-id="3a394-155">**Инапенфорцементклиентконнектион:: Сетсохрекуест**</span><span class="sxs-lookup"><span data-stu-id="3a394-155">**INapEnforcementClientConnection::SetSoHRequest**</span></span>](inapenforcementclientconnection-setsohrequest-method.md)                   | <span data-ttu-id="3a394-156">Задает запрос SoH.</span><span class="sxs-lookup"><span data-stu-id="3a394-156">Sets the SoH Request.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="3a394-157">**Инапенфорцементклиентконнектион:: Сетсохреспонсе**</span><span class="sxs-lookup"><span data-stu-id="3a394-157">**INapEnforcementClientConnection::SetSoHResponse**</span></span>](inapenforcementclientconnection-setsohresponse-method.md)                 | <span data-ttu-id="3a394-158">Задает SoH-Response и используется клиентом принудительного применения при получении пакета.</span><span class="sxs-lookup"><span data-stu-id="3a394-158">Sets the SoH-Response and is used by the enforcement client on receiving a packet.</span></span><br/>                                             |



 

## <a name="requirements"></a><span data-ttu-id="3a394-159">Требования</span><span class="sxs-lookup"><span data-stu-id="3a394-159">Requirements</span></span>



| <span data-ttu-id="3a394-160">Требование</span><span class="sxs-lookup"><span data-stu-id="3a394-160">Requirement</span></span> | <span data-ttu-id="3a394-161">Значение</span><span class="sxs-lookup"><span data-stu-id="3a394-161">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a394-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3a394-162">Minimum supported client</span></span><br/> | <span data-ttu-id="3a394-163">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3a394-163">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3a394-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3a394-164">Minimum supported server</span></span><br/> | <span data-ttu-id="3a394-165">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3a394-165">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3a394-166">Header</span><span class="sxs-lookup"><span data-stu-id="3a394-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a394-167"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a394-167"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3a394-168">IDL</span><span class="sxs-lookup"><span data-stu-id="3a394-168">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3a394-169"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3a394-169"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3a394-170">DLL</span><span class="sxs-lookup"><span data-stu-id="3a394-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a394-171"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a394-171"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3a394-172">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a394-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a394-173">Интерфейсы NAP</span><span class="sxs-lookup"><span data-stu-id="3a394-173">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="3a394-174">Справочник по NAP</span><span class="sxs-lookup"><span data-stu-id="3a394-174">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

