---
description: Асинхронные методы обратного вызова
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Асинхронные методы обратного вызова
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701335"
---
# <a name="asynchronous-callback-methods"></a><span data-ttu-id="6a858-103">Асинхронные методы обратного вызова</span><span class="sxs-lookup"><span data-stu-id="6a858-103">Asynchronous Callback Methods</span></span>

<span data-ttu-id="6a858-104">Media Foundation предоставляет единообразный способ реализации асинхронных методов с помощью интерфейса обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="6a858-104">Media Foundation provides a consistent way to implement asynchronous methods, using a callback interface.</span></span>

<span data-ttu-id="6a858-105">В этом разделе описывается реализация интерфейса обратного вызова и написание асинхронных методов, использующих этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6a858-105">This section describes how to implement the callback interface and how to write asynchronous methods that use this interface.</span></span> <span data-ttu-id="6a858-106">Он содержит следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="6a858-106">It contains the following topics.</span></span>



| <span data-ttu-id="6a858-107">Раздел</span><span class="sxs-lookup"><span data-stu-id="6a858-107">Topic</span></span>                                                                                | <span data-ttu-id="6a858-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6a858-108">Description</span></span>                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6a858-109">Вызов асинхронных методов</span><span class="sxs-lookup"><span data-stu-id="6a858-109">Calling Asynchronous Methods</span></span>](calling-asynchronous-methods.md)                     | <span data-ttu-id="6a858-110">Как вызывать асинхронные методы в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a858-110">How to call asynchronous methods in Media Foundation.</span></span>                                               |
| [<span data-ttu-id="6a858-111">Реализация асинхронного обратного вызова</span><span class="sxs-lookup"><span data-stu-id="6a858-111">Implementing the Asynchronous Callback</span></span>](implementing-the-asynchronous-callback.md) | <span data-ttu-id="6a858-112">Реализация метода обратного вызова в интерфейсе [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="6a858-112">How to implement the callback method in the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> |
| [<span data-ttu-id="6a858-113">Поддержка нескольких обратных вызовов</span><span class="sxs-lookup"><span data-stu-id="6a858-113">Supporting Multiple Callbacks</span></span>](supporting-multiple-callbacks.md)                   | <span data-ttu-id="6a858-114">Поддержка нескольких обратных вызовов в одном и том же классе C++.</span><span class="sxs-lookup"><span data-stu-id="6a858-114">How to support multiple callbacks within the same C++ class.</span></span>                                        |
| [<span data-ttu-id="6a858-115">Рабочие очереди</span><span class="sxs-lookup"><span data-stu-id="6a858-115">Work Queues</span></span>](work-queues.md)                                                       | <span data-ttu-id="6a858-116">Рабочие очереди предоставляют эффективный способ выполнения асинхронных операций в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="6a858-116">Work queues provide an efficient way to perform asynchronous operations on another thread.</span></span>          |
| [<span data-ttu-id="6a858-117">Создание асинхронного метода</span><span class="sxs-lookup"><span data-stu-id="6a858-117">Writing an Asynchronous Method</span></span>](writing-an-asynchronous-method.md)                 | <span data-ttu-id="6a858-118">Реализация асинхронных методов в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="6a858-118">How to implement asynchronous methods in Media Foundation.</span></span>                                          |
| [<span data-ttu-id="6a858-119">Пользовательские объекты асинхронных результатов</span><span class="sxs-lookup"><span data-stu-id="6a858-119">Custom Asynchronous Result Objects</span></span>](custom-asynchronous-result-objects.md)         | <span data-ttu-id="6a858-120">Как предоставить пользовательскую реализацию интерфейса [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="6a858-120">How to provide a custom implementation of the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="6a858-121">См. также</span><span class="sxs-lookup"><span data-stu-id="6a858-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a858-122">**Интерфейс Имфасинккаллбакк**</span><span class="sxs-lookup"><span data-stu-id="6a858-122">**IMFAsyncCallback Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[<span data-ttu-id="6a858-123">**Интерфейс Имфасинкресулт**</span><span class="sxs-lookup"><span data-stu-id="6a858-123">**IMFAsyncResult Interface**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[<span data-ttu-id="6a858-124">Media Foundation API платформы</span><span class="sxs-lookup"><span data-stu-id="6a858-124">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



