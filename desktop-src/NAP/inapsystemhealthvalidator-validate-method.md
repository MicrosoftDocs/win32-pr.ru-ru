---
title: Метод Validate Инапсистемхеалсвалидатор (Напсистемхеалсвалидатор. h)
description: Система защиты доступа к сети для проверки Сохрекуест, полученной от клиента.
ms.assetid: d67dc2c8-f18c-4e06-a51e-a538ca75c3f1
keywords:
- Проверка метода NAP
- Проверка метода NAP, интерфейс Инапсистемхеалсвалидатор
- Инапсистемхеалсвалидатор интерфейса NAP, метод Validate
topic_type:
- apiref
api_name:
- INapSystemHealthValidator.Validate
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f7589a67b9a3b1454e3c65b17ad6f584ce0e655
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672602"
---
# <a name="inapsystemhealthvalidatorvalidate-method"></a><span data-ttu-id="542ce-106">Метод Инапсистемхеалсвалидатор:: Validate</span><span class="sxs-lookup"><span data-stu-id="542ce-106">INapSystemHealthValidator::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="542ce-107">Платформа защиты доступа к сети недоступна начиная с Windows 10</span><span class="sxs-lookup"><span data-stu-id="542ce-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="542ce-108">Метод **инапсистемхеалсвалидатор:: Validate** определяется разработчиком SHV и вызывается системой защиты доступа к сети для проверки [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , полученного от клиента.</span><span class="sxs-lookup"><span data-stu-id="542ce-108">The **INapSystemHealthValidator::Validate** method is defined by the SHV developer and called by the NAP system to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) received from a client.</span></span>

## <a name="syntax"></a><span data-ttu-id="542ce-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="542ce-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] INapSystemHealthValidationRequest *request,
  [in] UINT32                            hintTimeOutInMsec,
  [in] INapServerCallback                *callback
);
```



## <a name="parameters"></a><span data-ttu-id="542ce-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="542ce-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="542ce-111">*запрос* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="542ce-111">*request* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="542ce-112">COM-указатель на объект [**инапсистемхеалсвалидатионрекуест**](inapsystemhealthvalidationrequest.md) , определяющий объект запроса проверки.</span><span class="sxs-lookup"><span data-stu-id="542ce-112">A COM pointer to an [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) object that identifies the validation request object.</span></span>

</dd> <dt>

<span data-ttu-id="542ce-113">*хинттимеаутинмсек* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="542ce-113">*hintTimeOutInMsec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="542ce-114">Длительность периода ожидания связи в миллисекундах.</span><span class="sxs-lookup"><span data-stu-id="542ce-114">The duration, in milliseconds, of the communication timeout period.</span></span> <span data-ttu-id="542ce-115">Средство проверки работоспособности системы (SHV) должно отвечать в течение этого периода времени; в противном случае ответ отбрасывается.</span><span class="sxs-lookup"><span data-stu-id="542ce-115">The System Health Validator (SHV) should respond within this amount of time; otherwise the response is dropped.</span></span>

> [!Note]  
> <span data-ttu-id="542ce-116">Время ожидания по умолчанию для всех SHV составляет 2000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="542ce-116">The default timeout for all SHVs is 2000 milliseconds.</span></span> <span data-ttu-id="542ce-117">Если используется значение, отличное от значения по умолчанию, время ожидания для всех зарегистрированных SHV изменится.</span><span class="sxs-lookup"><span data-stu-id="542ce-117">Using a value other than the default will change the timeout for all registered SHVs.</span></span>

 

</dd> <dt>

<span data-ttu-id="542ce-118">*обратный вызов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="542ce-118">*callback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="542ce-119">Указатель на объект обратного вызова [**инапсерверкаллбакк**](inapservercallback.md).</span><span class="sxs-lookup"><span data-stu-id="542ce-119">A pointer to the callback object [**INapServerCallback**](inapservercallback.md).</span></span> <span data-ttu-id="542ce-120">Этот указатель обратного вызова используется SHV при возврате **E \_ в ожидании** от вызова **инапсистемхеалсвалидатор:: Validate**.</span><span class="sxs-lookup"><span data-stu-id="542ce-120">This callback pointer is used by the SHVs when they return **E\_PENDING** from the call to **INapSystemHealthValidator::Validate**.</span></span> <span data-ttu-id="542ce-121">Используется для асинхронной проверки.</span><span class="sxs-lookup"><span data-stu-id="542ce-121">This is used for asynchronous validation.</span></span> <span data-ttu-id="542ce-122">Средства SHV должны реагировать в течение *хинттимеаутинмсек* времени, иначе ответ будет удален.</span><span class="sxs-lookup"><span data-stu-id="542ce-122">The SHVs are expected to respond within the *hintTimeOutInMsec* time or else the response will be dropped.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="542ce-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="542ce-123">Return value</span></span>

<span data-ttu-id="542ce-124">Если возвращается любой другой код ошибки, система предполагает, что произошел сбой Серверкомпонент и соответствующее сопоставление выполняется для передачи или сбоя.</span><span class="sxs-lookup"><span data-stu-id="542ce-124">If any other error code is returned, then the system assumes serverComponent failure has occurred, and the appropriate mapping is done to pass/fail.</span></span>



| <span data-ttu-id="542ce-125">Код возврата</span><span class="sxs-lookup"><span data-stu-id="542ce-125">Return code</span></span>                                                                                                | <span data-ttu-id="542ce-126">Описание</span><span class="sxs-lookup"><span data-stu-id="542ce-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="542ce-127"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="542ce-127"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="542ce-128">Указывает, что средство проверки установило Сохреспонсе для объекта Request.</span><span class="sxs-lookup"><span data-stu-id="542ce-128">Indicates that the validator has set an SoHResponse on the 'request' object.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="542ce-129"><dt>**\_в ожидании**</dt></span><span class="sxs-lookup"><span data-stu-id="542ce-129"><dt>**E\_PENDING**</dt></span></span> </dl>                  | <span data-ttu-id="542ce-130">Указывает, что OnComplete () будет вызываться в отдельном потоке.</span><span class="sxs-lookup"><span data-stu-id="542ce-130">Indicates that OnComplete() will be called on a separate thread.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="542ce-131"><dt>**\_сервер RPC \_ S \_ недоступен**</dt></span><span class="sxs-lookup"><span data-stu-id="542ce-131"><dt>**RPC\_S\_SERVER\_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="542ce-132">Указывает, что процесс средства проверки работоспособности системы (SHV) завершается без Напсервер фактической освобождения ссылки на него.</span><span class="sxs-lookup"><span data-stu-id="542ce-132">Indicates that the System Health Validator (SHV) process terminated without the NapServer actually releasing a reference to it.</span></span> <span data-ttu-id="542ce-133">Напсервер попытается повторно создать новую ссылку на SHV и снова выполнит вызов Validate.</span><span class="sxs-lookup"><span data-stu-id="542ce-133">The NapServer will try to re-create a new reference to the SHV and will reexecute the Validate call once.</span></span> <span data-ttu-id="542ce-134">Если при создании объекта или повторного выполнения проверки произошел сбой, SHV удаляется из списка загруженных SHV.</span><span class="sxs-lookup"><span data-stu-id="542ce-134">If the creation of the object or the re-executed Validate fails, the SHV is removed from the list of loaded SHVs.</span></span> <span data-ttu-id="542ce-135">Единственным способом перезагрузки этого средства SHV является отмена регистрации и повторной регистрации SHV, а также перезагрузка Напсервер</span><span class="sxs-lookup"><span data-stu-id="542ce-135">The only way this SHV can now be reloaded is to unregister and reregister the SHV again, or when the NapServer restarts</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="542ce-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="542ce-136">Remarks</span></span>

<span data-ttu-id="542ce-137">Чтобы обеспечить обнаружение вторжений, SHV будет запрашивать проверку клиентского компьютера независимо от того, отправляет ли клиент [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) , предназначенный для SHV.</span><span class="sxs-lookup"><span data-stu-id="542ce-137">In order to support intrusion detection, SHVs will be asked to validate the client machine regardless of whether the client sent an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) intended for the SHV.</span></span>

<span data-ttu-id="542ce-138">SHV должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="542ce-138">The SHV must do the following:</span></span>

-   <span data-ttu-id="542ce-139">Получение [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) из *запроса* путем вызова [**запроса. Жетсохрекуест ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span><span class="sxs-lookup"><span data-stu-id="542ce-139">Retrieve the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) from *request* by calling [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md).</span></span>
-   <span data-ttu-id="542ce-140">Если пакет [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) имеет значение NULL:</span><span class="sxs-lookup"><span data-stu-id="542ce-140">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet is null:</span></span>
    -   <span data-ttu-id="542ce-141">Если SHV является системой обнаружения вторжений, заполните пакет [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) соответствующим [**кодом ошибки NAP**](nap-error-constants.md) , чтобы убедиться, что клиентский компьютер является вредоносным.</span><span class="sxs-lookup"><span data-stu-id="542ce-141">If the SHV is an intrusion detection system, populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the appropriate [**NAP error code**](nap-error-constants.md) as to why the client machine is malicious.</span></span>
    -   <span data-ttu-id="542ce-142">Все остальные SHV должны заполнить пакет [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) кодом ошибки [**NAP \_ E \_ Missing No \_ SoH**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="542ce-142">All other SHVs should populate an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with an error code of [**NAP\_E\_MISSING\_SOH**](nap-error-constants.md).</span></span>
-   <span data-ttu-id="542ce-143">Если *напсистемженератед* имеет **значение true** из вызова [**запроса. Жетсохрекуест ()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), SHV должен ждать пакет [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) со следующим 3 ТЛВС: [**сохаттрибутетипесистемхеалсид**](sohattributetype-enum.md), **сохаттрибутетипефаилурекатегори**, **sohAttributeTypeErrorCodes**.</span><span class="sxs-lookup"><span data-stu-id="542ce-143">If *napSystemGenerated* is **TRUE** from the call to [**request.GetSoHRequest()**](inapsystemhealthvalidationrequest-getsohrequest-method.md), the SHV should expect an [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet with the following 3 TLVs: [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md), **sohAttributeTypeFailureCategory**, **sohAttributeTypeErrorCodes**.</span></span> <span data-ttu-id="542ce-144">Этот **сохрекуест** создается напажент от имени агента работоспособности системы (SHA), так как произошла ошибка при получении пакета запроса от SHA.</span><span class="sxs-lookup"><span data-stu-id="542ce-144">This **SoHRequest** is generated by the NapAgent on behalf of the System Health Agent (SHA) since there was an error in retrieving a request packet from the SHA.</span></span>
-   <span data-ttu-id="542ce-145">Проверьте пакет [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) .</span><span class="sxs-lookup"><span data-stu-id="542ce-145">Validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>
    -   <span data-ttu-id="542ce-146">Если [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) имеет неправильный формат, создайте пакет **сохреспонсе** с кодом ошибки [**\_ \_ Недопустимый \_ пакет NAP E**](nap-error-constants.md).</span><span class="sxs-lookup"><span data-stu-id="542ce-146">If the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) is malformed, then construct a **SoHResponse** packet with error code [**NAP\_E\_INVALID\_PACKET**](nap-error-constants.md).</span></span>
    -   <span data-ttu-id="542ce-147">Если SHV использует только кэшированные данные для проверки пакета [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh) (т. е. операций ввода-вывода не выполняется), то он может создать **сохреспонсе**, установить его для объекта в *запросе* и вернуть значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="542ce-147">If the SHV is only using cached information to validate the [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet (i.e. no I/O is performed), then it can construct the **SoHResponse**, set it on the object in *request* and return **S\_OK**.</span></span>
    -   <span data-ttu-id="542ce-148">Если SHV выполняет операции ввода-вывода для взаимодействия с внутренними серверами для проверки работоспособности клиента, он должен поставить в очередь операции ввода-вывода и вернуть эту функцию в **\_ ожидании**.</span><span class="sxs-lookup"><span data-stu-id="542ce-148">If the SHV is performing I/O in order to talk to its back-end servers to validate the client's health, then it must queue up the I/O and return this function with **E\_PENDING**.</span></span> <span data-ttu-id="542ce-149">В этом случае SHV должен вызвать [**обратный вызов. OnComplete ()**](inapservercallback-oncomplete-method.md) в отдельном потоке в течение периода ожидания, *хинттимеаутинмсек*.</span><span class="sxs-lookup"><span data-stu-id="542ce-149">In this case, the SHV must call [**callback.OnComplete()**](inapservercallback-oncomplete-method.md) on a separate thread within the timeout period, *hintTimeOutInMsec*.</span></span> <span data-ttu-id="542ce-150">В противном случае ответ SHV будет удален.</span><span class="sxs-lookup"><span data-stu-id="542ce-150">Otherwise, the SHV's response will be dropped.</span></span>
-   <span data-ttu-id="542ce-151">Не возвращайте никаких других ошибок, кроме перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="542ce-151">Do not return any other error other than those listed above.</span></span> <span data-ttu-id="542ce-152">Если SHV возвращает любой другой код ошибки (например,</span><span class="sxs-lookup"><span data-stu-id="542ce-152">If any other error code is returned by the SHV (eg.</span></span> <span data-ttu-id="542ce-153">часть системной ошибки), пакет будет удален.</span><span class="sxs-lookup"><span data-stu-id="542ce-153">some system error), the packet will be discarded.</span></span>

<span data-ttu-id="542ce-154">SHV должен возвращать TLV **сохаттрибутетипекомплианцересулткодес** или **Сохаттрибутетипефаилурекатегори** в своем [**сохрекуест**](/windows/win32/api/naptypes/ns-naptypes-soh).</span><span class="sxs-lookup"><span data-stu-id="542ce-154">An SHV must return either an **sohAttributeTypeComplianceResultCodes** or **sohAttributeTypeFailureCategory** TLV in its [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh).</span></span>

-   <span data-ttu-id="542ce-155">[**TLV сохаттрибутетипекомплианцересулткодес**](sohattributetype-enum.md). Если SHV может проверить работоспособность клиента (т. е. работоспособность или неработоспособность), возвращается этот TLV.</span><span class="sxs-lookup"><span data-stu-id="542ce-155">[**sohAttributeTypeComplianceResultCodes TLV**](sohattributetype-enum.md): If the SHV could validate the health of the client (i.e. healthy or unhealthy), this TLV is returned.</span></span>
-   <span data-ttu-id="542ce-156">[**TLV сохаттрибутетипефаилурекатегори**](sohattributetype-enum.md). Если на клиенте или сервере существовали какие либо компоненты или сбои связи, они должны быть обозначены этим TLV.</span><span class="sxs-lookup"><span data-stu-id="542ce-156">[**sohAttributeTypeFailureCategory TLV**](sohattributetype-enum.md): If there was any component or communication failure on the client or server, it must be indicated by this TLV.</span></span> <span data-ttu-id="542ce-157">Этот TLV будет сопоставлено с работоспособным или неработоспособным в зависимости от конфигурации SHV.</span><span class="sxs-lookup"><span data-stu-id="542ce-157">This TLV will further be mapped to healthy or unhealthy depending upon the SHV's configuration.</span></span> <span data-ttu-id="542ce-158">Дополнительные сведения см. в разделе интерфейс [**инапсерверманажемент**](inapservermanagement.md) и структура [**фаилурекатегоримаппинг**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) .</span><span class="sxs-lookup"><span data-stu-id="542ce-158">For more details, see the [**INapServerManagement**](inapservermanagement.md) interface and the [**FailureCategoryMapping**](/windows/win32/api/naptypes/ns-naptypes-failurecategorymapping) structure.</span></span>

<span data-ttu-id="542ce-159">SHV не должен хранить ссылки на *запрос* или *обратный вызов* после завершения вызова асинкронаус.</span><span class="sxs-lookup"><span data-stu-id="542ce-159">The SHV must not hold references to *request* or *callback* once the asyncronous call completes.</span></span>

## <a name="requirements"></a><span data-ttu-id="542ce-160">Требования</span><span class="sxs-lookup"><span data-stu-id="542ce-160">Requirements</span></span>



| <span data-ttu-id="542ce-161">Требование</span><span class="sxs-lookup"><span data-stu-id="542ce-161">Requirement</span></span> | <span data-ttu-id="542ce-162">Значение</span><span class="sxs-lookup"><span data-stu-id="542ce-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="542ce-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="542ce-163">Minimum supported client</span></span><br/> | <span data-ttu-id="542ce-164">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="542ce-164">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="542ce-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="542ce-165">Minimum supported server</span></span><br/> | <span data-ttu-id="542ce-166">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="542ce-166">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="542ce-167">Header</span><span class="sxs-lookup"><span data-stu-id="542ce-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="542ce-168"><dt>Напсистемхеалсвалидатор. h</dt></span><span class="sxs-lookup"><span data-stu-id="542ce-168"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="542ce-169">IDL</span><span class="sxs-lookup"><span data-stu-id="542ce-169">IDL</span></span><br/>                      | <dl> <span data-ttu-id="542ce-170"><dt>Напсистемхеалсвалидатор. idl</dt></span><span class="sxs-lookup"><span data-stu-id="542ce-170"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="542ce-171">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="542ce-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="542ce-172">**инапсистемхеалсвалидатор**</span><span class="sxs-lookup"><span data-stu-id="542ce-172">**INapSystemHealthValidator**</span></span>](inapsystemhealthvalidator.md)
</dt> </dl>

 

 





