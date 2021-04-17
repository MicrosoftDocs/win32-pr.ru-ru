---
title: Метод Инапсистемхеалсвалидатионрекуест Жетсохреспонсе (Напсистемхеалсвалидатор. h)
description: Извлекает Сохреспонсе.
ms.assetid: 7db9d134-5cd4-4a6c-8576-843b9a920864
keywords:
- Метод Жетсохреспонсе NAP
- Метод Жетсохреспонсе NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жетсохреспонсе
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHResponse
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10174edc2bcb9df8e61c98305e42633d2b984b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672853"
---
# <a name="inapsystemhealthvalidationrequestgetsohresponse-method"></a><span data-ttu-id="43886-106">Метод Инапсистемхеалсвалидатионрекуест:: Жетсохреспонсе</span><span class="sxs-lookup"><span data-stu-id="43886-106">INapSystemHealthValidationRequest::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="43886-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="43886-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="43886-108">Метод **инапсистемхеалсвалидатионрекуест:: жетсохреспонсе** извлекает [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="43886-108">The **INapSystemHealthValidationRequest::GetSoHResponse** method retrieves the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

## <a name="syntax"></a><span data-ttu-id="43886-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43886-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] SoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="43886-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="43886-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43886-111">*сохреспонсе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43886-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43886-112">Указатель на указатель на полученный [**сохреспонсе**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="43886-112">A pointer to a pointer to the received [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43886-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43886-113">Return value</span></span>

<span data-ttu-id="43886-114">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="43886-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="43886-115">Код возврата</span><span class="sxs-lookup"><span data-stu-id="43886-115">Return code</span></span>                                                                                     | <span data-ttu-id="43886-116">Описание</span><span class="sxs-lookup"><span data-stu-id="43886-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="43886-117"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="43886-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="43886-118">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="43886-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="43886-119"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="43886-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="43886-120">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="43886-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="43886-121"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="43886-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="43886-122">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43886-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="43886-123">Требования</span><span class="sxs-lookup"><span data-stu-id="43886-123">Requirements</span></span>



| <span data-ttu-id="43886-124">Требование</span><span class="sxs-lookup"><span data-stu-id="43886-124">Requirement</span></span> | <span data-ttu-id="43886-125">Значение</span><span class="sxs-lookup"><span data-stu-id="43886-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43886-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43886-126">Minimum supported client</span></span><br/> | <span data-ttu-id="43886-127">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="43886-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="43886-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43886-128">Minimum supported server</span></span><br/> | <span data-ttu-id="43886-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43886-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43886-130">Header</span><span class="sxs-lookup"><span data-stu-id="43886-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="43886-131"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="43886-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="43886-132">IDL</span><span class="sxs-lookup"><span data-stu-id="43886-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="43886-133"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="43886-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="43886-134">DLL</span><span class="sxs-lookup"><span data-stu-id="43886-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43886-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43886-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="43886-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43886-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43886-137">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="43886-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





