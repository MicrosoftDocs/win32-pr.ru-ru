---
title: Метод Инапсистемхеалсвалидатионрекуест Жеткоррелатионид (Напсистемхеалсвалидатор. h)
description: Используется средствами проверки работоспособности системы (SHV) для получения идентификатора корреляции. Затем SHV должен зарегистрировать эту информацию.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Метод Жеткоррелатионид NAP
- Метод Жеткоррелатионид NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жеткоррелатионид
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490359"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="96882-107">Метод Инапсистемхеалсвалидатионрекуест:: Жеткоррелатионид</span><span class="sxs-lookup"><span data-stu-id="96882-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="96882-108">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="96882-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="96882-109">Метод **инапсистемхеалсвалидатионрекуест:: жеткоррелатионид** используется средствами проверки работоспособности системы (SHV) для получения идентификатора корреляции.</span><span class="sxs-lookup"><span data-stu-id="96882-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="96882-110">Затем SHV должен зарегистрировать эту информацию.</span><span class="sxs-lookup"><span data-stu-id="96882-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="96882-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96882-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="96882-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="96882-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96882-113">*correlationId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="96882-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96882-114">Указатель на уникальный идентификатор [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) для обмена SoH.</span><span class="sxs-lookup"><span data-stu-id="96882-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96882-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="96882-115">Return value</span></span>

<span data-ttu-id="96882-116">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="96882-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="96882-117">Код возврата</span><span class="sxs-lookup"><span data-stu-id="96882-117">Return code</span></span>                                                                                     | <span data-ttu-id="96882-118">Описание</span><span class="sxs-lookup"><span data-stu-id="96882-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="96882-119"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="96882-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="96882-120">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="96882-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="96882-121"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="96882-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="96882-122">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="96882-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="96882-123"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="96882-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="96882-124">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="96882-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96882-125">Требования</span><span class="sxs-lookup"><span data-stu-id="96882-125">Requirements</span></span>



| <span data-ttu-id="96882-126">Требование</span><span class="sxs-lookup"><span data-stu-id="96882-126">Requirement</span></span> | <span data-ttu-id="96882-127">Значение</span><span class="sxs-lookup"><span data-stu-id="96882-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96882-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96882-128">Minimum supported client</span></span><br/> | <span data-ttu-id="96882-129">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="96882-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="96882-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96882-130">Minimum supported server</span></span><br/> | <span data-ttu-id="96882-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96882-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="96882-132">Header</span><span class="sxs-lookup"><span data-stu-id="96882-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="96882-133"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="96882-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="96882-134">IDL</span><span class="sxs-lookup"><span data-stu-id="96882-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="96882-135"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="96882-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="96882-136">DLL</span><span class="sxs-lookup"><span data-stu-id="96882-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="96882-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96882-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="96882-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96882-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96882-139">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="96882-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





