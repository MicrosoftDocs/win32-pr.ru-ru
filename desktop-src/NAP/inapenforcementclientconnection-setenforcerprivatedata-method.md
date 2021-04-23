---
title: Метод Инапенфорцементклиентконнектион Сетенфорцерприватедата (Напенфорцементклиент. h)
description: Используется в принудительном применении для установки закрытых данных.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Метод Сетенфорцерприватедата NAP
- Метод Сетенфорцерприватедата NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетенфорцерприватедата
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5773294e229a59ff07db8ef546d9d691b369b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071418"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a><span data-ttu-id="6421d-106">Метод Инапенфорцементклиентконнектион:: Сетенфорцерприватедата</span><span class="sxs-lookup"><span data-stu-id="6421d-106">INapEnforcementClientConnection::SetEnforcerPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="6421d-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="6421d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6421d-108">Метод **инапенфорцементклиентконнектион:: сетенфорцерприватедата** используется средством применения для установки закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="6421d-108">The **INapEnforcementClientConnection::SetEnforcerPrivateData** method is used by the enforcer to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6421d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6421d-109">Syntax</span></span>


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="6421d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="6421d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6421d-111">*privateData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6421d-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6421d-112">Указатель на большой двоичный объект непрозрачных данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , который может интерпретировать только этот обработчик.</span><span class="sxs-lookup"><span data-stu-id="6421d-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the enforcer can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6421d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6421d-113">Return value</span></span>

<span data-ttu-id="6421d-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="6421d-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6421d-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="6421d-115">Return code</span></span>                                                                                     | <span data-ttu-id="6421d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="6421d-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6421d-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6421d-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="6421d-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6421d-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6421d-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="6421d-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6421d-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6421d-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6421d-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6421d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="6421d-123">Requirements</span></span>



| <span data-ttu-id="6421d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="6421d-124">Requirement</span></span> | <span data-ttu-id="6421d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="6421d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6421d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6421d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="6421d-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6421d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6421d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6421d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="6421d-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6421d-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6421d-130">Header</span><span class="sxs-lookup"><span data-stu-id="6421d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6421d-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="6421d-132">IDL</span><span class="sxs-lookup"><span data-stu-id="6421d-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6421d-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="6421d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6421d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6421d-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6421d-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="6421d-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6421d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6421d-137">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="6421d-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





