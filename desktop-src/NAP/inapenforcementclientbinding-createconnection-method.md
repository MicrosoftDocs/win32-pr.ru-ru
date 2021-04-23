---
title: Метод Инапенфорцементклиентбиндинг CreateConnection (Напенфорцементклиент. h)
description: Используется принудительно триггерами для создания объектов подключения.
ms.assetid: 4d31928f-1a10-4168-a53c-256cbbf3e5c9
keywords:
- Метод CreateConnection NAP
- Метод CreateConnection NAP, интерфейс Инапенфорцементклиентбиндинг
- Инапенфорцементклиентбиндинг интерфейса NAP, метод CreateConnection
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.CreateConnection
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf530b9fefd0e5b361f4f86ef2421712c750be9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071420"
---
# <a name="inapenforcementclientbindingcreateconnection-method"></a><span data-ttu-id="ed7e9-106">Метод Инапенфорцементклиентбиндинг:: CreateConnection</span><span class="sxs-lookup"><span data-stu-id="ed7e9-106">INapEnforcementClientBinding::CreateConnection method</span></span>

> [!Note]  
> <span data-ttu-id="ed7e9-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="ed7e9-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ed7e9-108">Метод фабрики **инапенфорцементклиентбиндинг:: CreateConnection** используется принудительно для создания объектов подключения.</span><span class="sxs-lookup"><span data-stu-id="ed7e9-108">The **INapEnforcementClientBinding::CreateConnection** factory method is used by enforcers to create connection objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed7e9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ed7e9-109">Syntax</span></span>


```C++
HRESULT CreateConnection(
  [out] INapEnforcementClientConnection **connection
);
```



## <a name="parameters"></a><span data-ttu-id="ed7e9-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed7e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed7e9-111">*Подключение к* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ed7e9-111">*connection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed7e9-112">Указатель COM на новый интерфейс [**инапенфорцементклиентконнектион**](inapenforcementclientconnection.md) , возвращенный системой защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="ed7e9-112">A COM pointer to a new [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interface returned by the NAP system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed7e9-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed7e9-113">Return value</span></span>

<span data-ttu-id="ed7e9-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="ed7e9-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ed7e9-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ed7e9-115">Return code</span></span>                                                                                     | <span data-ttu-id="ed7e9-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ed7e9-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ed7e9-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ed7e9-118">Операция прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="ed7e9-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="ed7e9-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ed7e9-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="ed7e9-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ed7e9-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ed7e9-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ed7e9-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ed7e9-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed7e9-123">Remarks</span></span>

<span data-ttu-id="ed7e9-124">Клиент принудительного применения должен вызвать метод [**инапенфорцементклиентбиндинг:: Initialize**](inapenforcementclientbinding-initialize-method.md) перед вызовом этого или любого другого метода интерфейса [**инапенфорцементклиентбиндинг**](inapenforcementclientbinding.md) .</span><span class="sxs-lookup"><span data-stu-id="ed7e9-124">The enforcement client must call the [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) method before calling this or any other method of the [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed7e9-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ed7e9-125">Requirements</span></span>



| <span data-ttu-id="ed7e9-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ed7e9-126">Requirement</span></span> | <span data-ttu-id="ed7e9-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ed7e9-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed7e9-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed7e9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ed7e9-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed7e9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ed7e9-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed7e9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ed7e9-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed7e9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ed7e9-132">Header</span><span class="sxs-lookup"><span data-stu-id="ed7e9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed7e9-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="ed7e9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="ed7e9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ed7e9-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="ed7e9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ed7e9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed7e9-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="ed7e9-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ed7e9-138">See also</span></span>

<dl> <span data-ttu-id="ed7e9-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ed7e9-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="ed7e9-140">**инапенфорцементклиентбиндинг**</span><span class="sxs-lookup"><span data-stu-id="ed7e9-140">**INapEnforcementClientBinding**</span></span>](inapenforcementclientbinding.md)
</dt> <dt>

[<span data-ttu-id="ed7e9-141">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="ed7e9-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





