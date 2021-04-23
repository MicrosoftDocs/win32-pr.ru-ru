---
title: Метод Инапенфорцементклиентконнектион Сетприватедата (Напенфорцементклиент. h)
description: Используется Напажент для установки частных данных.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- Метод Сетприватедата NAP
- Метод Сетприватедата NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Сетприватедата
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071416"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="7c87b-106">Метод Инапенфорцементклиентконнектион:: Сетприватедата</span><span class="sxs-lookup"><span data-stu-id="7c87b-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="7c87b-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="7c87b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7c87b-108">Метод **инапенфорцементклиентконнектион:: сетприватедата** используется напажент для установки частных данных.</span><span class="sxs-lookup"><span data-stu-id="7c87b-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c87b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7c87b-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="7c87b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="7c87b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c87b-111">*privateData* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="7c87b-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c87b-112">Указатель на большой двоичный объект данных [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) , который может интерпретировать только напажент.</span><span class="sxs-lookup"><span data-stu-id="7c87b-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c87b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7c87b-113">Return value</span></span>

<span data-ttu-id="7c87b-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="7c87b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7c87b-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7c87b-115">Return code</span></span>                                                                                     | <span data-ttu-id="7c87b-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7c87b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c87b-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="7c87b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7c87b-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="7c87b-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7c87b-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7c87b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7c87b-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="7c87b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7c87b-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7c87b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7c87b-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7c87b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7c87b-123">Требования</span><span class="sxs-lookup"><span data-stu-id="7c87b-123">Requirements</span></span>



| <span data-ttu-id="7c87b-124">Требование</span><span class="sxs-lookup"><span data-stu-id="7c87b-124">Requirement</span></span> | <span data-ttu-id="7c87b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="7c87b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c87b-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c87b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="7c87b-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c87b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7c87b-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c87b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="7c87b-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7c87b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7c87b-130">Header</span><span class="sxs-lookup"><span data-stu-id="7c87b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c87b-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c87b-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c87b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="7c87b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7c87b-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7c87b-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7c87b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="7c87b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c87b-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c87b-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7c87b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c87b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c87b-137">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="7c87b-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





