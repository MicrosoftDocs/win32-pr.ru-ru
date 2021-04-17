---
title: Отмена вызова
description: Уведомление об отмене вызова отменяет операцию операций серверной службы и обратных вызовов модели служб.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Вызов веб-служб отмены вызовов для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "105691714"
---
# <a name="call-cancellation"></a><span data-ttu-id="0807e-106">Отмена вызова</span><span class="sxs-lookup"><span data-stu-id="0807e-106">Call cancellation</span></span>

<span data-ttu-id="0807e-107">Уведомление об отмене вызова отменяет операцию [операций серверной службы](server-side-service-operations.md) и обратных вызовов модели служб.</span><span class="sxs-lookup"><span data-stu-id="0807e-107">Call cancellation notification cancels the operation of [server side service operations](server-side-service-operations.md) and service-model callbacks.</span></span> <span data-ttu-id="0807e-108">Такая отмена может быть вызвана одной из двух причин:</span><span class="sxs-lookup"><span data-stu-id="0807e-108">Such cancellation can be for one of two reasons:</span></span>

-   <span data-ttu-id="0807e-109">Узел службы остановил операции из-за вызова функции [**всабортсервицехост**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .</span><span class="sxs-lookup"><span data-stu-id="0807e-109">The service host has stopped operations because of a call to the [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) function.</span></span>
-   <span data-ttu-id="0807e-110">Базовый канал вызвал ошибку.</span><span class="sxs-lookup"><span data-stu-id="0807e-110">The underlying channel has raised a fault.</span></span>


<span data-ttu-id="0807e-111">Чтобы получить уведомление об отмене, операция службы или обратный вызов модели службы должны зарегистрировать обратный [**вызов \_ \_ \_ обратного вызова операции WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) , вызвав функцию [**всрегистероператионфорканцел**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) .</span><span class="sxs-lookup"><span data-stu-id="0807e-111">To receive a cancellation notification, the service operation or service-model callback must register a [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback by calling the [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) function.</span></span>

<span data-ttu-id="0807e-112">При необходимости в ходе регистрации уведомления об отмене операция службы или обратный вызов модели службы также могут регистрировать данные о состоянии конкретного приложения и обратный вызов [**\_ \_ \_ \_ обратного вызова свободного состояния WS Operation**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .</span><span class="sxs-lookup"><span data-stu-id="0807e-112">Optionally, as part of the registering for cancellation notification, the service operation or service-model callback can also register application-specific state data and the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback.</span></span>

<span data-ttu-id="0807e-113">Данные о состоянии становятся доступными обратному вызову [**\_ \_ функции отмены \_ обратного вызова операции WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) .</span><span class="sxs-lookup"><span data-stu-id="0807e-113">The state data is made available to the [**WS\_OPERATION\_CANCEL\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) callback.</span></span> <span data-ttu-id="0807e-114">При завершении вызова вызывается обратный вызов [**\_ \_ \_ \_ обратного состояния операции WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) , чтобы дать приложению возможность освобождать данные о состоянии.</span><span class="sxs-lookup"><span data-stu-id="0807e-114">On call completion, the [**WS\_OPERATION\_FREE\_STATE\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) callback is called to give the application an opportunity to free the state data.</span></span>

<span data-ttu-id="0807e-115">Пример кода см. в разделе [блоккингсервицеексампле](blockingserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="0807e-115">For a code example, see [BlockingServiceExample](blockingserviceexample.md).</span></span>

<span data-ttu-id="0807e-116">Обратный вызов отмены вызывается только один раз в течение времени существования [операций серверной службы](server-side-service-operations.md) или функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0807e-116">The cancellation callback is called only once for the lifetime of the [server side service operations](server-side-service-operations.md) or callback function.</span></span>

<span data-ttu-id="0807e-117">Отмена вызова доступна для всех обратных вызовов узла службы, которые принимают [ \_ \_ контекст WS Operation](ws-operation-context.md) в качестве параметра.</span><span class="sxs-lookup"><span data-stu-id="0807e-117">Call cancellation is available in for all service host callbacks that take [WS\_OPERATION\_CONTEXT](ws-operation-context.md) as a parameter.</span></span>

<span data-ttu-id="0807e-118">Следующие элементы API связаны с отменой вызовов.</span><span class="sxs-lookup"><span data-stu-id="0807e-118">The following API elements relate to call cancellation.</span></span>

| <span data-ttu-id="0807e-119">Обратный вызов</span><span class="sxs-lookup"><span data-stu-id="0807e-119">Callback</span></span>                                                                         | <span data-ttu-id="0807e-120">Описание</span><span class="sxs-lookup"><span data-stu-id="0807e-120">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0807e-121">**\_ \_ обратный вызов операции WS Cancel \_**</span><span class="sxs-lookup"><span data-stu-id="0807e-121">**WS\_OPERATION\_CANCEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | <span data-ttu-id="0807e-122">Вызывается моделью службы для уведомления об отмене асинхронной операции службы в результате аварийного завершения работы узла службы.</span><span class="sxs-lookup"><span data-stu-id="0807e-122">Invoked by service model to notify a cancellation of an asynchronous service operation as a result of an aborted shutdown of service host.</span></span> |
| [<span data-ttu-id="0807e-123">**\_ \_ \_ обратный вызов свободного состояния WS Operation \_**</span><span class="sxs-lookup"><span data-stu-id="0807e-123">**WS\_OPERATION\_FREE\_STATE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | <span data-ttu-id="0807e-124">Вызывается моделью службы, чтобы разрешить приложению очищать данные состояния, зарегистрированные с помощью обратного вызова отмены.</span><span class="sxs-lookup"><span data-stu-id="0807e-124">Invoked by service model to allow an application to clean up state data that was registered with the cancellation callback.</span></span>                |



 



| <span data-ttu-id="0807e-125">Функция</span><span class="sxs-lookup"><span data-stu-id="0807e-125">Function</span></span>                                                             | <span data-ttu-id="0807e-126">Описание</span><span class="sxs-lookup"><span data-stu-id="0807e-126">Description</span></span>                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0807e-127">**всрегистероператионфорканцел**</span><span class="sxs-lookup"><span data-stu-id="0807e-127">**WsRegisterOperationForCancel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | <span data-ttu-id="0807e-128">Позволяет выполнить операцию службы или обратный вызов модели службы для регистрации уведомления об отмене.</span><span class="sxs-lookup"><span data-stu-id="0807e-128">Allows a service operation or service-model callback to register for a cancellation notification.</span></span> |



 

 

 




