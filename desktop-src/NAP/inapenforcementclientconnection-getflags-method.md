---
title: Метод Инапенфорцементклиентконнектион-Flags (Напенфорцементклиент. h)
description: Используется для различения ответов первого времени от ответов из-за кэширования Сохрекуестс с помощью триггеров. | Метод Инапенфорцементклиентконнектион-Flags (Напенфорцементклиент. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Методических флагов NAP
- Метод "Инапенфорцементклиентконнектион", интерфейс защиты доступа к сети
- Инапенфорцементклиентконнектион интерфейса NAP, метод «, помечающие»
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105651266"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="b4679-107">Метод Инапенфорцементклиентконнектион::</span><span class="sxs-lookup"><span data-stu-id="b4679-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="b4679-108">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b4679-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b4679-109">Метод **инапенфорцементклиентконнектион::** сохрекуестс используется для различения ответов первого времени от ответов из-за, кэшируемых с помощью триггеров.</span><span class="sxs-lookup"><span data-stu-id="b4679-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4679-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4679-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="b4679-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="b4679-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4679-112">*Флаги* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b4679-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4679-113">Указатель на флаг, определяющий, является ли [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) из-за кэшированного **сохрекуест**.</span><span class="sxs-lookup"><span data-stu-id="b4679-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="b4679-114">Если *Флаги* имеют значение [**фрешсохрекуест**](nap-type-constants.md), это новый запрос; в противном случае это кэшированный запрос.</span><span class="sxs-lookup"><span data-stu-id="b4679-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4679-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b4679-115">Return value</span></span>

<span data-ttu-id="b4679-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="b4679-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b4679-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b4679-117">Return code</span></span>                                                                                     | <span data-ttu-id="b4679-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b4679-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b4679-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b4679-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b4679-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="b4679-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b4679-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b4679-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b4679-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b4679-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b4679-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b4679-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b4679-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b4679-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b4679-125">Требования</span><span class="sxs-lookup"><span data-stu-id="b4679-125">Requirements</span></span>



| <span data-ttu-id="b4679-126">Требование</span><span class="sxs-lookup"><span data-stu-id="b4679-126">Requirement</span></span> | <span data-ttu-id="b4679-127">Значение</span><span class="sxs-lookup"><span data-stu-id="b4679-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4679-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4679-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b4679-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4679-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b4679-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4679-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b4679-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4679-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b4679-132">Header</span><span class="sxs-lookup"><span data-stu-id="b4679-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4679-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4679-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4679-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b4679-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4679-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4679-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b4679-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b4679-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4679-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4679-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b4679-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4679-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4679-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="b4679-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





