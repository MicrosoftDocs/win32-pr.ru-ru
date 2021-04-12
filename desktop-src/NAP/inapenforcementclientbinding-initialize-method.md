---
title: Метод Initialize Инапенфорцементклиентбиндинг (Напенфорцементклиент. h)
description: Автоматически запускает службу Напажент.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Инициализация метода NAP
- Инициализация метода NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489891"
---
# <a name="inapenforcementclientbindinginitialize-method"></a><span data-ttu-id="5d91a-106">Метод Инапенфорцементклиентбиндинг:: Initialize</span><span class="sxs-lookup"><span data-stu-id="5d91a-106">INapEnforcementClientBinding::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="5d91a-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="5d91a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5d91a-108">Метод **инапенфорцементклиентбиндинг:: Initialize** автоматически запускает службу напажент.</span><span class="sxs-lookup"><span data-stu-id="5d91a-108">The **INapEnforcementClientBinding::Initialize** method starts up the NapAgent service automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d91a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d91a-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a><span data-ttu-id="5d91a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5d91a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d91a-111">*идентификатор* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="5d91a-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d91a-112">Объект [**енфорцементентитид**](nap-datatypes.md) , определяющий клиента принудительного применения и его версию.</span><span class="sxs-lookup"><span data-stu-id="5d91a-112">An [**EnforcementEntityId**](nap-datatypes.md) that identifies the enforcement client and its version.</span></span>

</dd> <dt>

<span data-ttu-id="5d91a-113">*обратный вызов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5d91a-113">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d91a-114">COM-указатель на интерфейс [**инапенфорцементклиенткаллбакк**](inapenforcementclientcallback.md) , используемый напажент для обратного вызова клиентов принудительного применения с уведомлением/процессом.</span><span class="sxs-lookup"><span data-stu-id="5d91a-114">A COM pointer to an [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) interface used by the NapAgent to callback the enforcement clients with notify/process.</span></span> <span data-ttu-id="5d91a-115">Напажент содержит ссылку на объект, связанный с этим интерфейсом, пока не будет вызван метод [**инапенфорцементклиентбиндинг:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) .</span><span class="sxs-lookup"><span data-stu-id="5d91a-115">The NapAgent holds a reference to the object associated with this interface until [**INapEnforcementClientBinding::Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) is called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d91a-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5d91a-116">Return value</span></span>

<span data-ttu-id="5d91a-117">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="5d91a-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5d91a-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="5d91a-118">Return code</span></span>                                                                                                         | <span data-ttu-id="5d91a-119">Описание</span><span class="sxs-lookup"><span data-stu-id="5d91a-119">Description</span></span>                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5d91a-120"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-120"><dt>**S\_OK** </dt></span></span> </dl>                               | <span data-ttu-id="5d91a-121">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="5d91a-121">The operation is successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="5d91a-122"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>                     | <span data-ttu-id="5d91a-123">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="5d91a-123">Permissions error, access denied.</span></span><br/>                                             |
| <dl> <span data-ttu-id="5d91a-124"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>                      | <span data-ttu-id="5d91a-125">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d91a-125">System resource limit, could not perform the operation.</span></span><br/>                       |
| <dl> <span data-ttu-id="5d91a-126"><dt>**HRESULT (ошибка \_ уже \_ инициализирована)**</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-126"><dt>**HRESULT(ERROR\_ALREADY\_INITIALIZED)**</dt></span></span> </dl> | <span data-ttu-id="5d91a-127">Если этот параметр уже инициализирован ранее, возвращается этот код ошибки.</span><span class="sxs-lookup"><span data-stu-id="5d91a-127">If the enforcer has initialized previously, then this error code is returned.</span></span><br/> |
| <dl> <span data-ttu-id="5d91a-128"><dt>**Защита доступа к сети \_ E \_ не \_ зарегистрирована**</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-128"><dt>**NAP\_E\_NOT\_REGISTERED**</dt></span></span> </dl>              | <span data-ttu-id="5d91a-129">Если он не был зарегистрирован ранее, возвращается этот код ошибки.</span><span class="sxs-lookup"><span data-stu-id="5d91a-129">If the enforcer has not registered earlier, this error code is returned.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="5d91a-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5d91a-130">Remarks</span></span>

<span data-ttu-id="5d91a-131">Клиент принудительного применения должен вызвать метод **инапенфорцементклиентбиндинг:: Initialize** перед вызовом любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="5d91a-131">The enforcement client must call the **INapEnforcementClientBinding::Initialize** method before calling any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d91a-132">Требования</span><span class="sxs-lookup"><span data-stu-id="5d91a-132">Requirements</span></span>



| <span data-ttu-id="5d91a-133">Требование</span><span class="sxs-lookup"><span data-stu-id="5d91a-133">Requirement</span></span> | <span data-ttu-id="5d91a-134">Значение</span><span class="sxs-lookup"><span data-stu-id="5d91a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5d91a-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5d91a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5d91a-136">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5d91a-136">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5d91a-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5d91a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5d91a-138">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5d91a-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5d91a-139">Header</span><span class="sxs-lookup"><span data-stu-id="5d91a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d91a-140"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-140"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5d91a-141">IDL</span><span class="sxs-lookup"><span data-stu-id="5d91a-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5d91a-142"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-142"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5d91a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5d91a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d91a-144"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-144"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5d91a-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5d91a-145">See also</span></span>

<dl> <span data-ttu-id="5d91a-146"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5d91a-146"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="5d91a-147">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="5d91a-147">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="5d91a-148">**Инапенфорцементклиентбиндинг:: Uninitialize**</span><span class="sxs-lookup"><span data-stu-id="5d91a-148">**INapEnforcementClientBinding::Uninitialize**</span></span>](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





