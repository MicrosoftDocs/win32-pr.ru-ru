---
title: Метод Инапсистемхеалсажентрекуест Жетстрингкоррелатионид (Напсистемхеалсажент. h)
description: Используется агентами работоспособности системы для регистрации идентификатора корреляции.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- Метод Жетстрингкоррелатионид NAP
- Метод Жетстрингкоррелатионид NAP, интерфейс Инапсистемхеалсажентрекуест
- Инапсистемхеалсажентрекуест интерфейса NAP, метод Жетстрингкоррелатионид
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801829"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a><span data-ttu-id="4591a-106">Метод Инапсистемхеалсажентрекуест:: Жетстрингкоррелатионид</span><span class="sxs-lookup"><span data-stu-id="4591a-106">INapSystemHealthAgentRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="4591a-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="4591a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4591a-108">Метод **инапсистемхеалсажентрекуест:: жетстрингкоррелатионид** используется агентами работоспособности системы для записи идентификатора корреляции.</span><span class="sxs-lookup"><span data-stu-id="4591a-108">The **INapSystemHealthAgentRequest::GetStringCorrelationId** method is used by system health agents to log the correlation ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="4591a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4591a-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="4591a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4591a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4591a-111">*correlationId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="4591a-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4591a-112">Указатель на указатель на уникальный идентификатор [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) для этого обмена состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="4591a-112">A pointer to a pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4591a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4591a-113">Return value</span></span>

<span data-ttu-id="4591a-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="4591a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="4591a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4591a-115">Return code</span></span>                                                                                     | <span data-ttu-id="4591a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="4591a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="4591a-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="4591a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="4591a-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="4591a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="4591a-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="4591a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="4591a-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="4591a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="4591a-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="4591a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="4591a-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4591a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4591a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="4591a-123">Requirements</span></span>



| <span data-ttu-id="4591a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="4591a-124">Requirement</span></span> | <span data-ttu-id="4591a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="4591a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4591a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4591a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4591a-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4591a-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4591a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4591a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4591a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4591a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4591a-130">Header</span><span class="sxs-lookup"><span data-stu-id="4591a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4591a-131"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="4591a-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="4591a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="4591a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4591a-133"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4591a-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="4591a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4591a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4591a-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4591a-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="4591a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4591a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4591a-137">**инапсистемхеалсажентрекуест**</span><span class="sxs-lookup"><span data-stu-id="4591a-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





