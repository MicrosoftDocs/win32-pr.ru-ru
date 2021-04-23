---
title: Обработка запросов
description: Обработка запросов включает в себя четыре шага.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "103913964"
---
# <a name="processing-requests"></a><span data-ttu-id="a7647-103">Обработка запросов</span><span class="sxs-lookup"><span data-stu-id="a7647-103">Processing Requests</span></span>

<span data-ttu-id="a7647-104">Обработка запросов включает в себя четыре шага:</span><span class="sxs-lookup"><span data-stu-id="a7647-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="a7647-105">Получение запроса</span><span class="sxs-lookup"><span data-stu-id="a7647-105">Receiving a request</span></span>
-   <span data-ttu-id="a7647-106">Обработка запроса</span><span class="sxs-lookup"><span data-stu-id="a7647-106">Handling the request</span></span>
-   <span data-ttu-id="a7647-107">Отправка ответа</span><span class="sxs-lookup"><span data-stu-id="a7647-107">Sending the response</span></span>
-   <span data-ttu-id="a7647-108">Отмена запросов, которые не могут быть обработаны</span><span class="sxs-lookup"><span data-stu-id="a7647-108">Canceling requests that cannot be processed</span></span>

![Схема, на которой показан цикл обработки запросов.](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="a7647-110">Получение запроса</span><span class="sxs-lookup"><span data-stu-id="a7647-110">Receiving a Request</span></span>

<span data-ttu-id="a7647-111">API сервера HTTP предоставляет структуру запросов для хранения проанализированного входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="a7647-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="a7647-112">Эта структура выделяется приложением и инициализируется при получении входящего запроса.</span><span class="sxs-lookup"><span data-stu-id="a7647-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="a7647-113">Приложение вызывает функцию [**хттпрецеивехттпрекуест**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) для получения запроса.</span><span class="sxs-lookup"><span data-stu-id="a7647-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="a7647-114">Если буфер запроса слишком мал для получения запроса, приложение может увеличить размер буфера и вызвать **хттпрецеивехттпрекуест** еще раз, чтобы получить весь запрос.</span><span class="sxs-lookup"><span data-stu-id="a7647-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="a7647-115">Если запрос содержит данные тела сущности для получения, приложения вызывают [**хттпрецеиверекуестентитибоди**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) с идентификатором запроса, возвращенным в параметре *прекуестбуффер* во время вызова [**хттпрецеивехттпрекуест**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span><span class="sxs-lookup"><span data-stu-id="a7647-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="a7647-116">Обработка запроса</span><span class="sxs-lookup"><span data-stu-id="a7647-116">Handling the Request</span></span>

<span data-ttu-id="a7647-117">Приложение выполняет обработку запроса в зависимости от конкретного приложения и формирует ответ.</span><span class="sxs-lookup"><span data-stu-id="a7647-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="a7647-118">API сервера HTTP не накладывает время ожидания для этого процесса.</span><span class="sxs-lookup"><span data-stu-id="a7647-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="a7647-119">Отправка ответа</span><span class="sxs-lookup"><span data-stu-id="a7647-119">Sending the Response</span></span>

<span data-ttu-id="a7647-120">Когда приложение завершает обработку запроса и составления ответ, он вызывает функцию [**хттпсендхттпреспонсе**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) для отправки ответа.</span><span class="sxs-lookup"><span data-stu-id="a7647-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="a7647-121">Если ответ содержит данные тела сущности для отправки, приложение также вызывает [хттпсендреспонсинтитибоди](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span><span class="sxs-lookup"><span data-stu-id="a7647-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="a7647-122">Отмена запросов</span><span class="sxs-lookup"><span data-stu-id="a7647-122">Canceling Requests</span></span>

<span data-ttu-id="a7647-123">После того как приложение получило идентификатор запроса от его вызова к [**хттпрецеивехттпрекуест**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), он может в любое время отменить запрос, вызвав [хттпканцелхттпрекуест](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span><span class="sxs-lookup"><span data-stu-id="a7647-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




