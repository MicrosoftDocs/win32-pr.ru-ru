---
description: В этой версии примера программы были внесены несколько очевидных изменений, которые будут принимать первоначальный шаг при повышении производительности.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Редакция One: Очистка очевидных'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711773"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="89911-103">Редакция One: Очистка очевидных</span><span class="sxs-lookup"><span data-stu-id="89911-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="89911-104">В этой версии примера программы были внесены несколько очевидных изменений, которые будут принимать первоначальный шаг при повышении производительности.</span><span class="sxs-lookup"><span data-stu-id="89911-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="89911-105">Эта версия кода далеко не настроена на производительность, но это хороший добавочный шаг, позволяющий проанализировать влияние инкрементно лучших подходов.</span><span class="sxs-lookup"><span data-stu-id="89911-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="89911-106">Этот пример приложения обеспечивает намеренно низкую производительность, чтобы продемонстрировать улучшения производительности, внесенные в код.</span><span class="sxs-lookup"><span data-stu-id="89911-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="89911-107">Не используйте этот пример кода в приложении. Он предназначен только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="89911-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="89911-108">Изменения в этой версии</span><span class="sxs-lookup"><span data-stu-id="89911-108">Changes in this Version</span></span>

<span data-ttu-id="89911-109">Эта версия отражает следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="89911-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="89911-110">Удален СНДБУФ = 0.</span><span class="sxs-lookup"><span data-stu-id="89911-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="89911-111">Задержка 200 миллисекунд из-за небуферизованных отправлений и отложенных подтверждений удаляется.</span><span class="sxs-lookup"><span data-stu-id="89911-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="89911-112">Удалено поведение отправки и отправки.</span><span class="sxs-lookup"><span data-stu-id="89911-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="89911-113">Это изменение устраняет задержку в 200 мс из-за взаимодействий Nagle и отложенных ПОДТВЕРЖДЕНий.</span><span class="sxs-lookup"><span data-stu-id="89911-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="89911-114">Удалено предположение с прямым порядком следования.</span><span class="sxs-lookup"><span data-stu-id="89911-114">Removed little-endian assumption.</span></span> <span data-ttu-id="89911-115">Теперь байты находятся в порядке.</span><span class="sxs-lookup"><span data-stu-id="89911-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="89911-116">Оставшиеся проблемы</span><span class="sxs-lookup"><span data-stu-id="89911-116">Remaining Problems</span></span>

<span data-ttu-id="89911-117">В этой версии остаются следующие проблемы:</span><span class="sxs-lookup"><span data-stu-id="89911-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="89911-118">Приложение по-прежнему активно подключено.</span><span class="sxs-lookup"><span data-stu-id="89911-118">The application is still connect heavy.</span></span> <span data-ttu-id="89911-119">Так как задержка 600 + миллисекунд удаляется, приложение теперь обращается к 12 постоянно поддерживаемой скорости подключения в секунду.</span><span class="sxs-lookup"><span data-stu-id="89911-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="89911-120">Многие одновременные подключения теперь становятся проблемой.</span><span class="sxs-lookup"><span data-stu-id="89911-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="89911-121">Приложение по-прежнему имеет формат FAT; неизмененные ячейки по-прежнему распространяются на сервер.</span><span class="sxs-lookup"><span data-stu-id="89911-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="89911-122">Приложение по-прежнему имеет низкую потоковую передачу; 3-байтовые отправки по-прежнему небольшие отправляются.</span><span class="sxs-lookup"><span data-stu-id="89911-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="89911-123">Теперь приложение отправляет 2 байта/RTT, что равно 4 КБ/с при непосредственном соединении Ethernet.</span><span class="sxs-lookup"><span data-stu-id="89911-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="89911-124">Это не слишком быстро, но время ожидания может вызвать проблемы первыми.</span><span class="sxs-lookup"><span data-stu-id="89911-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="89911-125">Дополнительная нагрузка составляет до 99,3%, что по-прежнему не является хорошим процентом.</span><span class="sxs-lookup"><span data-stu-id="89911-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="89911-126">Ключевые метрики производительности</span><span class="sxs-lookup"><span data-stu-id="89911-126">Key Performance Metrics</span></span>

<span data-ttu-id="89911-127">Следующие ключевые метрики производительности выражаются во времени кругового пути (RTT), Гудпут и служебных издержках.</span><span class="sxs-lookup"><span data-stu-id="89911-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="89911-128">Описание этих терминов см. в разделе [терминология сети](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="89911-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="89911-129">Эта версия отражает следующие метрики производительности:</span><span class="sxs-lookup"><span data-stu-id="89911-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="89911-130">Время ячейки — 2 × RTT</span><span class="sxs-lookup"><span data-stu-id="89911-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="89911-131">Гудпут — 2 байта/RTT</span><span class="sxs-lookup"><span data-stu-id="89911-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="89911-132">Дополнительная нагрузка на протоколы — 99.3 процентов</span><span class="sxs-lookup"><span data-stu-id="89911-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="89911-133">См. также</span><span class="sxs-lookup"><span data-stu-id="89911-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89911-134">Повышение скорости работы приложения</span><span class="sxs-lookup"><span data-stu-id="89911-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="89911-135">Терминология сети</span><span class="sxs-lookup"><span data-stu-id="89911-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="89911-136">Базовая версия: очень плохо выполняемое приложение</span><span class="sxs-lookup"><span data-stu-id="89911-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="89911-137">Редакция 2. перепроектирование для уменьшения количества подключений</span><span class="sxs-lookup"><span data-stu-id="89911-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="89911-138">Редакция 3: отправка сжатого блока</span><span class="sxs-lookup"><span data-stu-id="89911-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="89911-139">Будущие улучшения</span><span class="sxs-lookup"><span data-stu-id="89911-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



