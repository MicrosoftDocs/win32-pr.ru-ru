---
title: Метод Инапенфорцементклиентконнектион Жетмакссизе (Напенфорцементклиент. h)
description: Возвращает максимальный размер пакета SoH для этого клиента.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Метод Жетмакссизе NAP
- Метод Жетмакссизе NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетмакссизе
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801852"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="9c514-106">Метод Инапенфорцементклиентконнектион:: Жетмакссизе</span><span class="sxs-lookup"><span data-stu-id="9c514-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="9c514-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="9c514-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9c514-108">Метод **инапенфорцементклиентконнектион:: жетмакссизе** получает максимальный размер пакета SoH для этого клиента.</span><span class="sxs-lookup"><span data-stu-id="9c514-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c514-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c514-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="9c514-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c514-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c514-111">*MAXSIZE* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="9c514-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c514-112">Указатель на [**протоколмакссизе**](nap-datatypes.md) , указывающий максимальный размер пакета SoH в байтах.</span><span class="sxs-lookup"><span data-stu-id="9c514-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c514-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c514-113">Return value</span></span>

<span data-ttu-id="9c514-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="9c514-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9c514-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="9c514-115">Return code</span></span>                                                                                     | <span data-ttu-id="9c514-116">Описание</span><span class="sxs-lookup"><span data-stu-id="9c514-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9c514-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="9c514-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9c514-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="9c514-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9c514-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="9c514-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9c514-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="9c514-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9c514-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="9c514-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9c514-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c514-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9c514-123">Требования</span><span class="sxs-lookup"><span data-stu-id="9c514-123">Requirements</span></span>



| <span data-ttu-id="9c514-124">Требование</span><span class="sxs-lookup"><span data-stu-id="9c514-124">Requirement</span></span> | <span data-ttu-id="9c514-125">Значение</span><span class="sxs-lookup"><span data-stu-id="9c514-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c514-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c514-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9c514-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c514-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9c514-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c514-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9c514-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9c514-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9c514-130">Header</span><span class="sxs-lookup"><span data-stu-id="9c514-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c514-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c514-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9c514-132">IDL</span><span class="sxs-lookup"><span data-stu-id="9c514-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c514-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c514-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="9c514-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9c514-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c514-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c514-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="9c514-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c514-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c514-137">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="9c514-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





