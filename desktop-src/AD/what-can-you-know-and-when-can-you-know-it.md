---
title: Что можно узнать, а также узнать, когда это возможно
description: Приложения, которые чувствительны к состояниям с задержкой, должны распознать состояния проблем и предпринять соответствующие меры.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654167"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a><span data-ttu-id="e842b-103">Что можно узнать, а когда это вы узнаете?</span><span class="sxs-lookup"><span data-stu-id="e842b-103">What Can You Know, and When Can You Know It?</span></span>

<span data-ttu-id="e842b-104">Приложения, которые чувствительны к состояниям с задержкой, должны распознать состояния проблем и предпринять соответствующие меры.</span><span class="sxs-lookup"><span data-stu-id="e842b-104">Applications that are sensitive to latency-induced states must recognize problem states and take appropriate action.</span></span> <span data-ttu-id="e842b-105">Существует два состояния проблем: отклонение версий и частичное обновление.</span><span class="sxs-lookup"><span data-stu-id="e842b-105">There are two problem states: version skew and partial update.</span></span> <span data-ttu-id="e842b-106">Отклонения версий не обнаруживаются при проверке службы каталогов (Помните, что аксиома распределенных вычислений, в которых [домен Active Directory службы используют эту модель репликации](why-active-directory-domain-services-uses-this-replication-model.md)).</span><span class="sxs-lookup"><span data-stu-id="e842b-106">Version skew is not detectable by examining the Directory Service (remember the axiom of distributed computing stated in [Why Active Directory Domain Services Use This Replication Model](why-active-directory-domain-services-uses-this-replication-model.md)).</span></span> <span data-ttu-id="e842b-107">Частичное обновление можно обнаружить, добавив метаданные к объектам, составляющим связанный набор.</span><span class="sxs-lookup"><span data-stu-id="e842b-107">Partial update can be detected by adding metadata to the objects that compose the related set.</span></span> <span data-ttu-id="e842b-108">В последующих разделах этого документа приведены предложения для таких метаданных.</span><span class="sxs-lookup"><span data-stu-id="e842b-108">Suggestions for such metadata appear in subsequent sections of this document.</span></span> <span data-ttu-id="e842b-109">Для снижения вероятности отклонения версий и частичного обновления могут потребоваться приложения стратегий.</span><span class="sxs-lookup"><span data-stu-id="e842b-109">There are avoidance strategies applications can take to reduce the possibility of both version skew and partial update.</span></span> <span data-ttu-id="e842b-110">Эти стратегии также обсуждаются в последующих разделах этого документа.</span><span class="sxs-lookup"><span data-stu-id="e842b-110">These strategies are also discussed in subsequent sections of this document.</span></span>

 

 




