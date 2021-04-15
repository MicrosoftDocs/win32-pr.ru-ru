---
description: В этой версии приложения используется сжатый блок отправки данных. Это изменение приводит к значительному улучшению производительности.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: Редакция 3. сжатый блок отправки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702094"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="c8f95-104">Редакция 3. сжатый блок отправки</span><span class="sxs-lookup"><span data-stu-id="c8f95-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="c8f95-105">В этой версии приложения используется сжатый блок отправки данных.</span><span class="sxs-lookup"><span data-stu-id="c8f95-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="c8f95-106">Это изменение приводит к значительному улучшению производительности.</span><span class="sxs-lookup"><span data-stu-id="c8f95-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="c8f95-107">Изменения в этой версии</span><span class="sxs-lookup"><span data-stu-id="c8f95-107">Changes in this Version</span></span>

<span data-ttu-id="c8f95-108">Эта версия отражает следующие изменения:</span><span class="sxs-lookup"><span data-stu-id="c8f95-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="c8f95-109">Обновления ячеек больше не сериализуются.</span><span class="sxs-lookup"><span data-stu-id="c8f95-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="c8f95-110">Так как используется блочная отправка, приложение больше не находится в чате.</span><span class="sxs-lookup"><span data-stu-id="c8f95-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="c8f95-111">Используется сжатие данных, что приводит к уменьшению объема приложения FAT.</span><span class="sxs-lookup"><span data-stu-id="c8f95-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="c8f95-112">По-прежнему существует проблема с этой версией приложения; риск возникновения взаимоблокировки, так как при использовании большой отправки не получается.</span><span class="sxs-lookup"><span data-stu-id="c8f95-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="c8f95-113">Сервер отправляет один байт для каждого полученного 3 байта.</span><span class="sxs-lookup"><span data-stu-id="c8f95-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="c8f95-114">Это может привести к взаимоблокировке, если размер буфера получения меньше 1000 байт для этого примера приложения.</span><span class="sxs-lookup"><span data-stu-id="c8f95-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="c8f95-115">Ключевые метрики производительности</span><span class="sxs-lookup"><span data-stu-id="c8f95-115">Key Performance Metrics</span></span>

<span data-ttu-id="c8f95-116">Следующие метрики производительности выражаются в времени кругового пути (RTT), Гудпут и служебных издержках.</span><span class="sxs-lookup"><span data-stu-id="c8f95-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="c8f95-117">Описание этих терминов см. в разделе [терминология сети](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c8f95-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="c8f95-118">Эта версия отражает следующие метрики производительности.</span><span class="sxs-lookup"><span data-stu-id="c8f95-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="c8f95-119">Время ожидания в ячейке — \* . 002</span><span class="sxs-lookup"><span data-stu-id="c8f95-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="c8f95-120">Гудпут — 2 КБ/RTT</span><span class="sxs-lookup"><span data-stu-id="c8f95-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="c8f95-121">Нагрузка на протоколы — 14%</span><span class="sxs-lookup"><span data-stu-id="c8f95-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="c8f95-122">Из 14% накладных расходов 6% из заголовков Ethernet, а другая 8% — с запуска и уничтожения подключения.</span><span class="sxs-lookup"><span data-stu-id="c8f95-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8f95-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c8f95-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8f95-124">Повышение скорости работы приложения</span><span class="sxs-lookup"><span data-stu-id="c8f95-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="c8f95-125">Терминология сети</span><span class="sxs-lookup"><span data-stu-id="c8f95-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="c8f95-126">Базовая версия: очень плохо выполняемое приложение</span><span class="sxs-lookup"><span data-stu-id="c8f95-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="c8f95-127">Редакция 1. Очистка очевидных</span><span class="sxs-lookup"><span data-stu-id="c8f95-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="c8f95-128">Редакция 2. перепроектирование для уменьшения количества подключений</span><span class="sxs-lookup"><span data-stu-id="c8f95-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="c8f95-129">Будущие улучшения</span><span class="sxs-lookup"><span data-stu-id="c8f95-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



