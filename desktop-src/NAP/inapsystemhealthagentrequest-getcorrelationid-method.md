---
title: Метод Инапсистемхеалсажентрекуест Жеткоррелатионид (Напсистемхеалсажент. h)
description: Используется агентами работоспособности системы для согласования ответов о состоянии работоспособности и состояния работоспособности.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Метод Жеткоррелатионид NAP
- Метод Жеткоррелатионид NAP, интерфейс Инапсистемхеалсажентрекуест
- Инапсистемхеалсажентрекуест интерфейса NAP, метод Жеткоррелатионид
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535603"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a><span data-ttu-id="f7b21-106">Метод Инапсистемхеалсажентрекуест:: Жеткоррелатионид</span><span class="sxs-lookup"><span data-stu-id="f7b21-106">INapSystemHealthAgentRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="f7b21-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="f7b21-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f7b21-108">Метод **инапсистемхеалсажентрекуест:: жеткоррелатионид** используется агентами работоспособности системы для согласования ответов о состоянии работоспособности и состояния работоспособности.</span><span class="sxs-lookup"><span data-stu-id="f7b21-108">The **INapSystemHealthAgentRequest::GetCorrelationId** method is used by system health agents to correlate SoH's and SoH-Responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7b21-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7b21-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="f7b21-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f7b21-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7b21-111">*correlationId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="f7b21-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7b21-112">Указатель на уникальный идентификатор [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) для обмена SoH.</span><span class="sxs-lookup"><span data-stu-id="f7b21-112">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7b21-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f7b21-113">Return value</span></span>

<span data-ttu-id="f7b21-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="f7b21-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="f7b21-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f7b21-115">Return code</span></span>                                                                                     | <span data-ttu-id="f7b21-116">Описание</span><span class="sxs-lookup"><span data-stu-id="f7b21-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f7b21-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b21-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f7b21-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="f7b21-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f7b21-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b21-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f7b21-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="f7b21-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f7b21-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f7b21-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f7b21-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7b21-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f7b21-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f7b21-123">Requirements</span></span>



| <span data-ttu-id="f7b21-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f7b21-124">Requirement</span></span> | <span data-ttu-id="f7b21-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f7b21-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b21-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f7b21-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f7b21-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f7b21-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f7b21-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f7b21-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f7b21-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f7b21-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f7b21-130">Header</span><span class="sxs-lookup"><span data-stu-id="f7b21-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7b21-131"><dt>Напсистемхеалсажент. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7b21-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="f7b21-132">IDL</span><span class="sxs-lookup"><span data-stu-id="f7b21-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7b21-133"><dt>Напсистемхеалсажент. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7b21-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7b21-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f7b21-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7b21-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7b21-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="f7b21-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f7b21-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7b21-137">**инапсистемхеалсажентрекуест**</span><span class="sxs-lookup"><span data-stu-id="f7b21-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





