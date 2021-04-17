---
description: Событие OnProgress Свбемсинк активируется, когда асинхронный вызов возвращает состояние выполняемого вызова.
ms.assetid: abb43916-f952-41fe-a5ba-0428864c0685
ms.tgt_platform: multiple
title: 'Событие Исвбемсинкевентс:: OnProgress (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnProgress
- ISWbemSinkEvents.OnProgress
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d322309adcfad33b1c303d7efd6af28db1cac80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105713030"
---
# <a name="iswbemsinkeventsonprogress-event"></a><span data-ttu-id="dd1eb-103">Событие Исвбемсинкевентс:: OnProgress</span><span class="sxs-lookup"><span data-stu-id="dd1eb-103">ISWbemSinkEvents::OnProgress event</span></span>

<span data-ttu-id="dd1eb-104">Событие **OnProgress** [**свбемсинк**](swbemsink.md) активируется, когда асинхронный вызов возвращает состояние выполняемого вызова.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-104">The **OnProgress** event of [**SWbemSink**](swbemsink.md) is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="dd1eb-105">Если события, экземпляры или классы создаются поставщиком, который поддерживает обновления состояния, можно поместить код в это событие, чтобы предоставить пользователям отзыв о состоянии асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-105">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to provide users with feedback about the status of an asynchronous operation.</span></span> <span data-ttu-id="dd1eb-106">Если требуется получить обновления состояния, необходимо установить параметр *ифлагс* асинхронного вызова в значение **вбемфлагсендстатус** (128/0x80), в противном случае это событие не будет запущено.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-106">You must set the *iFlags* parameter of the asynchronous call to **wbemFlagSendStatus** (128/0x80) if you want to receive status updates, otherwise this event is not triggered.</span></span>

<span data-ttu-id="dd1eb-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="dd1eb-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dd1eb-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd1eb-108">Syntax</span></span>


```VB
SWbemSink.OnProgress( _
  ByVal iUpperBound, _
  ByVal iCurrent, _
  ByVal strMessage, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="dd1eb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="dd1eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd1eb-110">*иуппербаунд*</span><span class="sxs-lookup"><span data-stu-id="dd1eb-110">*iUpperBound*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1eb-111">Целое число, описывающее общее количество задач для выполнения.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-111">Integer that describes the total number of tasks to complete.</span></span>

</dd> <dt>

<span data-ttu-id="dd1eb-112">*икуррент*</span><span class="sxs-lookup"><span data-stu-id="dd1eb-112">*iCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1eb-113">Текущий обрабатываемый элемент.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-113">Current item that is being processed.</span></span>

</dd> <dt>

<span data-ttu-id="dd1eb-114">*strMessage*</span><span class="sxs-lookup"><span data-stu-id="dd1eb-114">*strMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1eb-115">Сообщение, описывающее состояние текущей задачи.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-115">Message that describes the status of the current task.</span></span>

</dd> <dt>

<span data-ttu-id="dd1eb-116">*обжвбемасинкконтекст*</span><span class="sxs-lookup"><span data-stu-id="dd1eb-116">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="dd1eb-117">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который передается в исходный асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-117">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="dd1eb-118">Используйте этот параметр, чтобы указать происхождение асинхронного вызова, который активирует это событие, когда с помощью этого приемника объектов выполняется несколько асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-118">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd1eb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd1eb-119">Return value</span></span>

<span data-ttu-id="dd1eb-120">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-120">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="dd1eb-121">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dd1eb-121">Error codes</span></span>

<span data-ttu-id="dd1eb-122">После завершения события **OnProgress** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-122">After the completion of the **OnProgress** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="dd1eb-123">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="dd1eb-123">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="dd1eb-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-124">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="dd1eb-125">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="dd1eb-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="dd1eb-126">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-126">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="dd1eb-127">**вбемерртранспортфаилуре** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="dd1eb-127">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="dd1eb-128">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-128">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd1eb-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd1eb-129">Remarks</span></span>

<span data-ttu-id="dd1eb-130">Событие **OnProgress** активируется, когда асинхронный вызов возвращает состояние выполняемого вызова.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-130">The **OnProgress** event is triggered when an asynchronous call returns the status of a call that is in progress.</span></span> <span data-ttu-id="dd1eb-131">Если события, экземпляры или классы создаются поставщиком, который поддерживает обновления состояния, можно поместить код в это событие, чтобы дать пользователям отзыв о состоянии асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-131">If the events, instances, or classes are produced from a provider that supports status updates, you can place code in this event to give users feedback about the status of an asynchronous operation.</span></span>

> [!Note]  
> <span data-ttu-id="dd1eb-132">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-132">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="dd1eb-133">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-133">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="dd1eb-134">Чтобы устранить риски, используйте частично синхронное или синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="dd1eb-134">To eliminate the risks, use semi-synchronous or synchronous communication.</span></span> <span data-ttu-id="dd1eb-135">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="dd1eb-135">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dd1eb-136">Требования</span><span class="sxs-lookup"><span data-stu-id="dd1eb-136">Requirements</span></span>



| <span data-ttu-id="dd1eb-137">Требование</span><span class="sxs-lookup"><span data-stu-id="dd1eb-137">Requirement</span></span> | <span data-ttu-id="dd1eb-138">Значение</span><span class="sxs-lookup"><span data-stu-id="dd1eb-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd1eb-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd1eb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="dd1eb-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd1eb-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dd1eb-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd1eb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="dd1eb-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd1eb-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dd1eb-143">Header</span><span class="sxs-lookup"><span data-stu-id="dd1eb-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd1eb-144"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd1eb-144"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd1eb-145">IDL</span><span class="sxs-lookup"><span data-stu-id="dd1eb-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="dd1eb-146"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="dd1eb-146"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="dd1eb-147">DLL</span><span class="sxs-lookup"><span data-stu-id="dd1eb-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd1eb-148"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd1eb-148"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd1eb-149">CLSID</span><span class="sxs-lookup"><span data-stu-id="dd1eb-149">CLSID</span></span><br/>                    | <span data-ttu-id="dd1eb-150">\_СВБЕМСИНК CLSID</span><span class="sxs-lookup"><span data-stu-id="dd1eb-150">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="dd1eb-151">IID</span><span class="sxs-lookup"><span data-stu-id="dd1eb-151">IID</span></span><br/>                      | <span data-ttu-id="dd1eb-152">IID \_ исвбемсинкевентс</span><span class="sxs-lookup"><span data-stu-id="dd1eb-152">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="dd1eb-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd1eb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd1eb-154">**свбемсинк**</span><span class="sxs-lookup"><span data-stu-id="dd1eb-154">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

