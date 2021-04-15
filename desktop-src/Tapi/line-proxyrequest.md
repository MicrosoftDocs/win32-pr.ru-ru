---
description: Сообщение TAPI LINE \_ проксирекуест доставляет запрос в зарегистрированный обработчик прокси-функции.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Сообщение LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688807"
---
# <a name="line_proxyrequest-message"></a><span data-ttu-id="bbba4-103">Строка \_ сообщения проксирекуест</span><span class="sxs-lookup"><span data-stu-id="bbba4-103">LINE\_PROXYREQUEST message</span></span>

<span data-ttu-id="bbba4-104">Сообщение TAPI **Line \_ проксирекуест** доставляет запрос в зарегистрированный обработчик прокси-функции.</span><span class="sxs-lookup"><span data-stu-id="bbba4-104">The TAPI **LINE\_PROXYREQUEST** message delivers a request to a registered proxy function handler.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="bbba4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="bbba4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bbba4-106">*хдевице*</span><span class="sxs-lookup"><span data-stu-id="bbba4-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="bbba4-107">Маркер приложения для линейного устройства, на котором изменилось состояние агента.</span><span class="sxs-lookup"><span data-stu-id="bbba4-107">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="bbba4-108">*двкаллбаккинстанце*</span><span class="sxs-lookup"><span data-stu-id="bbba4-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="bbba4-109">Экземпляр обратного вызова, указанный при открытии линии вызова.</span><span class="sxs-lookup"><span data-stu-id="bbba4-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="bbba4-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="bbba4-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="bbba4-111">Указатель на структуру [**линепроксирекуест**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) , содержащую запрос, который должен быть обработан приложением-обработчиком прокси.</span><span class="sxs-lookup"><span data-stu-id="bbba4-111">Pointer to a [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) structure containing the request to be processed by the proxy handler application.</span></span>

</dd> <dt>

<span data-ttu-id="bbba4-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="bbba4-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="bbba4-113">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="bbba4-113">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="bbba4-114">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="bbba4-114">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="bbba4-115">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="bbba4-115">Reserved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bbba4-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bbba4-116">Return value</span></span>

<span data-ttu-id="bbba4-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="bbba4-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbba4-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bbba4-118">Remarks</span></span>

<span data-ttu-id="bbba4-119">Сообщение **Line \_ проксирекуест** отправляется только первому приложению, зарегистрированному для обработки запросов прокси-сервера типа, для которого выполняется доставка.</span><span class="sxs-lookup"><span data-stu-id="bbba4-119">The **LINE\_PROXYREQUEST** message is sent only to the first application that registered to handle proxy requests of the type being delivered.</span></span>

<span data-ttu-id="bbba4-120">Приложение должно обработать запрос, содержащийся в буфере прокси, и вызвать [**линепроксиреспонсе**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) для возврата данных или доставки результатов.</span><span class="sxs-lookup"><span data-stu-id="bbba4-120">The application should process the request contained in the proxy buffer and call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) to return data or deliver results.</span></span> <span data-ttu-id="bbba4-121">Обработка запроса должна выполняться в контексте функции обратного вызова TAPI приложения, только если ее можно выполнить немедленно, не дожидаясь ответа от любой другой сущности.</span><span class="sxs-lookup"><span data-stu-id="bbba4-121">Processing of the request should be done within the context of the application's TAPI callback function only if it can be performed immediately, without waiting for response from any other entity.</span></span> <span data-ttu-id="bbba4-122">Если приложению требуется взаимодействовать с другими сущностями (например, поставщик услуг для работы с ACD на основе УАТС или любая другая системная служба, которая может привести к блокировке), запрос должен быть помещен в приложение и функция обратного вызова завершается, чтобы избежать задержки получения дополнительных сообщений TAPI приложением.</span><span class="sxs-lookup"><span data-stu-id="bbba4-122">If the application needs to communicate with other entities (for example, a service provider to handle PBX-based ACD, or any other system service which might result in blocking), then the request should be queued within the application and the callback function exited to avoid delaying the receipt of further TAPI messages by the application.</span></span>

<span data-ttu-id="bbba4-123">В момент доставки **строки \_ проксирекуест** в обработчик прокси-сервера, TAPI уже вернул положительный результат функции *дврекуестид* в исходное приложение и разблокировал вызывающий поток для продолжения выполнения.</span><span class="sxs-lookup"><span data-stu-id="bbba4-123">At the time the **LINE\_PROXYREQUEST** is delivered to the proxy handler, TAPI has already returned a positive *dwRequestID* function result to the original application and unblocked the calling thread to continue execution.</span></span> <span data-ttu-id="bbba4-124">Приложение ожидает сообщение [**\_ ответа строки**](line-reply.md) , которое автоматически создается, когда приложение обработчика прокси-сервера вызывает [**линепроксиреспонсе**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="bbba4-124">The application is awaiting a [**LINE\_REPLY**](line-reply.md) message, which is automatically generated when the proxy handler application calls [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span>

<span data-ttu-id="bbba4-125">Приложение не должно освобождать память, на которую указывает *лппроксирекуест*.</span><span class="sxs-lookup"><span data-stu-id="bbba4-125">The application shall not free the memory pointed to by *lpProxyRequest*.</span></span> <span data-ttu-id="bbba4-126">TAPI освобождает память во время выполнения [**линепроксиреспонсе**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span><span class="sxs-lookup"><span data-stu-id="bbba4-126">TAPI frees the memory during the execution of [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).</span></span> <span data-ttu-id="bbba4-127">Приложение может вызвать [**линепроксиреспонсе**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) ровно один раз для каждого **сообщения \_ проксирекуест строки** .</span><span class="sxs-lookup"><span data-stu-id="bbba4-127">The application can call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactly once for each **LINE\_PROXYREQUEST** message.</span></span>

<span data-ttu-id="bbba4-128">Если приложение получает сообщение о [**\_ закрытии строки**](line-close.md) при наличии ожидающих запросов прокси-сервера, оно должно вызывать [**линепроксиреспонсе**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) для каждого ожидающего запроса, передавая ему соответствующее значение *двресулт* (например, линирр \_ оператионфаилед).</span><span class="sxs-lookup"><span data-stu-id="bbba4-128">If the application receives a [**LINE\_CLOSE**](line-close.md) message while it has pending proxy requests, it should call [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) for each pending request, passing in an appropriate *dwResult* value (such as LINEERR\_OPERATIONFAILED).</span></span>

## <a name="requirements"></a><span data-ttu-id="bbba4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="bbba4-129">Requirements</span></span>



| <span data-ttu-id="bbba4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="bbba4-130">Requirement</span></span> | <span data-ttu-id="bbba4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="bbba4-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="bbba4-132">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="bbba4-132">TAPI version</span></span><br/> | <span data-ttu-id="bbba4-133">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="bbba4-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="bbba4-134">Header</span><span class="sxs-lookup"><span data-stu-id="bbba4-134">Header</span></span><br/>       | <dl> <span data-ttu-id="bbba4-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="bbba4-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bbba4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bbba4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbba4-137">**\_закрыть строку**</span><span class="sxs-lookup"><span data-stu-id="bbba4-137">**LINE\_CLOSE**</span></span>](line-close.md)
</dt> <dt>

[<span data-ttu-id="bbba4-138">**\_ответ строки**</span><span class="sxs-lookup"><span data-stu-id="bbba4-138">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="bbba4-139">**линепроксирекуест**</span><span class="sxs-lookup"><span data-stu-id="bbba4-139">**LINEPROXYREQUEST**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[<span data-ttu-id="bbba4-140">**линепроксиреспонсе**</span><span class="sxs-lookup"><span data-stu-id="bbba4-140">**lineProxyResponse**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




