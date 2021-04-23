---
description: Базовая версия очень плохо выполняемого приложения в сокетах Windows (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Базовая версия: очень плохо выполняемое приложение'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702387"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="6f5e9-103">Базовая версия: очень плохо выполняемое приложение</span><span class="sxs-lookup"><span data-stu-id="6f5e9-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="6f5e9-104">Исходный, неудовлетворительный пример кода, используемый для вычисления обновлений, выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6f5e9-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="6f5e9-105">Для простоты в следующих примерах нет обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="6f5e9-106">Любое рабочее приложение всегда проверяет возвращаемые значения.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="6f5e9-107">Первые несколько примеров приложения обеспечивают намеренно низкую производительность, чтобы продемонстрировать улучшения производительности, внесенные в код.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="6f5e9-108">Не используйте эти примеры кода в приложении. они предназначены только для иллюстрации.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="6f5e9-109">В этом состоянии приложение имеет наихудшую возможную производительность сети.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="6f5e9-110">Ниже перечислены проблемы с этой версией примера приложения.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="6f5e9-111">Приложение находится в чате.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-111">The application is chatty.</span></span> <span data-ttu-id="6f5e9-112">Каждая транзакция слишком мала — ячейки не нужно обновлять по одной.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="6f5e9-113">Транзакции строго сериализуются, несмотря на то, что ячейки могут обновляться параллельно.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="6f5e9-114">Буфер отправки имеет нулевое значение, и в приложении возникает задержка 200-миллисекунда для каждой отправки — три раза на ячейку.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="6f5e9-115">Приложение очень активно подключается, подключаясь к каждой ячейке один раз.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="6f5e9-116">Приложения ограничены числом подключений в секунду для данного назначения из-за состояния ожидания, но это не является проблемой, так как каждая транзакция занимает более 600 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="6f5e9-117">Приложение является файловой системой FAT; Многие транзакции не влияют на состояние сервера, так как многие ячейки не изменяются с обновления на обновление.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="6f5e9-118">Приложение имеет низкую потоковую передачу; небольшие отправки потребляют много ресурсов ЦП и ОЗУ.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="6f5e9-119">В приложении предполагается, что для отправки используется представление с прямым порядком байтов.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="6f5e9-120">Это естественное предположение для текущей платформы Windows, но может быть опасно для долгосрочного кода.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="6f5e9-121">Ключевые метрики производительности</span><span class="sxs-lookup"><span data-stu-id="6f5e9-121">Key Performance Metrics</span></span>

<span data-ttu-id="6f5e9-122">Следующие метрики производительности выражаются в времени кругового пути (RTT), Гудпут и служебных издержках.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="6f5e9-123">Описание этих терминов см. в разделе [терминология сети](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="6f5e9-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="6f5e9-124">Время ячейки, сетевое время для одного обновления ячейки требует 4 \* RTT + 600 мс для взаимодействия Nagle и отложенного подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="6f5e9-125">Гудпут меньше 6 байт.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="6f5e9-126">Дополнительная нагрузка на протокол составляет 99,6%.</span><span class="sxs-lookup"><span data-stu-id="6f5e9-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f5e9-127">См. также</span><span class="sxs-lookup"><span data-stu-id="6f5e9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f5e9-128">Повышение скорости работы приложения</span><span class="sxs-lookup"><span data-stu-id="6f5e9-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="6f5e9-129">Терминология сети</span><span class="sxs-lookup"><span data-stu-id="6f5e9-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="6f5e9-130">Редакция 1. Очистка очевидных</span><span class="sxs-lookup"><span data-stu-id="6f5e9-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="6f5e9-131">Редакция 2. перепроектирование для уменьшения количества подключений</span><span class="sxs-lookup"><span data-stu-id="6f5e9-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="6f5e9-132">Редакция 3: отправка сжатого блока</span><span class="sxs-lookup"><span data-stu-id="6f5e9-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="6f5e9-133">Будущие улучшения</span><span class="sxs-lookup"><span data-stu-id="6f5e9-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



