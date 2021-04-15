---
title: Метод Инапсистемхеалсвалидатионрекуест Сетсохреспонсе (Напсистемхеалсвалидатор. h)
description: Позволяет средствам проверки работоспособности системы (SHV) настроить отправку Сохреспонсе на клиентский компьютер, соответствующий агенту работоспособности системы (SHA).
ms.assetid: 250b90ac-ce8f-4771-9d20-84c491adfb2c
keywords:
- Метод Сетсохреспонсе NAP
- Метод Сетсохреспонсе NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Сетсохреспонсе
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.SetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b818218ef4f8601ecf4927f5e8b90f93e5386b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415929"
---
# <a name="inapsystemhealthvalidationrequestsetsohresponse-method"></a><span data-ttu-id="b3c90-106">Метод Инапсистемхеалсвалидатионрекуест:: Сетсохреспонсе</span><span class="sxs-lookup"><span data-stu-id="b3c90-106">INapSystemHealthValidationRequest::SetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="b3c90-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="b3c90-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b3c90-108">Метод **инапсистемхеалсвалидатионрекуест:: сетсохреспонсе** позволяет средствам проверки работоспособности системы (SHV) настроить отправку [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) в его аналог агента работоспособности системы (SHA) на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="b3c90-108">The **INapSystemHealthValidationRequest::SetSoHResponse** method allows System Health Validators (SHVs) to set the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) to be sent to its System Health Agent (SHA) counterpart on the client-side.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3c90-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b3c90-109">Syntax</span></span>


```C++
HRESULT SetSoHResponse(
  [in] const SoHResponse *sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="b3c90-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3c90-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3c90-111">*сохреспонсе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b3c90-111">*sohResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b3c90-112">Указатель на структуру [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="b3c90-112">A pointer to a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3c90-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3c90-113">Return value</span></span>

<span data-ttu-id="b3c90-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="b3c90-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b3c90-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="b3c90-115">Return code</span></span>                                                                                     | <span data-ttu-id="b3c90-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b3c90-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3c90-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c90-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b3c90-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="b3c90-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b3c90-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c90-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b3c90-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="b3c90-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b3c90-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b3c90-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b3c90-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b3c90-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b3c90-123">Требования</span><span class="sxs-lookup"><span data-stu-id="b3c90-123">Requirements</span></span>



| <span data-ttu-id="b3c90-124">Требование</span><span class="sxs-lookup"><span data-stu-id="b3c90-124">Requirement</span></span> | <span data-ttu-id="b3c90-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b3c90-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3c90-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3c90-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b3c90-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b3c90-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="b3c90-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3c90-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b3c90-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3c90-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b3c90-130">Header</span><span class="sxs-lookup"><span data-stu-id="b3c90-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3c90-131"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3c90-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="b3c90-132">IDL</span><span class="sxs-lookup"><span data-stu-id="b3c90-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b3c90-133"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b3c90-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="b3c90-134">DLL</span><span class="sxs-lookup"><span data-stu-id="b3c90-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b3c90-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3c90-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="b3c90-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3c90-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3c90-137">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="b3c90-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





