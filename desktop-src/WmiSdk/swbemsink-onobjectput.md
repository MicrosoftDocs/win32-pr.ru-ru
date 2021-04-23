---
description: Событие Онобжектпут объекта Свбемсинк активируется при завершении асинхронной операции размещения. Это событие возвращает путь к объекту экземпляра или сохраненного класса.
ms.assetid: 2046dd03-ac2c-49fa-b1ad-a458967709e5
ms.tgt_platform: multiple
title: 'Событие Исвбемсинкевентс:: Онобжектпут (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.OnObjectPut
- ISWbemSinkEvents.OnObjectPut
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c6ed42105efe407558d80cd108e657e396e88763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272744"
---
# <a name="iswbemsinkeventsonobjectput-event"></a><span data-ttu-id="2fcf4-104">Событие Исвбемсинкевентс:: Онобжектпут</span><span class="sxs-lookup"><span data-stu-id="2fcf4-104">ISWbemSinkEvents::OnObjectPut event</span></span>

<span data-ttu-id="2fcf4-105">Событие **онобжектпут** объекта [**свбемсинк**](swbemsink.md) активируется при завершении асинхронной операции размещения.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-105">The **OnObjectPut** event of an [**SWbemSink**](swbemsink.md) object is triggered when an asynchronous Put operation is complete.</span></span> <span data-ttu-id="2fcf4-106">Это событие возвращает путь к объекту экземпляра или сохраненного класса.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-106">This event returns the object path of the instance or the saved class.</span></span>

<span data-ttu-id="2fcf4-107">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="2fcf4-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcf4-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2fcf4-108">Syntax</span></span>


```VB
SWbemSink.OnObjectPut( _
  ByVal objWbemObjectPath, _
  ByVal objWbemAsyncContext _
)
```



## <a name="parameters"></a><span data-ttu-id="2fcf4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2fcf4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2fcf4-110">*обжвбемобжектпас*</span><span class="sxs-lookup"><span data-stu-id="2fcf4-110">*objWbemObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="2fcf4-111">Объект [**свбемобжектпас**](swbemobjectpath.md) , содержащий путь к объекту экземпляра или класса, который операция размещения записывает в WMI.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-111">An [**SWbemObjectPath**](swbemobjectpath.md) object, that contains the object path of the instance or class that the put operation writes to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="2fcf4-112">*обжвбемасинкконтекст*</span><span class="sxs-lookup"><span data-stu-id="2fcf4-112">*objWbemAsyncContext*</span></span> 
</dt> <dd>

<span data-ttu-id="2fcf4-113">Объект [**свбемнамедвалуесет**](swbemnamedvalueset.md) , который передается в исходный асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-113">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is passed to the original asynchronous call.</span></span> <span data-ttu-id="2fcf4-114">Используйте этот параметр, чтобы указать происхождение асинхронного вызова, который активирует это событие, когда с помощью этого приемника объектов выполняется несколько асинхронных вызовов.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-114">Use this parameter to identify the origin of the asynchronous call that triggers this event when multiple asynchronous calls are made using this object sink.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2fcf4-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2fcf4-115">Return value</span></span>

<span data-ttu-id="2fcf4-116">Это событие не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-116">This event does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="2fcf4-117">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="2fcf4-117">Error codes</span></span>

<span data-ttu-id="2fcf4-118">После завершения события **онобжектпут** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-118">After the completion of the **OnObjectPut** event, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="2fcf4-119">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-119">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="2fcf4-120">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-120">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="2fcf4-121">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-121">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="2fcf4-122">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-122">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2fcf4-123">**вбемерртранспортфаилуре** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="2fcf4-123">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="2fcf4-124">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-124">Networking error occurred, preventing normal operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2fcf4-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2fcf4-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2fcf4-126">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-126">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="2fcf4-127">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-127">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="2fcf4-128">Чтобы устранить риски, используйте либо частично синхронное соединение, либо синхронное взаимодействие.</span><span class="sxs-lookup"><span data-stu-id="2fcf4-128">To eliminate the risks, use either semi-synchronous communication or synchronous communication.</span></span> <span data-ttu-id="2fcf4-129">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="2fcf4-129">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="2fcf4-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2fcf4-130">Requirements</span></span>



| <span data-ttu-id="2fcf4-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2fcf4-131">Requirement</span></span> | <span data-ttu-id="2fcf4-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2fcf4-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcf4-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2fcf4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcf4-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2fcf4-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2fcf4-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2fcf4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcf4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2fcf4-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2fcf4-137">Header</span><span class="sxs-lookup"><span data-stu-id="2fcf4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2fcf4-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2fcf4-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="2fcf4-139">IDL</span><span class="sxs-lookup"><span data-stu-id="2fcf4-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2fcf4-140"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2fcf4-140"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="2fcf4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2fcf4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcf4-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcf4-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="2fcf4-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="2fcf4-143">CLSID</span></span><br/>                    | <span data-ttu-id="2fcf4-144">\_СВБЕМСИНК CLSID</span><span class="sxs-lookup"><span data-stu-id="2fcf4-144">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="2fcf4-145">IID</span><span class="sxs-lookup"><span data-stu-id="2fcf4-145">IID</span></span><br/>                      | <span data-ttu-id="2fcf4-146">IID \_ исвбемсинкевентс</span><span class="sxs-lookup"><span data-stu-id="2fcf4-146">IID\_ISWbemSinkEvents</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="2fcf4-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2fcf4-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2fcf4-148">**свбемсинк**</span><span class="sxs-lookup"><span data-stu-id="2fcf4-148">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

