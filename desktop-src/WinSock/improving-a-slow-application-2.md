---
description: В этом разделе рассматривается часть примера приложения, которая работает по сети очень медленно. В этом разделе вносятся изменения в исходный код, чтобы повысить его производительность.
ms.assetid: 29b96540-1b45-46b7-871a-e728aa50ad24
title: Повышение скорости работы приложения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae5bbec57791155852a41b1413e0d863f8704c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701516"
---
# <a name="improving-a-slow-application"></a><span data-ttu-id="0746b-104">Повышение скорости работы приложения</span><span class="sxs-lookup"><span data-stu-id="0746b-104">Improving a Slow Application</span></span>

<span data-ttu-id="0746b-105">В этом разделе рассматривается часть примера приложения, которая работает по сети очень медленно.</span><span class="sxs-lookup"><span data-stu-id="0746b-105">This section examines a portion of a sample application that operates over the network very slowly.</span></span> <span data-ttu-id="0746b-106">В этом разделе вносятся изменения в исходный код, чтобы повысить его производительность.</span><span class="sxs-lookup"><span data-stu-id="0746b-106">Throughout this section, modifications are made to the initial code to improve its performance.</span></span>

<span data-ttu-id="0746b-107">Пример макета — это обновленная часть игры «Life».</span><span class="sxs-lookup"><span data-stu-id="0746b-107">The mock sample is the updated portion for a game called Life.</span></span> <span data-ttu-id="0746b-108">Приложение записывается таким, что клиент выполняет вычисления для обновлений и отправляет их на сервер.</span><span class="sxs-lookup"><span data-stu-id="0746b-108">The application is written such that the client performs the calculations for the updates and sends them to the server.</span></span> <span data-ttu-id="0746b-109">Затем сервер отобразит итоговое поле срока службы.</span><span class="sxs-lookup"><span data-stu-id="0746b-109">The server then displays the resulting Life field.</span></span> <span data-ttu-id="0746b-110">Выходные данные клиента — это поток байтов, сгруппированных по трем (триады), каждому Triplet, представляющему одно обновление ячейки.</span><span class="sxs-lookup"><span data-stu-id="0746b-110">The output from the client is a stream of bytes, grouped in threes (triplets), each triplet representing one cell update.</span></span> <span data-ttu-id="0746b-111">Байты в Triplet представляют строку, столбец и значение, соответственно, для ячейки.</span><span class="sxs-lookup"><span data-stu-id="0746b-111">The bytes in the triplet represent the row, column, and value, respectively, for the cell.</span></span>

<span data-ttu-id="0746b-112">Этот пример начинается в качестве намеренно плохо выполняющегося приложения, предоставляющего базовые показатели, из которых можно проиллюстрировать улучшения производительности.</span><span class="sxs-lookup"><span data-stu-id="0746b-112">This sample begins as an intentionally poor performing application, which provides the baseline from which performance improvements can be illustrated.</span></span> <span data-ttu-id="0746b-113">После этого код повышеен в три раза, чтобы устранить различные проблемы, влияющие на производительность.</span><span class="sxs-lookup"><span data-stu-id="0746b-113">From there, the code is improved three times to address various issues that affect performance.</span></span> <span data-ttu-id="0746b-114">Эти примеры следует читать по порядку, так как каждая итерация улучшает предыдущую версию.</span><span class="sxs-lookup"><span data-stu-id="0746b-114">These samples should be read in order, as each iteration improves on the previous version.</span></span>

<span data-ttu-id="0746b-115">Базовый код и редакции, улучшающие этот код, следующие:</span><span class="sxs-lookup"><span data-stu-id="0746b-115">The baseline code, and the revisions that improve that code, are the following:</span></span>

-   [<span data-ttu-id="0746b-116">Базовая версия: очень плохо выполняемое приложение</span><span class="sxs-lookup"><span data-stu-id="0746b-116">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
-   [<span data-ttu-id="0746b-117">Редакция 1. Очистка очевидных</span><span class="sxs-lookup"><span data-stu-id="0746b-117">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
-   [<span data-ttu-id="0746b-118">Редакция 2. перепроектирование для уменьшения количества подключений</span><span class="sxs-lookup"><span data-stu-id="0746b-118">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
-   [<span data-ttu-id="0746b-119">Редакция 3: отправка сжатого блока</span><span class="sxs-lookup"><span data-stu-id="0746b-119">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
-   [<span data-ttu-id="0746b-120">Будущие улучшения</span><span class="sxs-lookup"><span data-stu-id="0746b-120">Future Improvements</span></span>](future-improvements-2.md)

> [!WARNING]
> <span data-ttu-id="0746b-121">Первые несколько примеров приложения обеспечивают намеренно низкую производительность, чтобы продемонстрировать улучшения производительности, внесенные в код.</span><span class="sxs-lookup"><span data-stu-id="0746b-121">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="0746b-122">Не используйте эти примеры кода в приложении. они предназначены только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="0746b-122">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0746b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0746b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0746b-124">Высокопроизводительные приложения Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="0746b-124">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



