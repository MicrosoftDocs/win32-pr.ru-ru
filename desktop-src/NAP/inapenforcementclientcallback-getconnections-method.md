---
title: Метод Инапенфорцементклиенткаллбаккных соединений (Напенфорцементклиент. h)
description: Вызывается Напажент и реализуется клиентом принудительного применения для возврата набора соединений.
ms.assetid: 8f697217-5799-48e4-9f0b-715f516e48d9
keywords:
- Метод соединений NAP
- Метод соединений NAP, интерфейс Инапенфорцементклиенткаллбакк
- Инапенфорцементклиенткаллбакк интерфейса NAP, метод соединений
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.GetConnections
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acdc68dbc69cabe710414f3fa2501585f3e384e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892706"
---
# <a name="inapenforcementclientcallbackgetconnections-method"></a><span data-ttu-id="c150e-106">Метод Инапенфорцементклиенткаллбакк:: соединений</span><span class="sxs-lookup"><span data-stu-id="c150e-106">INapEnforcementClientCallback::GetConnections method</span></span>

> [!Note]  
> <span data-ttu-id="c150e-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="c150e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c150e-108">Метод обратного вызова **инапенфорцементклиенткаллбакк::** noreturn вызывается напажент и реализуется клиентом принудительного применения для возврата набора соединений.</span><span class="sxs-lookup"><span data-stu-id="c150e-108">The **INapEnforcementClientCallback::GetConnections** callback method is called by the NapAgent and implemented by the enforcement client to return a set of connections.</span></span>

## <a name="syntax"></a><span data-ttu-id="c150e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c150e-109">Syntax</span></span>


```C++
HRESULT GetConnections(
  [out] Connections **connections
);
```



## <a name="parameters"></a><span data-ttu-id="c150e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="c150e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c150e-111">*подключения* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c150e-111">*connections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c150e-112">Указатель на текущий набор обслуживаемых [**соединений**](connections-struct.md).</span><span class="sxs-lookup"><span data-stu-id="c150e-112">A pointer to the current set of maintained [**Connections**](connections-struct.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c150e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c150e-113">Return value</span></span>

<span data-ttu-id="c150e-114">Этот метод обратного вызова должен возвращать один из следующих кодов ошибок.</span><span class="sxs-lookup"><span data-stu-id="c150e-114">This callback method must return one the following error codes.</span></span>



| <span data-ttu-id="c150e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c150e-115">Return code</span></span>                                                                                                | <span data-ttu-id="c150e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="c150e-116">Description</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c150e-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="c150e-117"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c150e-118">Верните это значение, если операция завершилась удачно.</span><span class="sxs-lookup"><span data-stu-id="c150e-118">Return this value if the operation succeeded.</span></span><br/>                                                                                                                                                              |
| <dl> <span data-ttu-id="c150e-119"><dt>**\_сервер RPC \_ S \_ недоступен**</dt></span><span class="sxs-lookup"><span data-stu-id="c150e-119"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="c150e-120">Возврат этого значения приводит к удалению принудительного применения из списка связанных-SHA и соответствующей записи кэша Напажент для записи на диск.</span><span class="sxs-lookup"><span data-stu-id="c150e-120">Returning this value causes the enforcer to be removed from the bound-SHA list, and the corresponding NapAgent cache entry to be flushed.</span></span> <span data-ttu-id="c150e-121">После этого сбой SHA может повторно инициализироваться с помощью Напажент.</span><span class="sxs-lookup"><span data-stu-id="c150e-121">The failing SHA can then re-initialize itself with the NapAgent.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c150e-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c150e-122">Requirements</span></span>



| <span data-ttu-id="c150e-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c150e-123">Requirement</span></span> | <span data-ttu-id="c150e-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c150e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c150e-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c150e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c150e-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c150e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c150e-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c150e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c150e-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c150e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c150e-129">Header</span><span class="sxs-lookup"><span data-stu-id="c150e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c150e-130"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="c150e-130"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="c150e-131">IDL</span><span class="sxs-lookup"><span data-stu-id="c150e-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c150e-132"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c150e-132"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c150e-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c150e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c150e-134">**инапенфорцементклиенткаллбакк**</span><span class="sxs-lookup"><span data-stu-id="c150e-134">**INapEnforcementClientCallback**</span></span>](inapenforcementclientcallback.md)
</dt> </dl>

 

 





