---
title: Функции модели репликации для служб домен Active Directory Services
description: Модель репликации, используемая в домен Active Directory Services, называется нестрогой согласованностью нескольких хозяев с конвергенцией.
ms.assetid: 8fd63871-68b4-4ed6-8165-145cbc90c213
ms.tgt_platform: multiple
keywords:
- Службы домен Active Directory, модель репликации
- Функции модели репликации Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923c49dd648063ebd6afd086be3729f28f1e4080
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654188"
---
# <a name="features-of-the-replication-model-for-active-directory-domain-services"></a><span data-ttu-id="3a12f-105">Функции модели репликации для служб домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="3a12f-105">Features of the Replication Model for Active Directory Domain Services</span></span>

<span data-ttu-id="3a12f-106">Модель репликации, используемая в домен Active Directory Services, называется *нестрогой согласованностью нескольких хозяев с конвергенцией*.</span><span class="sxs-lookup"><span data-stu-id="3a12f-106">The replication model used in Active Directory Domain Services is called *multi-master loose consistency with convergence*.</span></span> <span data-ttu-id="3a12f-107">В этой модели каталог может иметь много реплик; система репликации распространяет изменения, внесенные в любую заданную реплику, во все остальные реплики.</span><span class="sxs-lookup"><span data-stu-id="3a12f-107">In this model, the directory can have many replicas; a replication system propagates changes made at any given replica to all other replicas.</span></span> <span data-ttu-id="3a12f-108">Не гарантируется, что реплики будут согласованы друг с другом в определенный момент времени ("слабая согласованность"), так как изменения могут быть применены к любой реплике в любое время ("несколько хозяев").</span><span class="sxs-lookup"><span data-stu-id="3a12f-108">The replicas are not guaranteed to be consistent with each other at any particular time ("loose consistency"), because changes can be applied to any replica at any time ("multi-master").</span></span> <span data-ttu-id="3a12f-109">Если системе разрешено достичь стабильного состояния, при котором новые обновления не выполняются и все предыдущие обновления были полностью реплицированы, все реплики гарантированно сходятся по одному и тому же набору значений ("схождение").</span><span class="sxs-lookup"><span data-stu-id="3a12f-109">If the system is allowed to reach a steady state, in which no new updates are occurring and all previous updates have been completely replicated, all replicas are guaranteed to converge on the same set of values ("convergence").</span></span>

 

 




