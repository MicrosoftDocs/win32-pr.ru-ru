---
description: Помимо включения контроля цифр и получения уведомления о цифрах по одному, приложение может также запросить, чтобы в буфере собираются несколько цифр.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Сбор цифр
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673520"
---
# <a name="digit-gathering"></a><span data-ttu-id="1c3f7-103">Сбор цифр</span><span class="sxs-lookup"><span data-stu-id="1c3f7-103">Digit Gathering</span></span>

<span data-ttu-id="1c3f7-104">Помимо включения контроля цифр и получения уведомления о цифрах по одному, приложение может также запросить, чтобы в буфере собираются несколько цифр.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-104">Besides enabling digit monitoring and being notified of digits one at a time, an application can also request that multiple digits be collected in a buffer.</span></span> <span data-ttu-id="1c3f7-105">Приложение уведомляется только при заполнении буфера или при выполнении какого-либо другого условия завершения.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-105">Only when the buffer is full or when some other termination condition is met is the application notified.</span></span> <span data-ttu-id="1c3f7-106">Сбор цифр полезен для таких функций, как коллекция номеров кредитных карт.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-106">Digit gathering is useful for functions such as credit card number collection.</span></span> <span data-ttu-id="1c3f7-107">Он выполняется, когда приложение вызывает [**линегасердигитс**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), указывая буфер для заполнения цифрами.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-107">It is performed when an application calls [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), specifying a buffer to fill with digits.</span></span> <span data-ttu-id="1c3f7-108">Сбор цифр завершается, когда выполняется одно из следующих условий.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-108">Digit gathering terminates when one of the following conditions is true:</span></span>

-   <span data-ttu-id="1c3f7-109">Было собрано запрошенное количество цифр.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-109">The requested number of digits has been collected.</span></span>
-   <span data-ttu-id="1c3f7-110">Обнаружена одна из нескольких завершающих цифр.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-110">One of multiple termination digits is detected.</span></span> <span data-ttu-id="1c3f7-111">Цифры завершения задаются как [**линегасердигитс**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), а завершающая цифра также помещается в буфер.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-111">The termination digits are specified to [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), and the termination digit is placed in the buffer as well.</span></span>
-   <span data-ttu-id="1c3f7-112">Истекло одно из двух истечения времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-112">One of two timeouts expires.</span></span> <span data-ttu-id="1c3f7-113">Время ожидания — это первое время ожидания, определяющее максимальную продолжительность до того, как должна быть собрана первая цифра, и время ожидания между цифрами, с указанием максимальной длительности между последовательными цифрами.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-113">The timeouts are a first digit timeout, specifying the maximum duration before the first digit must be collected, and an inter-digit timeout, specifying the maximum duration between successive digits.</span></span>
-   <span data-ttu-id="1c3f7-114">Сбор цифр явным образом отменяется с помощью [**линегасердигитс**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) с другим набором параметров для запуска нового запроса на сбор данных или с помощью параметра буфера цифр **null** для отмены.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-114">Digit gathering is canceled explicitly by [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) again with either another set of parameters to start a new gathering request or by using a **NULL** digit buffer parameter to cancel.</span></span>

<span data-ttu-id="1c3f7-115">Когда по какой-либо причине сбор цифр завершается, в приложение, которое запросило сбор цифр, отправляется сообщение [**\_ гасердигитс**](line-gatherdigits.md) .</span><span class="sxs-lookup"><span data-stu-id="1c3f7-115">When digit gathering terminates for any reason, a [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is sent to the application that requested the digit gathering.</span></span> <span data-ttu-id="1c3f7-116">Однозначный запрос на сбор данных может быть выполнен в любой момент времени во всех приложениях, являющихся владельцами вызова.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-116">Only a single digit gathering request can be outstanding on a call at any given time across all applications that are owners of the call.</span></span>

<span data-ttu-id="1c3f7-117">Сбор цифр и отслеживание цифр можно включить одновременно для одного вызова.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-117">Digit gathering and digit monitoring can be enabled on the same call at the same time.</span></span> <span data-ttu-id="1c3f7-118">В этом случае приложение получит сообщение [**Line \_ монитордигитс**](line-monitordigits.md) для каждой обнаруженной цифры и \_ сообщение гасердигитс отдельной строки при обратной отправке буфера.</span><span class="sxs-lookup"><span data-stu-id="1c3f7-118">In that case, the application will receive a [**LINE\_MONITORDIGITS**](line-monitordigits.md) message for each detected digit and a separate LINE\_GATHERDIGITS message when the buffer is sent back.</span></span>

 

 



