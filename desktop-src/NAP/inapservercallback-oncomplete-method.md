---
title: Метод onComplete Инапсерверкаллбакк (Напсистемхеалсвалидатор. h)
description: Используется SHV для сигнализации о завершении асинхронного запроса.
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- Метод onComplete NAP
- Метод onComplete NAP, интерфейс Инапсерверкаллбакк
- Инапсерверкаллбакк интерфейса NAP, метод onComplete
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef846d3d9dc2d6618f0eca9f097d74222606eb4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493236"
---
# <a name="inapservercallbackoncomplete-method"></a><span data-ttu-id="920da-106">Метод Инапсерверкаллбакк:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="920da-106">INapServerCallback::OnComplete method</span></span>

> [!Note]  
> <span data-ttu-id="920da-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="920da-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="920da-108">Метод **инапсерверкаллбакк:: OnComplete** используется SHV для сигнализации о завершении асинхронного запроса.</span><span class="sxs-lookup"><span data-stu-id="920da-108">The **INapServerCallback::OnComplete** method is used by SHVs to signal asynchronous request completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="920da-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="920da-109">Syntax</span></span>


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="920da-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="920da-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="920da-111">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="920da-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="920da-112">Указатель на объект [**инапсистемхеалсвалидатионрекуест**](inapsystemhealthvalidationrequest.md) , представляющий запрос на проверку.</span><span class="sxs-lookup"><span data-stu-id="920da-112">A pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that represents a validation request.</span></span>

</dd> <dt>

<span data-ttu-id="920da-113">*код ошибки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="920da-113">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="920da-114">[**Код ошибки NAP**](nap-error-constants.md) , указывающий причину, по которой не удалось выполнить проверку.</span><span class="sxs-lookup"><span data-stu-id="920da-114">A [**NAP error code**](nap-error-constants.md) that indicates the reason why the validation could not be performed.</span></span>

> [!Note]  
> <span data-ttu-id="920da-115">Как правило, возвращаемое значение метода [**инапсистемхеалсвалидатионрекуест:: сетсохреспонсе**](inapsystemhealthvalidationrequest-setsohresponse-method.md) передается этому параметру.</span><span class="sxs-lookup"><span data-stu-id="920da-115">Typically, the return value of the [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) method is passed to this parameter.</span></span> <span data-ttu-id="920da-116">Однако, если **сетсохреспонсе** не удалось вызвать из-за сбоя повторной обработки, передается значение, возвращенное неудачной командой.</span><span class="sxs-lookup"><span data-stu-id="920da-116">However, if **SetSoHResponse** could not be called due to a reprocessing failure, the value returned by the failed command is passed.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="920da-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="920da-117">Return value</span></span>

<span data-ttu-id="920da-118">Также могут возвращаться другие коды ошибок, относящиеся к COM.</span><span class="sxs-lookup"><span data-stu-id="920da-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="920da-119">Код возврата</span><span class="sxs-lookup"><span data-stu-id="920da-119">Return code</span></span>                                                                                     | <span data-ttu-id="920da-120">Описание</span><span class="sxs-lookup"><span data-stu-id="920da-120">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="920da-121"><dt>**С \_ ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="920da-121"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="920da-122">Операция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="920da-122">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="920da-123"><dt>**Д \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="920da-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="920da-124">Ошибка разрешений, доступ запрещен.</span><span class="sxs-lookup"><span data-stu-id="920da-124">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="920da-125"><dt>**Д \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="920da-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="920da-126">Не удалось выполнить операцию из – за пределов системных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="920da-126">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="920da-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="920da-127">Remarks</span></span>

<span data-ttu-id="920da-128">Проверяющие элементы управления должны возвращать \_ значение "ОК", если проверка [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) может быть завершена независимо от того, прошел ли **сохрекуест** проверку работоспособности.</span><span class="sxs-lookup"><span data-stu-id="920da-128">Validators must return S\_OK if the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) validation could be completed, regardless of whether the **SoHRequest** passed the health check.</span></span>

## <a name="requirements"></a><span data-ttu-id="920da-129">Требования</span><span class="sxs-lookup"><span data-stu-id="920da-129">Requirements</span></span>



| <span data-ttu-id="920da-130">Требование</span><span class="sxs-lookup"><span data-stu-id="920da-130">Requirement</span></span> | <span data-ttu-id="920da-131">Значение</span><span class="sxs-lookup"><span data-stu-id="920da-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="920da-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="920da-132">Minimum supported client</span></span><br/> | <span data-ttu-id="920da-133">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="920da-133">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="920da-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="920da-134">Minimum supported server</span></span><br/> | <span data-ttu-id="920da-135">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="920da-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="920da-136">Header</span><span class="sxs-lookup"><span data-stu-id="920da-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="920da-137"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="920da-137"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="920da-138">IDL</span><span class="sxs-lookup"><span data-stu-id="920da-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="920da-139"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="920da-139"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="920da-140">DLL</span><span class="sxs-lookup"><span data-stu-id="920da-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="920da-141"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="920da-141"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="920da-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="920da-142">See also</span></span>

<dl> <span data-ttu-id="920da-143"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="920da-143"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="920da-144">**инапсерверкаллбакк**</span><span class="sxs-lookup"><span data-stu-id="920da-144">**INapServerCallback**</span></span>](inapservercallback.md)
</dt> <dt>

[<span data-ttu-id="920da-145">**инапсистемхеалсвалидатионрекуест**</span><span class="sxs-lookup"><span data-stu-id="920da-145">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





