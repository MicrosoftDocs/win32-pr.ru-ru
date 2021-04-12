---
description: Событие OnComplete объекта Свбемсинк активируется после завершения асинхронного вызова. Это событие указывает клиентскому приложению, результату асинхронной операции и предоставляет сведения об ошибке при сбое асинхронного вызова.
ms.assetid: 2723185d-5b8b-4cc7-ada3-51c3275272a9
ms.tgt_platform: multiple
title: 'Событие Исвбемсинкевентс:: OnComplete (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnCompleted
- ISWbemSinkEvents.OnCompleted
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 16cb0362b5c1b1d432d72bb959103adbb7315069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155811"
---
# <a name="iswbemsinkeventsoncompleted-event"></a><span data-ttu-id="7ff4b-104">Событие Исвбемсинкевентс:: OnComplete</span><span class="sxs-lookup"><span data-stu-id="7ff4b-104">ISWbemSinkEvents::OnCompleted event</span></span>

<span data-ttu-id="7ff4b-105">Событие **OnComplete** объекта [**свбемсинк**](swbemsink.md) активируется после завершения асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-105">The **OnCompleted** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous call is complete.</span></span> <span data-ttu-id="7ff4b-106">Это событие указывает клиентскому приложению, результату асинхронной операции и предоставляет сведения об ошибке при сбое асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-106">This event indicates to the client application, the result of an asynchronous operation, and provides error information when the asynchronous call fails.</span></span>

<span data-ttu-id="7ff4b-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7ff4b-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7ff4b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ff4b-108">Syntax</span></span>


```VB
SWbemSink.OnCompleted( _
  ByVal iHResult, _
  ByVal objWbemErrorObject, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="7ff4b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ff4b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ff4b-110">*ихресулт*</span><span class="sxs-lookup"><span data-stu-id="7ff4b-110">*iHResult*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff4b-111">Значение HRESULT завершенного асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-111">The HRESULT of the completed asynchronous method.</span></span> <span data-ttu-id="7ff4b-112">Значение HRESULT совпадает со значением, возвращаемым из эквивалентного [API COM для](com-api-for-wmi.md) вызова метода WMI.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-112">The HRESULT is the same as the value that is returned from an equivalent [COM API for WMI](com-api-for-wmi.md) method call.</span></span> <span data-ttu-id="7ff4b-113">Проверьте это значение, чтобы определить, успешно ли вызван асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-113">Check this value to determine whether or not the asynchronous call is successful.</span></span> <span data-ttu-id="7ff4b-114">Если асинхронный вызов выполнен успешно, этот параметр содержит значение WBEM, \_ \_ No \_ Error (0).</span><span class="sxs-lookup"><span data-stu-id="7ff4b-114">If the asynchronous call is successful, this parameter contains WBEM\_S\_NO\_ERROR (0).</span></span> <span data-ttu-id="7ff4b-115">В случае сбоя асинхронного вызова этот параметр содержит код ошибки.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-115">If the asynchronous call fails, this parameter contains an error code.</span></span>

</dd> <dt>

<span data-ttu-id="7ff4b-116">*обжвбемерроробжект*</span><span class="sxs-lookup"><span data-stu-id="7ff4b-116">*objWbemErrorObject*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff4b-117">Содержит объект [**свбемластеррор**](swbemlasterror.md) при сбое асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-117">Contains an [**SWbemLastError**](swbemlasterror.md) object when the asynchronous method fails.</span></span>

</dd> <dt>

<span data-ttu-id="7ff4b-118">*обжвбемасинкконтекст*</span><span class="sxs-lookup"><span data-stu-id="7ff4b-118">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="7ff4b-119">Это объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который передается в исходный асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-119">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="7ff4b-120">Используйте этот параметр, чтобы указать происхождение асинхронного вызова, который активирует это событие, когда с помощью этого приемника объектов выполняется несколько асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-120">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ff4b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7ff4b-121">Return value</span></span>

<span data-ttu-id="7ff4b-122">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-122">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7ff4b-123">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="7ff4b-123">Error codes</span></span>

<span data-ttu-id="7ff4b-124">После завершения события **OnComplete** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-124">After completion of the **OnCompleted** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="7ff4b-125">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="7ff4b-125">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="7ff4b-126">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-126">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7ff4b-127">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="7ff4b-127">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="7ff4b-128">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-128">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="7ff4b-129">**вбемерртранспортфаилуре** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="7ff4b-129">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="7ff4b-130">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-130">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7ff4b-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7ff4b-131">Remarks</span></span>

<span data-ttu-id="7ff4b-132">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="7ff4b-133">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="7ff4b-134">Чтобы устранить риски, используйте семисинчронаус или синхронный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="7ff4b-134">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="7ff4b-135">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="7ff4b-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ff4b-136">Требования</span><span class="sxs-lookup"><span data-stu-id="7ff4b-136">Requirements</span></span>



| <span data-ttu-id="7ff4b-137">Требование</span><span class="sxs-lookup"><span data-stu-id="7ff4b-137">Requirement</span></span> | <span data-ttu-id="7ff4b-138">Значение</span><span class="sxs-lookup"><span data-stu-id="7ff4b-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ff4b-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7ff4b-139">Minimum supported client</span></span><br/> | <span data-ttu-id="7ff4b-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ff4b-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7ff4b-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7ff4b-141">Minimum supported server</span></span><br/> | <span data-ttu-id="7ff4b-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ff4b-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7ff4b-143">Header</span><span class="sxs-lookup"><span data-stu-id="7ff4b-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ff4b-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ff4b-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ff4b-145">IDL</span><span class="sxs-lookup"><span data-stu-id="7ff4b-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ff4b-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ff4b-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ff4b-147">DLL</span><span class="sxs-lookup"><span data-stu-id="7ff4b-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ff4b-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ff4b-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7ff4b-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="7ff4b-149">CLSID</span></span><br/>                    | <span data-ttu-id="7ff4b-150">\_СВБЕМСИНК CLSID</span><span class="sxs-lookup"><span data-stu-id="7ff4b-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="7ff4b-151">IID</span><span class="sxs-lookup"><span data-stu-id="7ff4b-151">IID</span></span><br/>                      | <span data-ttu-id="7ff4b-152">IID \_ исвбемсинкевентс</span><span class="sxs-lookup"><span data-stu-id="7ff4b-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



 

