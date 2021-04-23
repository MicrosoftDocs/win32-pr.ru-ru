---
description: Нужна
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Нужна
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104560250"
---
# <a name="seeking"></a><span data-ttu-id="d9e23-103">Нужна</span><span class="sxs-lookup"><span data-stu-id="d9e23-103">Seeking</span></span>

<span data-ttu-id="d9e23-104">Фильтры поддерживают поиск через интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="d9e23-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="d9e23-105">Приложение запрашивает диспетчер графа фильтров для **имедиасикинг** и использует его для выполнения команд Seek.</span><span class="sxs-lookup"><span data-stu-id="d9e23-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="d9e23-106">Диспетчер графов фильтров распространяет каждую команду поиска на все фильтры модуля подготовки отчетов в графе.</span><span class="sxs-lookup"><span data-stu-id="d9e23-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="d9e23-107">Каждый модуль подготовки отчетов передает командный поток через выходные контакты вышестоящего фильтра до тех пор, пока не достигнет фильтра, который может выполнить поиск.</span><span class="sxs-lookup"><span data-stu-id="d9e23-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="d9e23-108">Как правило, фильтр источника или фильтр синтаксического анализатора, например, [Разделитель AVI](avi-splitter-filter.md), выполняет операцию поиска.</span><span class="sxs-lookup"><span data-stu-id="d9e23-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="d9e23-109">Когда фильтр выполняет операцию поиска, он очищает все ожидающие данные.</span><span class="sxs-lookup"><span data-stu-id="d9e23-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="d9e23-110">Результат заключается в том, чтобы максимально сокращать задержку команд Seek, поскольку существующие данные очищаются из графа.</span><span class="sxs-lookup"><span data-stu-id="d9e23-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="d9e23-111">После команды Seek время потока сбрасывается в ноль.</span><span class="sxs-lookup"><span data-stu-id="d9e23-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="d9e23-112">На следующей схеме показана последовательность событий.</span><span class="sxs-lookup"><span data-stu-id="d9e23-112">The following diagram illustrates the sequence of events.</span></span>

![последовательность событий](images/seeking.png)

<span data-ttu-id="d9e23-114">Если фильтр синтаксического анализатора имеет более одного выходного ПИН-кода, он обычно назначает один из них для приема команд Seek.</span><span class="sxs-lookup"><span data-stu-id="d9e23-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="d9e23-115">Другие ПИН-коды отклоняются или игнорируют любые команды поиска, которые они получают.</span><span class="sxs-lookup"><span data-stu-id="d9e23-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="d9e23-116">Таким образом средство синтаксического анализа сохраняет все его потоки в синхронизированном виде.</span><span class="sxs-lookup"><span data-stu-id="d9e23-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="d9e23-117">Однако все выходные сигналы должны реализовывать [**имедиасикинг:: Capabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) и [**Имедиасикинг:: чекккапабилитиес**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) , чтобы получить возможности поиска фильтра.</span><span class="sxs-lookup"><span data-stu-id="d9e23-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="d9e23-118">Это гарантирует, что диспетчер графа фильтров вернет правильное значение в приложение.</span><span class="sxs-lookup"><span data-stu-id="d9e23-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="d9e23-119">Интерфейс [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) устарел для фильтров.</span><span class="sxs-lookup"><span data-stu-id="d9e23-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="d9e23-120">Клиенты автоматизации по-прежнему должны использовать этот интерфейс в диспетчере графов фильтров, так как **имедиасикинг** не совместима с автоматизацией, но диспетчер графов фильтров преобразует все вызовы **Имедиапоситион** в вызовы **имедиасикинг** .</span><span class="sxs-lookup"><span data-stu-id="d9e23-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9e23-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d9e23-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9e23-122">Очистки</span><span class="sxs-lookup"><span data-stu-id="d9e23-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="d9e23-123">Время и часы в DirectShow</span><span class="sxs-lookup"><span data-stu-id="d9e23-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



