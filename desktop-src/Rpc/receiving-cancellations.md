---
title: Получение отмен
description: Серверное приложение может вызвать Рпксервертестканцел с помощью обработчика привязки в вопросе, чтобы выяснить, запросил ли клиент отмену асинхронного вызова. \_ \_ Если Клиент отменил вызов, он вернет RPC S OK.
ms.assetid: ac7d7a50-a788-40a9-b57d-1f528bdbd7df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50b8b48ef2796dab071ac705edf0ffca5156e235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068343"
---
# <a name="receiving-cancellations"></a><span data-ttu-id="21308-104">Получение отмен</span><span class="sxs-lookup"><span data-stu-id="21308-104">Receiving Cancellations</span></span>

<span data-ttu-id="21308-105">Серверное приложение может вызвать [**рпксервертестканцел**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) с помощью обработчика привязки в вопросе, чтобы выяснить, запросил ли клиент отмену асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="21308-105">The server application can call [**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel) with the binding handle of the call in question to find out if the client has requested cancellation of the asynchronous call.</span></span> <span data-ttu-id="21308-106">\_ \_ Если Клиент отменил вызов, он вернет RPC S OK.</span><span class="sxs-lookup"><span data-stu-id="21308-106">It will return RPC\_S\_OK if the client canceled the call.</span></span>

 

 




