---
description: Метод Cancel объекта Свбемсинк отменяет все невыполненные асинхронные операции, связанные с этим приемником объекта.
ms.assetid: dbe1eb24-5d9d-407a-b7c6-c58ec6891d7a
ms.tgt_platform: multiple
title: 'Метод Исвбемсинк:: Cancel (Wbemdisp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSink.Cancel
- ISWbemSink.Cancel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37bb44e8c34aa3cd7f9d491656461097e5a2bb5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272745"
---
# <a name="iswbemsinkcancel-method"></a><span data-ttu-id="b1f5b-103">Метод Исвбемсинк:: Cancel</span><span class="sxs-lookup"><span data-stu-id="b1f5b-103">ISWbemSink::Cancel method</span></span>

<span data-ttu-id="b1f5b-104">Метод **Cancel** объекта [**свбемсинк**](swbemsink.md) отменяет все невыполненные асинхронные операции, связанные с этим приемником объекта.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-104">The **Cancel** method of the [**SWbemSink**](swbemsink.md) object cancels all outstanding asynchronous operations that are associated with this object sink.</span></span>

<span data-ttu-id="b1f5b-105">Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b1f5b-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b1f5b-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1f5b-106">Syntax</span></span>


```VB
SWbemSink.Cancel()
```



## <a name="parameters"></a><span data-ttu-id="b1f5b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1f5b-107">Parameters</span></span>

<span data-ttu-id="b1f5b-108">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b1f5b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1f5b-109">Return value</span></span>

<span data-ttu-id="b1f5b-110">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-110">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b1f5b-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b1f5b-111">Error codes</span></span>

<span data-ttu-id="b1f5b-112">После завершения метода **Cancel** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать один из кодов ошибок, приведенных ниже.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-112">After the completion of the **Cancel** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="b1f5b-113">**вбемеррфаилед** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="b1f5b-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="b1f5b-114">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="b1f5b-115">**вбемерраутофмемори** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b1f5b-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b1f5b-116">Недостаточно памяти для завершения операции.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-116">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1f5b-117">**вбемерртранспортфаилуре** -2147749909 (0x80041015)</span><span class="sxs-lookup"><span data-stu-id="b1f5b-117">**wbemErrTransportFailure** - 2147749909 (0x80041015)</span></span>
</dt> <dd>

<span data-ttu-id="b1f5b-118">Произошла сетевая ошибка, препятствующая нормальной работе.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-118">Networking error occurred, preventing normal operation.</span></span>

</dd> <dt>

<span data-ttu-id="b1f5b-119">**вбемерракцессдениед** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="b1f5b-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="b1f5b-120">Текущее или указанное имя пользователя и пароль не являются допустимыми или разрешены для создания подключения.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-120">Current or specified user name and password are not valid or authorized to make the connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b1f5b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1f5b-121">Remarks</span></span>

<span data-ttu-id="b1f5b-122">Нельзя отменить только один асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-122">You cannot cancel only one asynchronous call.</span></span> <span data-ttu-id="b1f5b-123">Если ожидается несколько асинхронных вызовов, использующих этот приемник объектов, этот метод отменяет все асинхронные вызовы с помощью этого приемника объекта.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-123">If multiple asynchronous calls are pending that use this object sink, then this method cancels all the asynchronous calls using this object sink.</span></span> <span data-ttu-id="b1f5b-124">Асинхронные вызовы, связанные с другими приемниками объектов, остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-124">Asynchronous calls that are associated with other object sinks continue unaffected.</span></span>

<span data-ttu-id="b1f5b-125">Невозможно присвоить этот приемник значение **Nothing** для отмены асинхронной операции.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-125">You cannot assign this sink to **Nothing** to cancel an asynchronous operation.</span></span> <span data-ttu-id="b1f5b-126">Необходимо вызвать метод **Cancel** , чтобы сделать Инструментарий WMI прекращением операции и освободить связанные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-126">You must call the **Cancel** method to make WMI discontinue the operation and free the associated resources.</span></span> <span data-ttu-id="b1f5b-127">Это очень важно при длительных асинхронных операциях, таких как запросы или операции, которые никогда не были выполнены, например [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span><span class="sxs-lookup"><span data-stu-id="b1f5b-127">This is very important with lengthy asynchronous operations, such as queries, or operations that never complete, such as [**ExecNotificationQueryAsync**](swbemservices-execnotificationqueryasync.md).</span></span>

> [!Note]  
> <span data-ttu-id="b1f5b-128">Асинхронный обратный вызов позволяет пользователю без проверки подлинности предоставлять данные в приемник.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-128">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="b1f5b-129">Это создает угрозы безопасности для сценариев и приложений.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-129">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="b1f5b-130">Чтобы устранить риски, используйте семисинчронаус или синхронный обмен данными.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-130">To eliminate the risks, use semisynchronous or synchronous communication.</span></span> <span data-ttu-id="b1f5b-131">Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="b1f5b-131">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="b1f5b-132">В следующем примере показано, как отменить асинхронный вызов.</span><span class="sxs-lookup"><span data-stu-id="b1f5b-132">The following example shows you how to cancel an asynchronous call.</span></span>


```VB
objwbemsink.Cancel()
set objwbemsink= Nothing
```



## <a name="requirements"></a><span data-ttu-id="b1f5b-133">Требования</span><span class="sxs-lookup"><span data-stu-id="b1f5b-133">Requirements</span></span>



| <span data-ttu-id="b1f5b-134">Требование</span><span class="sxs-lookup"><span data-stu-id="b1f5b-134">Requirement</span></span> | <span data-ttu-id="b1f5b-135">Значение</span><span class="sxs-lookup"><span data-stu-id="b1f5b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1f5b-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b1f5b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b1f5b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1f5b-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1f5b-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b1f5b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b1f5b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1f5b-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1f5b-140">Header</span><span class="sxs-lookup"><span data-stu-id="b1f5b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1f5b-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1f5b-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1f5b-142">IDL</span><span class="sxs-lookup"><span data-stu-id="b1f5b-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1f5b-143"><dt>Wbemdisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1f5b-143"><dt>Wbemdisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1f5b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b1f5b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1f5b-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1f5b-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1f5b-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1f5b-146">CLSID</span></span><br/>                    | <span data-ttu-id="b1f5b-147">\_СВБЕМСИНК CLSID</span><span class="sxs-lookup"><span data-stu-id="b1f5b-147">CLSID\_SWbemSink</span></span><br/>                                                             |
| <span data-ttu-id="b1f5b-148">IID</span><span class="sxs-lookup"><span data-stu-id="b1f5b-148">IID</span></span><br/>                      | <span data-ttu-id="b1f5b-149">IID \_ исвбемсинк</span><span class="sxs-lookup"><span data-stu-id="b1f5b-149">IID\_ISWbemSink</span></span><br/>                                                              |



## <a name="see-also"></a><span data-ttu-id="b1f5b-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b1f5b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1f5b-151">**свбемсинк**</span><span class="sxs-lookup"><span data-stu-id="b1f5b-151">**SWbemSink**</span></span>](swbemsink.md)
</dt> </dl>

 

