---
title: Метод Инапсистемхеалсвалидатионрекуест Жетстрингкоррелатионид (Напсистемхеалсвалидатор. h)
description: Используется средствами проверки работоспособности системы (SHV), которые должны записывать эти сведения в журнал.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Метод Жетстрингкоррелатионид NAP
- Метод Жетстрингкоррелатионид NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жетстрингкоррелатионид
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535525"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="70c7a-106">Метод Инапсистемхеалсвалидатионрекуест:: Жетстрингкоррелатионид</span><span class="sxs-lookup"><span data-stu-id="70c7a-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="70c7a-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="70c7a-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="70c7a-108">Метод **инапсистемхеалсвалидатионрекуест:: жетстрингкоррелатионид** используется средствами проверки работоспособности системы (SHV), которые должны записывать эти сведения в журнал.</span><span class="sxs-lookup"><span data-stu-id="70c7a-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="70c7a-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="70c7a-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="70c7a-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="70c7a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70c7a-111">*correlationId* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="70c7a-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70c7a-112">Указатель на указатель на уникальный [**стрингкоррелатионид**](nap-type-constants.md) для обмена SoH.</span><span class="sxs-lookup"><span data-stu-id="70c7a-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70c7a-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="70c7a-113">Return value</span></span>

<span data-ttu-id="70c7a-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="70c7a-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="70c7a-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="70c7a-115">Return code</span></span>                                                                                     | <span data-ttu-id="70c7a-116">Описание</span><span class="sxs-lookup"><span data-stu-id="70c7a-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="70c7a-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="70c7a-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="70c7a-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="70c7a-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="70c7a-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="70c7a-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="70c7a-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="70c7a-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="70c7a-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="70c7a-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="70c7a-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="70c7a-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="70c7a-123">Требования</span><span class="sxs-lookup"><span data-stu-id="70c7a-123">Requirements</span></span>



| <span data-ttu-id="70c7a-124">Требование</span><span class="sxs-lookup"><span data-stu-id="70c7a-124">Requirement</span></span> | <span data-ttu-id="70c7a-125">Значение</span><span class="sxs-lookup"><span data-stu-id="70c7a-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70c7a-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="70c7a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="70c7a-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="70c7a-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="70c7a-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="70c7a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="70c7a-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="70c7a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="70c7a-130">Header</span><span class="sxs-lookup"><span data-stu-id="70c7a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="70c7a-131"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="70c7a-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="70c7a-132">IDL</span><span class="sxs-lookup"><span data-stu-id="70c7a-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="70c7a-133"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="70c7a-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="70c7a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="70c7a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="70c7a-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="70c7a-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="70c7a-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="70c7a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70c7a-137">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="70c7a-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





