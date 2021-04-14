---
title: Метод Инапенфорцементклиентконнектион Жетстрингкоррелатионид (Напенфорцементклиент. h)
description: Возвращает строковую версию идентификатора, используемого для корреляции запросов и ответов.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Метод Жетстрингкоррелатионид NAP
- Метод Жетстрингкоррелатионид NAP, интерфейс Инапенфорцементклиентконнектион
- Инапенфорцементклиентконнектион интерфейса NAP, метод Жетстрингкоррелатионид
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533965"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="dc59a-106">Метод Инапенфорцементклиентконнектион:: Жетстрингкоррелатионид</span><span class="sxs-lookup"><span data-stu-id="dc59a-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="dc59a-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="dc59a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="dc59a-108">Метод **инапенфорцементклиентконнектион:: жетстрингкоррелатионид** Получает строковую версию идентификатора, используемого для корреляции запросов и ответов.</span><span class="sxs-lookup"><span data-stu-id="dc59a-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc59a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc59a-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="dc59a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="dc59a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc59a-111">*correlationId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="dc59a-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc59a-112">Указатель на структуру [**каунтедстринг**](/windows/win32/api/naptypes/ns-naptypes-countedstring) , которая содержит строковую версию [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)объекта Connection.</span><span class="sxs-lookup"><span data-stu-id="dc59a-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc59a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dc59a-113">Return value</span></span>

<span data-ttu-id="dc59a-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="dc59a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="dc59a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="dc59a-115">Return code</span></span>                                                                                     | <span data-ttu-id="dc59a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="dc59a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc59a-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="dc59a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="dc59a-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="dc59a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dc59a-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="dc59a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="dc59a-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="dc59a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="dc59a-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="dc59a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="dc59a-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dc59a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="dc59a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="dc59a-123">Requirements</span></span>



| <span data-ttu-id="dc59a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="dc59a-124">Requirement</span></span> | <span data-ttu-id="dc59a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="dc59a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc59a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dc59a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="dc59a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dc59a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dc59a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dc59a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="dc59a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dc59a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dc59a-130">Header</span><span class="sxs-lookup"><span data-stu-id="dc59a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc59a-131"><dt>Напенфорцементклиент. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc59a-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="dc59a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="dc59a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dc59a-133"><dt>Напенфорцементклиент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dc59a-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="dc59a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="dc59a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc59a-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc59a-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="dc59a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dc59a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc59a-137">**инапенфорцементклиентконнектион**</span><span class="sxs-lookup"><span data-stu-id="dc59a-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





