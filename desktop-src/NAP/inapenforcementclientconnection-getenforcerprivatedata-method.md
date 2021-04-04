---
title: Метод Инапенфорцементклиентконнектион Жетенфорцерприватедата (Напенфорцементклиент. h)
description: Используется в принудительном применении для получения закрытых данных.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Метод Жетенфорцерприватедата NAP
- Метод Жетенфорцерприватедата NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетенфорцерприватедата
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d592ad0b11abf2b349b0810d67b05f2ee4086060
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137726"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a><span data-ttu-id="2b604-106">Метод Инапенфорцементклиентконнектион:: Жетенфорцерприватедата</span><span class="sxs-lookup"><span data-stu-id="2b604-106">INapEnforcementClientConnection::GetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="2b604-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="2b604-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2b604-108">Метод **инапенфорцементклиентконнектион:: жетенфорцерприватедата** используется средством применения для получения закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="2b604-108">The **INapEnforcementClientConnection::GetEnforcerPrivateData** method is used by the enforcer to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b604-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b604-109">Syntax</span></span>


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="2b604-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="2b604-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b604-111">*privateData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="2b604-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2b604-112">Указатель на указатель на большой двоичный объект непрозрачных данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , который может интерпретировать только данный объект.</span><span class="sxs-lookup"><span data-stu-id="2b604-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b604-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2b604-113">Return value</span></span>

<span data-ttu-id="2b604-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="2b604-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2b604-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="2b604-115">Return code</span></span>                                                                                     | <span data-ttu-id="2b604-116">Описание</span><span class="sxs-lookup"><span data-stu-id="2b604-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2b604-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="2b604-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2b604-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="2b604-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2b604-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="2b604-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2b604-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="2b604-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2b604-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2b604-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2b604-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2b604-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2b604-123">Требования</span><span class="sxs-lookup"><span data-stu-id="2b604-123">Requirements</span></span>



| <span data-ttu-id="2b604-124">Требование</span><span class="sxs-lookup"><span data-stu-id="2b604-124">Requirement</span></span> | <span data-ttu-id="2b604-125">Значение</span><span class="sxs-lookup"><span data-stu-id="2b604-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b604-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b604-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2b604-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b604-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2b604-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b604-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2b604-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b604-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2b604-130">Header</span><span class="sxs-lookup"><span data-stu-id="2b604-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b604-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b604-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="2b604-132">IDL</span><span class="sxs-lookup"><span data-stu-id="2b604-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2b604-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2b604-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="2b604-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2b604-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b604-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b604-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="2b604-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b604-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b604-137">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="2b604-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





