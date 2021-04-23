---
description: Поток данных в графе фильтра
ms.assetid: 3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3
title: Поток данных в графе фильтра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38e0e730dd78e3a42a1121e4a63a053e6016402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895137"
---
# <a name="data-flow-in-the-filter-graph"></a><span data-ttu-id="06684-103">Поток данных в графе фильтра</span><span class="sxs-lookup"><span data-stu-id="06684-103">Data Flow in the Filter Graph</span></span>

<span data-ttu-id="06684-104">В этом разделе описывается перемещение данных мультимедиа с помощью графа фильтра.</span><span class="sxs-lookup"><span data-stu-id="06684-104">This section describes how media data moves through the filter graph.</span></span> <span data-ttu-id="06684-105">Обычно вам не нужно знать эти сведения для написания приложения DirectShow, хотя в некоторых ситуациях это может оказаться полезным.</span><span class="sxs-lookup"><span data-stu-id="06684-105">Usually, you do not need to know these details to write a DirectShow application, although in some situations you may find it helpful.</span></span> <span data-ttu-id="06684-106">Если вы пишете фильтр DirectShow, то необходимо понимать этот материал.</span><span class="sxs-lookup"><span data-stu-id="06684-106">If you are writing a DirectShow filter, you will need to understand this material.</span></span>

<span data-ttu-id="06684-107">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="06684-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="06684-108">Общие сведения о потоке данных в DirectShow</span><span class="sxs-lookup"><span data-stu-id="06684-108">Overview of Data Flow in DirectShow</span></span>](overview-of-data-flow-in-directshow.md)
-   [<span data-ttu-id="06684-109">Транспорты</span><span class="sxs-lookup"><span data-stu-id="06684-109">Transports</span></span>](transports.md)
-   [<span data-ttu-id="06684-110">Примеры и Распределительы</span><span class="sxs-lookup"><span data-stu-id="06684-110">Samples and Allocators</span></span>](samples-and-allocators.md)
-   [<span data-ttu-id="06684-111">Фильтрация состояний</span><span class="sxs-lookup"><span data-stu-id="06684-111">Filter States</span></span>](filter-states.md)
-   [<span data-ttu-id="06684-112">Модель опроса</span><span class="sxs-lookup"><span data-stu-id="06684-112">Pull Model</span></span>](pull-model.md)

## <a name="related-topics"></a><span data-ttu-id="06684-113">См. также</span><span class="sxs-lookup"><span data-stu-id="06684-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06684-114">Поток данных для разработчиков фильтров</span><span class="sxs-lookup"><span data-stu-id="06684-114">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> </dl>

 

 



