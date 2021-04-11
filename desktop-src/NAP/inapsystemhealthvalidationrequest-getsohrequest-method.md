---
title: Метод Инапсистемхеалсвалидатионрекуест Жетсохрекуест (Напсистемхеалсвалидатор. h)
description: Позволяет средствам проверки работоспособности системы (SHV) получать и проверять сведения о Сохрекуест, отправленные их аналогами агента работоспособности системы (SHA) на клиенте.
ms.assetid: e06e07c6-7305-4171-b94e-19c360e94c67
keywords:
- Метод Жетсохрекуест NAP
- Метод Жетсохрекуест NAP, интерфейс Инапсистемхеалсвалидатионрекуест
- Инапсистемхеалсвалидатионрекуест интерфейса NAP, метод Жетсохрекуест
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetSoHRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306c9307f99f91e0b0a48a1c5ffeaf19b4ea1f12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137723"
---
# <a name="inapsystemhealthvalidationrequestgetsohrequest-method"></a><span data-ttu-id="54bf0-106">Метод Инапсистемхеалсвалидатионрекуест:: Жетсохрекуест</span><span class="sxs-lookup"><span data-stu-id="54bf0-106">INapSystemHealthValidationRequest::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="54bf0-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="54bf0-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="54bf0-108">Метод **инапсистемхеалсвалидатионрекуест:: жетсохрекуест** позволяет средствам проверки работоспособности системы получать и проверять сведения [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , отправленные их аналогами агента работоспособности системы (SHA) на клиенте.</span><span class="sxs-lookup"><span data-stu-id="54bf0-108">The **INapSystemHealthValidationRequest::GetSoHRequest** method allows System Health Validators (SHVs) to retrieve and validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) information sent by their System Health Agent (SHA) counterparts on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="54bf0-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="54bf0-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] SoHRequest **sohRequest,
  [out] BOOL       *napSystemGenerated
);
```



## <a name="parameters"></a><span data-ttu-id="54bf0-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="54bf0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54bf0-111">*сохрекуест* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="54bf0-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54bf0-112">Указатель на указатель на структуру [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="54bf0-112">A pointer to a pointer to an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) structure.</span></span>

</dd> <dt>

<span data-ttu-id="54bf0-113">*напсистемженератед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="54bf0-113">*napSystemGenerated* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54bf0-114">**Логическое** значение, равное **true** , если состояние работоспособности было создано напажент от имени SHA и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="54bf0-114">A **BOOL** that is **TRUE** if the SoH was created by the NapAgent on behalf of the SHA and **FALSE** otherwise.</span></span> <span data-ttu-id="54bf0-115">Он используется в основном для обозначения сбоя SHA в SHV.</span><span class="sxs-lookup"><span data-stu-id="54bf0-115">It is primarily used to indicate an SHA failure to the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54bf0-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="54bf0-116">Return value</span></span>

<span data-ttu-id="54bf0-117">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="54bf0-117">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="54bf0-118">Код возврата</span><span class="sxs-lookup"><span data-stu-id="54bf0-118">Return code</span></span>                                                                                     | <span data-ttu-id="54bf0-119">Описание</span><span class="sxs-lookup"><span data-stu-id="54bf0-119">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="54bf0-120"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="54bf0-120"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="54bf0-121">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="54bf0-121">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="54bf0-122"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="54bf0-122"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="54bf0-123">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="54bf0-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="54bf0-124"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="54bf0-124"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="54bf0-125">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54bf0-125">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54bf0-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="54bf0-126">Remarks</span></span>

<span data-ttu-id="54bf0-127">Параметр *сохрекуест* может возвращать **значение NULL** , если клиент не отправлял [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) в SHV.</span><span class="sxs-lookup"><span data-stu-id="54bf0-127">The *sohRequest* parameter may return **NULL** if the client did not send an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) to the SHV.</span></span> <span data-ttu-id="54bf0-128">В этом сценарии SHV может заполнить **сохреспонсе** кодом ошибки [**NAP \_ E \_ Missing No \_ SoH**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="54bf0-128">In that scenario the SHV can populate an **SoHResponse** with the error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>

<span data-ttu-id="54bf0-129">Если параметр *напсистемженератед* имеет **значение true**, формат *сохрекуест* выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="54bf0-129">If the *napSystemGenerated* parameter is **TRUE**, the format of *SoHRequest* is as follows:</span></span>

-   <span data-ttu-id="54bf0-130">[**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md)= <id></span><span class="sxs-lookup"><span data-stu-id="54bf0-130">[**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md)= <id></span></span>
-   <span data-ttu-id="54bf0-131">[**сохаттрибутетипефаилурекатегори**](sohattributetype-enum.md) =  [ **фаилурекатегориклиенткомпонент**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span><span class="sxs-lookup"><span data-stu-id="54bf0-131">[**sohAttributeTypeFailureCategory**](sohattributetype-enum.md)= [**failureCategoryClientComponent**](/windows/win32/api/naptypes/ne-naptypes-failurecategory)</span></span>
-   <span data-ttu-id="54bf0-132">[**сохаттрибутетипирроркодес**](sohattributetype-enum.md)  =  [ **<SHA-Failure-Error-code>**](nap-error-constants.md)</span><span class="sxs-lookup"><span data-stu-id="54bf0-132">[**sohAttributeTypeErrorCodes**](sohattributetype-enum.md) = [**<sha-failure-error-code>**](nap-error-constants.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="54bf0-133">Требования</span><span class="sxs-lookup"><span data-stu-id="54bf0-133">Requirements</span></span>



| <span data-ttu-id="54bf0-134">Требование</span><span class="sxs-lookup"><span data-stu-id="54bf0-134">Requirement</span></span> | <span data-ttu-id="54bf0-135">Значение</span><span class="sxs-lookup"><span data-stu-id="54bf0-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54bf0-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="54bf0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="54bf0-137">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="54bf0-137">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="54bf0-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="54bf0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="54bf0-139">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54bf0-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="54bf0-140">Header</span><span class="sxs-lookup"><span data-stu-id="54bf0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="54bf0-141"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="54bf0-141"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="54bf0-142">IDL</span><span class="sxs-lookup"><span data-stu-id="54bf0-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54bf0-143"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54bf0-143"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="54bf0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="54bf0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54bf0-145"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54bf0-145"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="54bf0-146">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="54bf0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54bf0-147">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="54bf0-147">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





