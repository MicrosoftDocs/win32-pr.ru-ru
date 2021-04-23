---
description: Изменения динамического формата
ms.assetid: ff60de5a-3edc-405d-aa02-8704b96d5e87
title: Изменения динамического формата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49496e0b43d9b120f6daf27007cde98191a7765b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673032"
---
# <a name="dynamic-format-changes"></a><span data-ttu-id="34161-103">Изменения динамического формата</span><span class="sxs-lookup"><span data-stu-id="34161-103">Dynamic Format Changes</span></span>

<span data-ttu-id="34161-104">При соединении двух фильтров они согласуются с типом мультимедиа, который описывает формат данных, которые доставляются вышестоящим фильтром.</span><span class="sxs-lookup"><span data-stu-id="34161-104">When two filters connect, they agree on a media type, which describes the format of the data that the upstream filter will deliver.</span></span> <span data-ttu-id="34161-105">В большинстве случаев тип носителя фиксирован на время соединения.</span><span class="sxs-lookup"><span data-stu-id="34161-105">In most cases, the media type is fixed for the duration of the connection.</span></span> <span data-ttu-id="34161-106">Однако DirectShow предлагает ограниченную поддержку фильтров для изменения типа носителя.</span><span class="sxs-lookup"><span data-stu-id="34161-106">However, DirectShow does offer limited support for filters to change the media type.</span></span> <span data-ttu-id="34161-107">Когда фильтр переключает типы носителей, он называется *динамическим изменением формата*.</span><span class="sxs-lookup"><span data-stu-id="34161-107">When a filter switches media types, it is called a *dynamic format change*.</span></span> <span data-ttu-id="34161-108">При написании фильтра DirectShow следует учитывать механизмы динамического изменения формата.</span><span class="sxs-lookup"><span data-stu-id="34161-108">If you are writing a DirectShow filter, you should be aware of the mechanisms for dynamic format changes.</span></span> <span data-ttu-id="34161-109">Даже если фильтр не поддерживает такие изменения, он должен правильно реагировать, если другой фильтр запрашивает новый формат.</span><span class="sxs-lookup"><span data-stu-id="34161-109">Even if your filter does not support such changes, it should respond correctly if another filter requests a new format.</span></span>

<span data-ttu-id="34161-110">DirectShow определяет несколько различных механизмов для изменения динамических форматов в зависимости от состояния графа фильтра и требуемого типа изменения.</span><span class="sxs-lookup"><span data-stu-id="34161-110">DirectShow defines several distinct mechanisms for dynamic format changes, depending on the state of filter graph and the type of change that is required.</span></span>

-   <span data-ttu-id="34161-111">Если граф остановлен, ПИН-коды могут повторно подключиться к типу носителя и заново согласовать его.</span><span class="sxs-lookup"><span data-stu-id="34161-111">If the graph is stopped, the pins can reconnect and renegotiate the media type.</span></span> <span data-ttu-id="34161-112">Дополнительные сведения см. в разделе [Повторное подключение ПИН](reconnecting-pins.md)-кодов.</span><span class="sxs-lookup"><span data-stu-id="34161-112">For more information, see [Reconnecting Pins](reconnecting-pins.md).</span></span>
-   <span data-ttu-id="34161-113">Некоторые фильтры могут переподключать ПИН-коды даже в том случае, если граф активен (работает или приостановлен).</span><span class="sxs-lookup"><span data-stu-id="34161-113">Some filters can reconnect pins even while the graph is active (running or paused).</span></span> <span data-ttu-id="34161-114">Дополнительные сведения об этом механизме см. в разделе [динамическое](dynamic-reconnection.md)повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="34161-114">For more information about this mechanism, see [Dynamic Reconnection](dynamic-reconnection.md).</span></span>

<span data-ttu-id="34161-115">В противном случае, если граф активен, но рассматриваемые фильтры не поддерживают повторное подключение к динамическому ПИН-коду, существует три возможных механизма изменения формата:</span><span class="sxs-lookup"><span data-stu-id="34161-115">Otherwise, if the graph is active, but the filters in question do not support dynamic pin reconnections, there are three possible mechanisms for changing the format:</span></span>

-   <span data-ttu-id="34161-116">[Куерякцепт (нисходящий)](queryaccept--downstream.md) используется, когда закрепление вывода предлагает изменение формата подчиненному узлу, но только в том случае, если новый формат не требует большего буфера.</span><span class="sxs-lookup"><span data-stu-id="34161-116">[QueryAccept (Downstream)](queryaccept--downstream.md) is used when If an output pin proposes a format change to its downstream peer, but only if the new format does not require a larger buffer.</span></span>
-   <span data-ttu-id="34161-117">[Куерякцепт (вышестоящий)](queryaccept--upstream.md) используется, когда закрепление ввода предлагает изменение формата вышестоящего однорангового узла.</span><span class="sxs-lookup"><span data-stu-id="34161-117">[QueryAccept (Upstream)](queryaccept--upstream.md) is used when an input pin proposes a format change to its upstream peer.</span></span> <span data-ttu-id="34161-118">Новый формат может быть таким же, что и размер, или он может быть больше.</span><span class="sxs-lookup"><span data-stu-id="34161-118">The new format can be the same size, or it can be larger.</span></span>
-   <span data-ttu-id="34161-119">[Рецеивеконнектион](receiveconnection.md) используется, когда закрепление вывода предлагает изменение формата подчиненному узлу, а новый формат требует большего буфера.</span><span class="sxs-lookup"><span data-stu-id="34161-119">[ReceiveConnection](receiveconnection.md) is used when an output pin proposes a format change to its downstream peer, and the new format requires a larger buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="34161-120">См. также</span><span class="sxs-lookup"><span data-stu-id="34161-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34161-121">Обработка изменений формата из модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="34161-121">Handling Format Changes from the Video Renderer</span></span>](handling-format-changes-from-the-video-renderer.md)
</dt> </dl>

 

 



