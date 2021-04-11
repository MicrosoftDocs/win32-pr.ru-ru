---
description: В этой редакции пример приложения перерабатывается для устранения ненужных подключений.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: Редакция 2. перепроектирование для уменьшения числа подключений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155874"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="60b8f-103">Редакция 2. перепроектирование для уменьшения числа подключений</span><span class="sxs-lookup"><span data-stu-id="60b8f-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="60b8f-104">В этой редакции пример приложения перерабатывается для устранения ненужных подключений.</span><span class="sxs-lookup"><span data-stu-id="60b8f-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="60b8f-105">Эти примеры приложений также обеспечивают намеренно низкую производительность, чтобы продемонстрировать улучшения производительности, внесенные в код.</span><span class="sxs-lookup"><span data-stu-id="60b8f-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="60b8f-106">Не используйте этот пример кода в приложении. Он предназначен только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="60b8f-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="60b8f-107">Оставшиеся проблемы</span><span class="sxs-lookup"><span data-stu-id="60b8f-107">Remaining Problems</span></span>

<span data-ttu-id="60b8f-108">Изменения в редакции два переизменили приложение, чтобы установить только одно подключение для каждого обновления.</span><span class="sxs-lookup"><span data-stu-id="60b8f-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="60b8f-109">Приложение по-прежнему включает следующие проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="60b8f-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="60b8f-110">Приложение по-прежнему сериализуется и передается в чате.</span><span class="sxs-lookup"><span data-stu-id="60b8f-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="60b8f-111">Приложение по-прежнему имеет структуру FAT; Существует много операций отправки, которые не нуждаются в операции в этом проекте.</span><span class="sxs-lookup"><span data-stu-id="60b8f-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="60b8f-112">Отправка по-прежнему составляет всего 3 байта, что снижает скорость потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="60b8f-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="60b8f-113">Ключевые метрики производительности</span><span class="sxs-lookup"><span data-stu-id="60b8f-113">Key Performance Metrics</span></span>

<span data-ttu-id="60b8f-114">Следующие метрики производительности выражаются в времени кругового пути (RTT), Гудпут и служебных издержках.</span><span class="sxs-lookup"><span data-stu-id="60b8f-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="60b8f-115">Описание этих терминов см. в разделе [терминология сети](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="60b8f-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="60b8f-116">Эта версия отражает следующие метрики производительности.</span><span class="sxs-lookup"><span data-stu-id="60b8f-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="60b8f-117">Время ячейки — 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="60b8f-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="60b8f-118">Гудпут — 4 байта/RTT</span><span class="sxs-lookup"><span data-stu-id="60b8f-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="60b8f-119">Дополнительная нагрузка на протоколы — 96,8%</span><span class="sxs-lookup"><span data-stu-id="60b8f-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="60b8f-120">См. также</span><span class="sxs-lookup"><span data-stu-id="60b8f-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60b8f-121">Повышение скорости работы приложения</span><span class="sxs-lookup"><span data-stu-id="60b8f-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="60b8f-122">Терминология сети</span><span class="sxs-lookup"><span data-stu-id="60b8f-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="60b8f-123">Базовая версия: очень плохо выполняемое приложение</span><span class="sxs-lookup"><span data-stu-id="60b8f-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="60b8f-124">Редакция 1. Очистка очевидных</span><span class="sxs-lookup"><span data-stu-id="60b8f-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="60b8f-125">Редакция 3: отправка сжатого блока</span><span class="sxs-lookup"><span data-stu-id="60b8f-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="60b8f-126">Будущие улучшения</span><span class="sxs-lookup"><span data-stu-id="60b8f-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



