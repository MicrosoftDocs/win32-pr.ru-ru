---
title: Поведение репликации в службах домен Active Directory Services
description: Репликация является единообразной и предсказуемой; Учитывая набор изменений, внесенных в данную реплику, результат может быть прогнозируемым \ 8212; изменения будут распространены на все другие реплики.
ms.assetid: 4e9f2e43-6375-4663-93ca-55112fd00abe
ms.tgt_platform: multiple
keywords:
- Службы домен Active Directory Active Directory, репликация
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41009a733f99366e499a25baca989f4f28794aea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103887623"
---
# <a name="replication-behavior-in-active-directory-domain-services"></a><span data-ttu-id="c72b9-104">Поведение репликации в службах домен Active Directory Services</span><span class="sxs-lookup"><span data-stu-id="c72b9-104">Replication Behavior in Active Directory Domain Services</span></span>

<span data-ttu-id="c72b9-105">Репликация является единообразной и предсказуемой; Учитывая набор изменений, внесенных в данную реплику, результат может быть прогнозируемым — изменения будут распространяться на все другие реплики.</span><span class="sxs-lookup"><span data-stu-id="c72b9-105">Replication behavior is consistent and predictable; given a set of changes to a given replica, the outcome can be predicted—the changes will be propagated to all other replicas.</span></span> <span data-ttu-id="c72b9-106">Девисинг надежную общую модель для прогнозирования того, когда изменения будут применены на всех других репликах или в определенной реплике, невозможно, поскольку будущее состояние распределенной системы в целом не может быть известно.</span><span class="sxs-lookup"><span data-stu-id="c72b9-106">Devising a reliable general model for predicting when the changes will be applied at all other replicas, or at a particular replica, is impossible, because the future state of the distributed system as a whole cannot be known.</span></span> <span data-ttu-id="c72b9-107">Это называется недетерминированной задержкой, и приложения, использующие каталог, должны понимать и разрешать его.</span><span class="sxs-lookup"><span data-stu-id="c72b9-107">This is called "nondeterministic latency," and applications that use the directory must understand and allow for it.</span></span>

<span data-ttu-id="c72b9-108">Ситуация не так сложна, как может показаться.</span><span class="sxs-lookup"><span data-stu-id="c72b9-108">The situation is not as complex at it might appear.</span></span> <span data-ttu-id="c72b9-109">Приложение должно размещать только три состояния:</span><span class="sxs-lookup"><span data-stu-id="c72b9-109">There are only three states that an application must accommodate:</span></span>

-   <span data-ttu-id="c72b9-110">Отклонение версий: ни одно из изменений, примененных к данной исходной реплике, не распространялось на указанную реплику назначения.</span><span class="sxs-lookup"><span data-stu-id="c72b9-110">Version Skew: None of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="c72b9-111">Приложение, считывающее исходную реплику, видит новую версию информации, в то время как приложение, считывающее назначение, видит старую версию (или ничего, если новые сведения были добавлены в первый раз).</span><span class="sxs-lookup"><span data-stu-id="c72b9-111">An application reading the source replica sees the new version of the information, while an application reading the destination sees the old version (or nothing, if the new information was added for the first time).</span></span> <span data-ttu-id="c72b9-112">Отклонение версий применяется ко всем потребителям службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="c72b9-112">Version skew applies to all directory service consumers.</span></span>
-   <span data-ttu-id="c72b9-113">Частичное обновление: некоторые изменения, примененные к данной исходной реплике, распространяются на указанную реплику назначения.</span><span class="sxs-lookup"><span data-stu-id="c72b9-113">Partial Update: Some of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="c72b9-114">Приложение, считывающее исходную реплику, видит новую информацию, в то время как приложение, считывающее назначение, видит комбинацию старой и новой информации (или только часть новой информации, если новая информация была добавлена в первый раз).</span><span class="sxs-lookup"><span data-stu-id="c72b9-114">An application reading the source replica sees the new information, while an application reading the destination sees a mix of old and new information (or only some of the new information, if the new information was added for the first time).</span></span> <span data-ttu-id="c72b9-115">Частичное обновление применяется к потребителям службы каталогов, использующим два или более связанных объектов для хранения своих данных.</span><span class="sxs-lookup"><span data-stu-id="c72b9-115">Partial update applies to directory service consumers that use two or more related objects to store their information.</span></span>
-   <span data-ttu-id="c72b9-116">Полностью реплицированное состояние: все изменения, примененные к данной исходной реплике, распространяются на указанную реплику назначения.</span><span class="sxs-lookup"><span data-stu-id="c72b9-116">Fully Replicated State: All of the changes that are applied to a given source replica have propagated to a given destination replica.</span></span> <span data-ttu-id="c72b9-117">Приложения на репликах источника и назначения видят одну и ту же информацию.</span><span class="sxs-lookup"><span data-stu-id="c72b9-117">Applications at the source and destination replicas see the same information.</span></span>

 

 




