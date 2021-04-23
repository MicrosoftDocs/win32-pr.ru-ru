---
description: Класс Кмсгсреад обеспечивает поддержку для рабочего потока, в котором запросы могут быть отправлены асинхронно, а не напрямую.
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: Класс КМСГ
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662029"
---
# <a name="cmsg-class"></a><span data-ttu-id="c68fa-103">Класс КМСГ</span><span class="sxs-lookup"><span data-stu-id="c68fa-103">CMsg class</span></span>

<span data-ttu-id="c68fa-104">Класс [**кмсгсреад**](cmsgthread.md) обеспечивает поддержку для рабочего потока, в котором запросы могут быть отправлены асинхронно, а не напрямую.</span><span class="sxs-lookup"><span data-stu-id="c68fa-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="c68fa-105">Класс [**камсреад**](camthread.md) предоставляет рабочий поток, к которому могут отправляться отдельные запросы.</span><span class="sxs-lookup"><span data-stu-id="c68fa-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="c68fa-106">Только один клиент может выполнить запрос за раз, и клиент блокируется до тех пор, пока рабочий поток не завершит запрос.</span><span class="sxs-lookup"><span data-stu-id="c68fa-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="c68fa-107">В отличие от этого класс **кмсгсреад** предоставляет рабочий поток, в который может быть отправлено любое количество запросов.</span><span class="sxs-lookup"><span data-stu-id="c68fa-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="c68fa-108">Запросы (в форме объекта) помещаются `CMsg` в очередь и выполняются в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="c68fa-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="c68fa-109">Ответ или возвращаемое значение не получено.</span><span class="sxs-lookup"><span data-stu-id="c68fa-109">No reply or return value is received.</span></span>



| <span data-ttu-id="c68fa-110">Элементы данных</span><span class="sxs-lookup"><span data-stu-id="c68fa-110">Data Members</span></span>              | <span data-ttu-id="c68fa-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c68fa-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68fa-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="c68fa-112">dwFlags</span></span>                   | <span data-ttu-id="c68fa-113">Параметр Flag для кода запроса.</span><span class="sxs-lookup"><span data-stu-id="c68fa-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="c68fa-114">лппарам</span><span class="sxs-lookup"><span data-stu-id="c68fa-114">lpParam</span></span>                   | <span data-ttu-id="c68fa-115">Данные, необходимые рабочему потоку в качестве параметра или возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="c68fa-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="c68fa-116">Эти данные не должны основываться на стеке, так как на них будет ссылка в течение некоторого времени после завершения операции очереди.</span><span class="sxs-lookup"><span data-stu-id="c68fa-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="c68fa-117">певент</span><span class="sxs-lookup"><span data-stu-id="c68fa-117">pEvent</span></span>                    | <span data-ttu-id="c68fa-118">Объект события, который может сообщить рабочему потоку для указания на завершение операции.</span><span class="sxs-lookup"><span data-stu-id="c68fa-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="c68fa-119">Uiacp</span><span class="sxs-lookup"><span data-stu-id="c68fa-119">uMsg</span></span>                      | <span data-ttu-id="c68fa-120">Код запроса, определяемый клиентом класса потока и понятный переопределенной функцией рабочего потока.</span><span class="sxs-lookup"><span data-stu-id="c68fa-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="c68fa-121">Функции элементов</span><span class="sxs-lookup"><span data-stu-id="c68fa-121">Member Functions</span></span>          | <span data-ttu-id="c68fa-122">Описание</span><span class="sxs-lookup"><span data-stu-id="c68fa-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="c68fa-123">**кмсг**</span><span class="sxs-lookup"><span data-stu-id="c68fa-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="c68fa-124">Конструирует объект [**КМСГ**](cmsg-cmsg.md) .</span><span class="sxs-lookup"><span data-stu-id="c68fa-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



