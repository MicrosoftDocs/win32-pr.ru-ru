---
title: Метод Инапенфорцементклиентконнектион Сетфлагс (Напенфорцементклиент. h)
description: Используется для различения ответов первого времени от ответов из-за кэширования Сохрекуестс с помощью триггеров. | Метод Инапенфорцементклиентконнектион Сетфлагс (Напенфорцементклиент. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Метод Сетфлагс NAP
- Метод Сетфлагс NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетфлагс
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105651473"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="acc76-107">Метод Инапенфорцементклиентконнектион:: Сетфлагс</span><span class="sxs-lookup"><span data-stu-id="acc76-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="acc76-108">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="acc76-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="acc76-109">Метод **инапенфорцементклиентконнектион:: сетфлагс** используется для различения ответов первого времени от ответов из-за того, что сохрекуестс кэшируется принудительно.</span><span class="sxs-lookup"><span data-stu-id="acc76-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="acc76-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acc76-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="acc76-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="acc76-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acc76-112">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acc76-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acc76-113">Флаги, определяющие, является ли [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) причиной кэширования **сохрекуест**.</span><span class="sxs-lookup"><span data-stu-id="acc76-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="acc76-114">Если *Флаги* имеют значение [**фрешсохрекуест**](nap-type-constants.md), это новый запрос; в противном случае это кэшированный запрос.</span><span class="sxs-lookup"><span data-stu-id="acc76-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acc76-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acc76-115">Return value</span></span>

<span data-ttu-id="acc76-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="acc76-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="acc76-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="acc76-117">Return code</span></span>                                                                                     | <span data-ttu-id="acc76-118">Описание</span><span class="sxs-lookup"><span data-stu-id="acc76-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="acc76-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="acc76-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="acc76-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="acc76-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="acc76-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="acc76-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="acc76-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="acc76-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="acc76-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="acc76-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="acc76-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="acc76-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="acc76-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acc76-125">Remarks</span></span>

<span data-ttu-id="acc76-126">Это значение задается параметром Напажент.</span><span class="sxs-lookup"><span data-stu-id="acc76-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="acc76-127">Требования</span><span class="sxs-lookup"><span data-stu-id="acc76-127">Requirements</span></span>



| <span data-ttu-id="acc76-128">Требование</span><span class="sxs-lookup"><span data-stu-id="acc76-128">Requirement</span></span> | <span data-ttu-id="acc76-129">Значение</span><span class="sxs-lookup"><span data-stu-id="acc76-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acc76-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acc76-130">Minimum supported client</span></span><br/> | <span data-ttu-id="acc76-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="acc76-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="acc76-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acc76-132">Minimum supported server</span></span><br/> | <span data-ttu-id="acc76-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="acc76-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="acc76-134">Header</span><span class="sxs-lookup"><span data-stu-id="acc76-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="acc76-135"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="acc76-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="acc76-136">IDL</span><span class="sxs-lookup"><span data-stu-id="acc76-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="acc76-137"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="acc76-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="acc76-138">DLL</span><span class="sxs-lookup"><span data-stu-id="acc76-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acc76-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acc76-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="acc76-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acc76-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acc76-141">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="acc76-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





