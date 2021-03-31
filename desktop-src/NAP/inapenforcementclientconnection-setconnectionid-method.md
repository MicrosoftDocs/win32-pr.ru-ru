---
title: Метод Инапенфорцементклиентконнектион Сетконнектионид (Напенфорцементклиент. h)
description: Используется для установки уникального идентификатора соединения и должен быть задан клиентом принудительного применения сразу после создания соединения.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- Метод Сетконнектионид NAP
- Метод Сетконнектионид NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетконнектионид
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988442"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="760a4-106">Метод Инапенфорцементклиентконнектион:: Сетконнектионид</span><span class="sxs-lookup"><span data-stu-id="760a4-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="760a4-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="760a4-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="760a4-108">Метод **инапенфорцементклиентконнектион:: сетконнектионид** используется для установки уникального идентификатора соединения и должен быть задан клиентом принудительного применения сразу после создания соединения.</span><span class="sxs-lookup"><span data-stu-id="760a4-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="760a4-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="760a4-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="760a4-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="760a4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="760a4-111">*connectionId* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="760a4-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="760a4-112">Указатель на [**ConnectionId**](nap-datatypes.md) , который однозначно определяет соединение.</span><span class="sxs-lookup"><span data-stu-id="760a4-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="760a4-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="760a4-113">Return value</span></span>

<span data-ttu-id="760a4-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="760a4-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="760a4-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="760a4-115">Return code</span></span>                                                                                     | <span data-ttu-id="760a4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="760a4-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="760a4-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="760a4-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="760a4-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="760a4-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="760a4-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="760a4-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="760a4-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="760a4-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="760a4-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="760a4-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="760a4-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="760a4-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="760a4-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="760a4-123">Remarks</span></span>

<span data-ttu-id="760a4-124">Этот ConnectionID в основном используется в целях ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="760a4-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="760a4-125">Требования</span><span class="sxs-lookup"><span data-stu-id="760a4-125">Requirements</span></span>



| <span data-ttu-id="760a4-126">Требование</span><span class="sxs-lookup"><span data-stu-id="760a4-126">Requirement</span></span> | <span data-ttu-id="760a4-127">Значение</span><span class="sxs-lookup"><span data-stu-id="760a4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="760a4-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="760a4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="760a4-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="760a4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="760a4-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="760a4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="760a4-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="760a4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="760a4-132">Header</span><span class="sxs-lookup"><span data-stu-id="760a4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="760a4-133"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="760a4-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="760a4-134">IDL</span><span class="sxs-lookup"><span data-stu-id="760a4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="760a4-135"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="760a4-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="760a4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="760a4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="760a4-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="760a4-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="760a4-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="760a4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="760a4-139">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="760a4-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





