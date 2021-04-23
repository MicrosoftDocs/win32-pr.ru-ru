---
title: Метод Инапенфорцементклиентконнектион Жетприватедата (Напенфорцементклиент. h)
description: Используется Напажент для получения закрытых данных.
ms.assetid: d38ef523-b645-401f-b3a9-1315ef39931a
keywords:
- Метод Жетприватедата NAP
- Метод Жетприватедата NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетприватедата
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6618ff7b25ad57cbb943107e80f299d9b6a68bea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891682"
---
# <a name="inapenforcementclientconnectiongetprivatedata-method"></a><span data-ttu-id="63581-106">Метод Инапенфорцементклиентконнектион:: Жетприватедата</span><span class="sxs-lookup"><span data-stu-id="63581-106">INapEnforcementClientConnection::GetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="63581-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="63581-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="63581-108">Метод **инапенфорцементклиентконнектион:: жетприватедата** используется напажент для получения закрытых данных.</span><span class="sxs-lookup"><span data-stu-id="63581-108">The **INapEnforcementClientConnection::GetPrivateData** method is used by the NapAgent to get private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="63581-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63581-109">Syntax</span></span>


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a><span data-ttu-id="63581-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="63581-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63581-111">*privateData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="63581-111">*privateData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63581-112">Указатель на указатель на BLOB-объект непрозрачных данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , который может интерпретировать только напажент.</span><span class="sxs-lookup"><span data-stu-id="63581-112">A pointer to a pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) opaque data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63581-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="63581-113">Return value</span></span>

<span data-ttu-id="63581-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="63581-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="63581-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="63581-115">Return code</span></span>                                                                                     | <span data-ttu-id="63581-116">Описание</span><span class="sxs-lookup"><span data-stu-id="63581-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="63581-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="63581-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="63581-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="63581-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="63581-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="63581-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="63581-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="63581-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="63581-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="63581-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="63581-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63581-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="63581-123">Требования</span><span class="sxs-lookup"><span data-stu-id="63581-123">Requirements</span></span>



| <span data-ttu-id="63581-124">Требование</span><span class="sxs-lookup"><span data-stu-id="63581-124">Requirement</span></span> | <span data-ttu-id="63581-125">Значение</span><span class="sxs-lookup"><span data-stu-id="63581-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63581-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63581-126">Minimum supported client</span></span><br/> | <span data-ttu-id="63581-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63581-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="63581-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63581-128">Minimum supported server</span></span><br/> | <span data-ttu-id="63581-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63581-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="63581-130">Header</span><span class="sxs-lookup"><span data-stu-id="63581-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="63581-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="63581-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="63581-132">IDL</span><span class="sxs-lookup"><span data-stu-id="63581-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="63581-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="63581-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="63581-134">DLL</span><span class="sxs-lookup"><span data-stu-id="63581-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63581-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63581-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="63581-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63581-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63581-137">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="63581-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





