---
title: Метод Инапенфорцементклиентконнектион Жетконнектионид (Напенфорцементклиент. h)
description: Используется для получения уникального идентификатора соединения клиента.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- Метод Жетконнектионид NAP
- Метод Жетконнектионид NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетконнектионид
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137730"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="7477e-106">Метод Инапенфорцементклиентконнектион:: Жетконнектионид</span><span class="sxs-lookup"><span data-stu-id="7477e-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="7477e-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7477e-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7477e-108">Метод **инапенфорцементклиентконнектион:: жетконнектионид** используется для получения уникального идентификатора соединения клиента.</span><span class="sxs-lookup"><span data-stu-id="7477e-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="7477e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7477e-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="7477e-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7477e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7477e-111">*connectionId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="7477e-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7477e-112">Указатель на указатель на [**ConnectionId**](nap-datatypes.md) , однозначно определяющий это соединение.</span><span class="sxs-lookup"><span data-stu-id="7477e-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7477e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7477e-113">Return value</span></span>

<span data-ttu-id="7477e-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="7477e-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7477e-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7477e-115">Return code</span></span>                                                                                     | <span data-ttu-id="7477e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7477e-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7477e-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7477e-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7477e-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="7477e-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7477e-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7477e-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7477e-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7477e-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7477e-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7477e-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7477e-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7477e-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7477e-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7477e-123">Remarks</span></span>

<span data-ttu-id="7477e-124">Идентификатор соединения в основном используется в целях ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="7477e-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7477e-125">Требования</span><span class="sxs-lookup"><span data-stu-id="7477e-125">Requirements</span></span>



| <span data-ttu-id="7477e-126">Требование</span><span class="sxs-lookup"><span data-stu-id="7477e-126">Requirement</span></span> | <span data-ttu-id="7477e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="7477e-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7477e-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7477e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7477e-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7477e-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7477e-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7477e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7477e-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7477e-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7477e-132">Header</span><span class="sxs-lookup"><span data-stu-id="7477e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7477e-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7477e-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7477e-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7477e-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7477e-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7477e-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7477e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7477e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7477e-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7477e-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7477e-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7477e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7477e-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="7477e-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





