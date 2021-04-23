---
description: Будущие улучшения примера кода приложения Winsock.
ms.assetid: 317baa53-6bc8-42bd-8f56-480cab29ae6b
title: Будущие улучшения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 938f38334a4bbe392e83efc0be12905fb7ae66a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701523"
---
# <a name="future-improvements"></a><span data-ttu-id="6e4d9-103">Будущие улучшения</span><span class="sxs-lookup"><span data-stu-id="6e4d9-103">Future Improvements</span></span>

<span data-ttu-id="6e4d9-104">В этом приложении можно внести несколько усовершенствований, например:</span><span class="sxs-lookup"><span data-stu-id="6e4d9-104">There are several improvements that can be made to this application, such as:</span></span>

-   <span data-ttu-id="6e4d9-105">Приложение может создать одно постоянное подключение.</span><span class="sxs-lookup"><span data-stu-id="6e4d9-105">A single, persistent connection could be created by the application.</span></span> <span data-ttu-id="6e4d9-106">Необходимо добавить соответствующую обработку ошибок.</span><span class="sxs-lookup"><span data-stu-id="6e4d9-106">Appropriate error handling would have to be added.</span></span> <span data-ttu-id="6e4d9-107">Это снизит затраты, связанные с запуском и уничтожением подключения.</span><span class="sxs-lookup"><span data-stu-id="6e4d9-107">This would reduce the overhead associated with connection startup and teardown.</span></span>
-   <span data-ttu-id="6e4d9-108">Код ответа на сервере можно оптимизировать для консолидации ответов, уменьшая количество пакетов, отправленных с сервера.</span><span class="sxs-lookup"><span data-stu-id="6e4d9-108">The reply code on the server could be optimized to consolidate replies, reducing the number of packets sent from the server.</span></span>
-   <span data-ttu-id="6e4d9-109">Можно вносить улучшения в протокол.</span><span class="sxs-lookup"><span data-stu-id="6e4d9-109">Improvements in the protocol could be made.</span></span> <span data-ttu-id="6e4d9-110">Например, можно использовать битовую маску обновления, чтобы указать, какие ячейки должны быть обновлены, и только отправленные данные ячейки.</span><span class="sxs-lookup"><span data-stu-id="6e4d9-110">For example, an update bitmask could be used to signify which cells are to be updated, and only that cell data sent.</span></span>
-   <span data-ttu-id="6e4d9-111">Обновления могут быть перекрывающиеся с помощью разных потоков, чтобы сеть не проходила во время работы функции **компутенекст** .</span><span class="sxs-lookup"><span data-stu-id="6e4d9-111">Updates could be overlapped using different threads, so that the network is not idle while the **ComputeNext** function is running.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6e4d9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6e4d9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e4d9-113">Повышение скорости работы приложения</span><span class="sxs-lookup"><span data-stu-id="6e4d9-113">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="6e4d9-114">Базовая версия: очень плохо выполняемое приложение</span><span class="sxs-lookup"><span data-stu-id="6e4d9-114">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="6e4d9-115">Редакция 1. Очистка очевидных</span><span class="sxs-lookup"><span data-stu-id="6e4d9-115">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="6e4d9-116">Редакция 2. перепроектирование для уменьшения количества подключений</span><span class="sxs-lookup"><span data-stu-id="6e4d9-116">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="6e4d9-117">Редакция 3: отправка сжатого блока</span><span class="sxs-lookup"><span data-stu-id="6e4d9-117">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> </dl>

 

 



