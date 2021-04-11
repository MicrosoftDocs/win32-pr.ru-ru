---
description: ТСПИ включает ряд операций, которые начинают время существования маркера вызова.
ms.assetid: 28e171a3-db47-40fd-9c5a-d7b76d834a99
title: Асинхронные ответы и события для новых дескрипторов вызовов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02511a083c318afb227e3e172191d3ab84a69fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911220"
---
# <a name="async-replies-versus-events-on-new-call-handles"></a><span data-ttu-id="98491-103">Асинхронные ответы и события для новых дескрипторов вызовов</span><span class="sxs-lookup"><span data-stu-id="98491-103">Async Replies versus Events on New Call Handles</span></span>

<span data-ttu-id="98491-104">ТСПИ включает ряд операций, которые начинают время существования маркера вызова.</span><span class="sxs-lookup"><span data-stu-id="98491-104">TSPI includes a number of operations that start the lifetime of a call handle.</span></span> <span data-ttu-id="98491-105">Если поставщик услуг возвращает результат для такой операции, он должен заполнить непрозрачный маркер типа **хдрвкалл**, который используется для нового вызова перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="98491-105">If the service provider returns SUCCESS for such an operation, it must fill in the opaque handle of type **HDRVCALL**, which it uses for the new call before it returns.</span></span> <span data-ttu-id="98491-106">TAPI никогда не выполняет операции с вызовом до получения [*соответствующей \_ процедуры завершения*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="98491-106">TAPI never performs operations on the call before the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) has been received.</span></span> <span data-ttu-id="98491-107">Если поставщик услуг возвращает ошибку, этот маркер автоматически становится недопустимым (т. е. без [**тспи \_ линеклосекалл**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span><span class="sxs-lookup"><span data-stu-id="98491-107">If the service provider returns FAILURE, the handle automatically becomes invalid (that is, without [**TSPI\_lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)).</span></span> <span data-ttu-id="98491-108">По сути, TAPI обрабатывает этот обработчик как "пока не допустим" до асинхронного завершения.</span><span class="sxs-lookup"><span data-stu-id="98491-108">In effect, TAPI treats the handle as "not yet valid" until the asynchronous completion.</span></span>

<span data-ttu-id="98491-109">Поставщик услуг также должен рассматривать этот обработчик как "еще не действителен" до тех пор, пока не будет получена соответствующая [*\_ процедура завершения*](/windows/win32/api/tspi/nc-tspi-async_completion) .</span><span class="sxs-lookup"><span data-stu-id="98491-109">The service provider must also treat the handle as "not yet valid" until after the matching [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) is received.</span></span> <span data-ttu-id="98491-110">Иными словами, он не должен выдавать никаких функций для [*\_ событий строк*](/windows/win32/api/tspi/nc-tspi-lineevent) для нового вызова или включать его в число вызовов в сообщениях или структурах данных состояния для строки.</span><span class="sxs-lookup"><span data-stu-id="98491-110">In other words, it must not issue any [*Line\_Event*](/windows/win32/api/tspi/nc-tspi-lineevent) functions for the new call or include it in call counts in messages or status data structures for the line.</span></span>

<span data-ttu-id="98491-111">Уровень TAPI также соответствует этим ограничениям жизненного цикла; новый маркер вызова не возвращается или является допустимым до соответствующего сообщения [**\_ ответа строки**](./line-reply.md) , и никакие события для нового вызова не доставляются приложению до тех пор, пока не будет отправлено \_ сообщение с ответом строки.</span><span class="sxs-lookup"><span data-stu-id="98491-111">The TAPI level also conforms to these life cycle restrictions; a new call handle is not returned or valid until the matching [**LINE\_REPLY**](./line-reply.md) message, and no events for the new call are delivered to the application until after the LINE\_REPLY message.</span></span>

<span data-ttu-id="98491-112">Ниже перечислены операции ТСПИ, к которым применяется принцип "время жизни запуска".</span><span class="sxs-lookup"><span data-stu-id="98491-112">The TSPI operations to which this "start lifetime" principle applies are the following:</span></span>

-   [<span data-ttu-id="98491-113">**ТСПИ \_ линекомплететрансфер**</span><span class="sxs-lookup"><span data-stu-id="98491-113">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="98491-114">**ТСПИ \_ линефорвард**</span><span class="sxs-lookup"><span data-stu-id="98491-114">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="98491-115">**ТСПИ \_ линемакекалл**</span><span class="sxs-lookup"><span data-stu-id="98491-115">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="98491-116">**ТСПИ \_ линепиккуп**</span><span class="sxs-lookup"><span data-stu-id="98491-116">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="98491-117">**ТСПИ \_ линепрепареаддтоконференце**</span><span class="sxs-lookup"><span data-stu-id="98491-117">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="98491-118">**ТСПИ \_ линесетупконференце**</span><span class="sxs-lookup"><span data-stu-id="98491-118">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="98491-119">**ТСПИ \_ линесетуптрансфер**</span><span class="sxs-lookup"><span data-stu-id="98491-119">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="98491-120">**ТСПИ \_ линеунпарк**</span><span class="sxs-lookup"><span data-stu-id="98491-120">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
