---
description: '\_Тип данных DRV REQUESTID используется для предоставления уникального идентификатора для запроса поставщику услуг.'
ms.assetid: cef6a42a-2e40-4f65-8fab-79cfba143206
title: DRV_REQUESTID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9c0db093b06b263bcdc702ff14af7e308033f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683419"
---
# <a name="drv_requestid"></a><span data-ttu-id="9b58f-103">DRV \_ REQUESTID</span><span class="sxs-lookup"><span data-stu-id="9b58f-103">DRV\_REQUESTID</span></span>

<span data-ttu-id="9b58f-104">Тип данных **DRV \_ REQUESTID** используется для предоставления уникального идентификатора для запроса поставщику услуг.</span><span class="sxs-lookup"><span data-stu-id="9b58f-104">The **DRV\_REQUESTID** datatype is used to supply a unique identifier for a request to the service provider.</span></span> <span data-ttu-id="9b58f-105">Значение этого типа передается в качестве параметра каждой функции, которая разрешает асинхронную операцию.</span><span class="sxs-lookup"><span data-stu-id="9b58f-105">A value of this type is passed as a parameter to every function that allows for asynchronous operation.</span></span> <span data-ttu-id="9b58f-106">Если операция является асинхронной, поставщик услуг возвращает это значение в качестве возвращаемого значения функции.</span><span class="sxs-lookup"><span data-stu-id="9b58f-106">If the operation is asynchronous, the service provider returns this value as the return value of the function.</span></span> <span data-ttu-id="9b58f-107">Каждый раз, когда поставщик услуг помечает запрос как асинхронный таким образом, он должен в конечном итоге сообщить о завершении операции, вызвав функцию обратного вызова [*\_ процедуры завершения*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="9b58f-107">Whenever the service provider flags a request as asynchronous in this way, it must eventually report the operation is complete by calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function.</span></span>

<span data-ttu-id="9b58f-108">TAPI гарантирует, что предоставляемые им значения **DRV \_** являются строго положительными, то есть между значениями 0x00000001 и 0x7FFFFFFF включительно.</span><span class="sxs-lookup"><span data-stu-id="9b58f-108">TAPI ensures that the **DRV\_REQUESTID** values it supplies are strictly positive, that is, between the values of 0x00000001 and 0x7FFFFFFF, inclusive.</span></span> <span data-ttu-id="9b58f-109">Более того, значения являются уникальными в том случае, если значение не возвращено функцией для пометки запроса как асинхронное будет повторно использовано до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="9b58f-109">Furthermore, the values are unique in that no value returned from a function to flag the request as asynchronous will be re-used before the operation is reported complete.</span></span>

 

 
