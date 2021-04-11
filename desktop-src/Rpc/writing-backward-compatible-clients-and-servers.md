---
title: Написание обратно совместимых клиентов и серверов
description: Теоретически, схема управления версиями RPC помогает избежать невозможности обмена данными между измененными серверами и клиентами и их развернутыми аналогами.
ms.assetid: 0c7d6716-e4ed-447e-bf64-906d55bec907
keywords:
- Удаленный вызов процедур RPC, рекомендации, обратная совместимость
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac5ae011c8a9c346bc0f89fb73e26265d487721
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104132898"
---
# <a name="writing-backward-compatible-clients-and-servers"></a><span data-ttu-id="4cbd3-104">Написание обратно совместимых клиентов и серверов</span><span class="sxs-lookup"><span data-stu-id="4cbd3-104">Writing Backward Compatible Clients and Servers</span></span>

<span data-ttu-id="4cbd3-105">Теоретически, схема управления версиями RPC помогает избежать невозможности обмена данными между измененными серверами и клиентами и их развернутыми аналогами.</span><span class="sxs-lookup"><span data-stu-id="4cbd3-105">In theory, the versioning scheme of RPC helps prevent miscommunication between modified servers and clients and their deployed counterparts.</span></span> <span data-ttu-id="4cbd3-106">Однако на практике разработчики часто должны внести изменения в существующие интерфейсы без изменения версии, так как предыдущие клиенты и серверы должны иметь возможность взаимодействовать с новыми.</span><span class="sxs-lookup"><span data-stu-id="4cbd3-106">In practice, however, developers frequently must introduce changes to existing interfaces without modifying the version, because previous clients and servers must be able to communicate with new ones.</span></span> <span data-ttu-id="4cbd3-107">Это большая проблема для стандартного RPC, чем для COM; запросы — это естественный способ поиска поддерживаемых интерфейсов в COM, а для эквивалентного покрытия необходимо использовать обработку исключений RPC.</span><span class="sxs-lookup"><span data-stu-id="4cbd3-107">This is a larger issue for standard RPC than for COM; querying is a natural way of searching for supported interfaces in COM, while in RPC exception handling must be used for equivalent coverage.</span></span>

<span data-ttu-id="4cbd3-108">В этом разделе обсуждаются оптимальные методы программирования RPC для решения этих ситуаций.</span><span class="sxs-lookup"><span data-stu-id="4cbd3-108">This section discusses the best RPC programming practices for addressing these situations.</span></span> <span data-ttu-id="4cbd3-109">Этот раздел состоит из следующих разделов:</span><span class="sxs-lookup"><span data-stu-id="4cbd3-109">This section is divided into the following topics:</span></span>

-   [<span data-ttu-id="4cbd3-110">Теория управления версиями для RPC и COM</span><span class="sxs-lookup"><span data-stu-id="4cbd3-110">The Versioning Theory for RPC and COM</span></span>](the-versioning-theory-for-rpc-and-com.md)
-   [<span data-ttu-id="4cbd3-111">Изменение интерфейсов с обратной совместимостью</span><span class="sxs-lookup"><span data-stu-id="4cbd3-111">Changing Interfaces in a Backward Compatible Manner</span></span>](changing-interfaces-in-a-backward-compatible-manner.md)
-   [<span data-ttu-id="4cbd3-112">Примеры несовместимых изменений</span><span class="sxs-lookup"><span data-stu-id="4cbd3-112">Examples of Incompatible Changes</span></span>](examples-of-incompatible-changes.md)

 

 




