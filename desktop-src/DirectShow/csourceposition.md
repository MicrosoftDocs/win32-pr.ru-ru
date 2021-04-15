---
description: Ксаурцепоситион является абстрактным классом для реализации интерфейса Имедиапоситион в фильтре источника.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Класс Ксаурцепоситион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105655577"
---
# <a name="csourceposition-class"></a><span data-ttu-id="eb0d1-103">Класс Ксаурцепоситион</span><span class="sxs-lookup"><span data-stu-id="eb0d1-103">CSourcePosition class</span></span>

<span data-ttu-id="eb0d1-104">`CSourcePosition` является абстрактным классом для реализации интерфейса [**имедиапоситион**](/windows/desktop/api/Control/nn-control-imediaposition) в фильтре источника.</span><span class="sxs-lookup"><span data-stu-id="eb0d1-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="eb0d1-105">Этот класс устарел.</span><span class="sxs-lookup"><span data-stu-id="eb0d1-105">This class is obsolete.</span></span> <span data-ttu-id="eb0d1-106">Если фильтр источников доступен для поиска, он должен предоставлять интерфейс [**имедиасикинг**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) вместо **имедиапоситион**.</span><span class="sxs-lookup"><span data-stu-id="eb0d1-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="eb0d1-107">Для этой цели можно использовать базовый класс [**ксаурцесикинг**](csourceseeking.md) .</span><span class="sxs-lookup"><span data-stu-id="eb0d1-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



