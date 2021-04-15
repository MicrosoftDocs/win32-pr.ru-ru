---
description: Метод DeleteAsync \_ метода SWbemObject асинхронно удаляет текущий класс или текущий экземпляр.
ms.assetid: b8d67fa5-5217-422b-acbe-5eea6028deeb
ms.tgt_platform: multiple
title: Метод SWbemObject.DeleteAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
- ISWbemObject.DeleteAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7951b84a2b5d9f06061f4cefb04c797ccfea3ecd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701959"
---
# <a name="swbemobjectdeleteasync_-method"></a><span data-ttu-id="85742-103">SWbemObject. DeleteAsync, \_ метод</span><span class="sxs-lookup"><span data-stu-id="85742-103">SWbemObject.DeleteAsync\_ method</span></span>

<span data-ttu-id="85742-104">Метод **DeleteAsync \_** метода [**SWbemObject**](swbemobject.md) асинхронно удаляет текущий класс или текущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="85742-104">The **DeleteAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously deletes either the current class or the current instance.</span></span> <span data-ttu-id="85742-105">Если в динамическом поставщике предоставлен класс или экземпляр, то иногда невозможно удалить этот объект, если поставщик не поддерживает удаление класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="85742-105">If a dynamic provider supplies the class or instance, sometimes it is not possible to delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="85742-106">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="85742-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="85742-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85742-107">Syntax</span></span>


```VB
SWbemObject.DeleteAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="85742-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="85742-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85742-109">*обжвбемсинк* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="85742-109">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85742-110">Приемник объекта, который возвращает результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="85742-110">Object sink that returns the outcome of the delete operation.</span></span>

</dd> <dt>

<span data-ttu-id="85742-111">*ифлагс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="85742-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85742-112">Целое число, определяющее поведение вызова.</span><span class="sxs-lookup"><span data-stu-id="85742-112">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="85742-113">Этот параметр может принимать следующие значения.</span><span class="sxs-lookup"><span data-stu-id="85742-113">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="85742-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>Вбемфлагсендстатус \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="85742-114"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="85742-115">Вызывает асинхронные вызовы для отправки обновлений состояния обработчику событий [**свбемсинк. OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="85742-115">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="85742-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>Вбемфлагдонтсендстатус \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="85742-116"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* ( 0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="85742-117">Не позволяет асинхронным вызовам отправлять обновления состояния в обработчик событий [**OnProgress**](swbemsink-onprogress.md) для приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="85742-117">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="85742-118">*обжвбемнамедвалуесет* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="85742-118">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85742-119">Обычно этот параметр не определен.</span><span class="sxs-lookup"><span data-stu-id="85742-119">This parameter is typically undefined.</span></span> <span data-ttu-id="85742-120">В противном случае это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , элементы которого представляют сведения о контексте, которые могут использоваться поставщиком, обслуживающим запрос.</span><span class="sxs-lookup"><span data-stu-id="85742-120">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="85742-121">Поставщик, который поддерживает или требует такую информацию, должен документировать распознанные имена значений, тип данных значения, допустимые значения и семантику.</span><span class="sxs-lookup"><span data-stu-id="85742-121">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="85742-122">*обжвбемасинкконтекст* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="85742-122">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="85742-123">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который возвращает приемнику объекта, чтобы узнать источник исходного асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="85742-123">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="85742-124">Используйте этот параметр, если вы выполняете несколько асинхронных вызовов, использующих один и тот же приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="85742-124">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="85742-125">Чтобы использовать этот параметр, создайте объект **свбемнамедвалуесет** и используйте метод [**свбемнамедвалуесет. Add**](swbemnamedvalueset-add.md) , чтобы добавить значение, идентифицирующее выполняемый асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="85742-125">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="85742-126">Этот объект **свбемнамедвалуесет** возвращается в приемник объекта, и источник вызова можно извлечь с помощью метода [**свбемнамедвалуесет. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="85742-126">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="85742-127">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="85742-127">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85742-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="85742-128">Return value</span></span>

<span data-ttu-id="85742-129">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="85742-129">This method does not return a value.</span></span> <span data-ttu-id="85742-130">Если этот вызов выполнен успешно, результат операции удаления предоставляется через предоставленный приемник объекта.</span><span class="sxs-lookup"><span data-stu-id="85742-130">If this call is successful, the result of the delete operation is provided through the supplied object sink.</span></span>

## <a name="error-codes"></a><span data-ttu-id="85742-131">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="85742-131">Error codes</span></span>

<span data-ttu-id="85742-132">После завершения метода **DeleteAsync \_** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок из следующего списка.</span><span class="sxs-lookup"><span data-stu-id="85742-132">After the completion of the **DeleteAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="85742-133">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="85742-133">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="85742-134">Текущий контекст не имеет достаточных прав безопасности для удаления объекта.</span><span class="sxs-lookup"><span data-stu-id="85742-134">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="85742-135">**вбемеррфаилед** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="85742-135">**wbemErrFailed** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="85742-136">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="85742-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="85742-137">**вбемерринвалидкласс** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="85742-137">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="85742-138">Указанный класс не существует.</span><span class="sxs-lookup"><span data-stu-id="85742-138">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="85742-139">**вбемерринвалидоператион** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="85742-139">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="85742-140">Не удается удалить объект.</span><span class="sxs-lookup"><span data-stu-id="85742-140">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="85742-141">**вбемеррнотфаунд** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="85742-141">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="85742-142">Объект не существует.</span><span class="sxs-lookup"><span data-stu-id="85742-142">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="85742-143">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="85742-143">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="85742-144">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="85742-144">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="85742-145">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85742-145">Remarks</span></span>

<span data-ttu-id="85742-146">Этот вызов возвращает немедленно.</span><span class="sxs-lookup"><span data-stu-id="85742-146">This call returns immediately.</span></span> <span data-ttu-id="85742-147">Состояние возвращается вызывающему объекту с помощью обратного вызова, доставляемого в приемник, указанный в *обжвбемсинк*.</span><span class="sxs-lookup"><span data-stu-id="85742-147">The status is returned to the caller through a callback delivered to the sink that is specified in *objWbemSink*.</span></span>

<span data-ttu-id="85742-148">Асинхронный обратный вызов позволяет пользователю, не прошедшему проверку подлинности, предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="85742-148">An asynchronous callback allows a nonauthenticated user to provide data to the sink.</span></span> <span data-ttu-id="85742-149">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="85742-149">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="85742-150">Чтобы устранить риски, используйте либо семисинчронаус связь, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="85742-150">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="85742-151">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="85742-151">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="85742-152">Требования</span><span class="sxs-lookup"><span data-stu-id="85742-152">Requirements</span></span>



| <span data-ttu-id="85742-153">Требование</span><span class="sxs-lookup"><span data-stu-id="85742-153">Requirement</span></span> | <span data-ttu-id="85742-154">Значение</span><span class="sxs-lookup"><span data-stu-id="85742-154">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="85742-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="85742-155">Minimum supported client</span></span><br/> | <span data-ttu-id="85742-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85742-156">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="85742-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="85742-157">Minimum supported server</span></span><br/> | <span data-ttu-id="85742-158">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85742-158">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="85742-159">Header</span><span class="sxs-lookup"><span data-stu-id="85742-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="85742-160"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="85742-160"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="85742-161">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="85742-161">Type library</span></span><br/>             | <dl> <span data-ttu-id="85742-162"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="85742-162"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="85742-163">DLL</span><span class="sxs-lookup"><span data-stu-id="85742-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="85742-164"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85742-164"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="85742-165">CLSID</span><span class="sxs-lookup"><span data-stu-id="85742-165">CLSID</span></span><br/>                    | <span data-ttu-id="85742-166">\_SWBEMOBJECT CLSID</span><span class="sxs-lookup"><span data-stu-id="85742-166">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="85742-167">IID</span><span class="sxs-lookup"><span data-stu-id="85742-167">IID</span></span><br/>                      | <span data-ttu-id="85742-168">IID \_ исвбемобжект</span><span class="sxs-lookup"><span data-stu-id="85742-168">IID\_ISWbemObject</span></span><br/>                                                            |



 

