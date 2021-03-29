---
title: Обнаружение и предотвращение задержки репликации
description: Задержка репликации является фактом жизни в слабо связанном распределенной системе.
ms.assetid: ea65759b-2bfa-4859-8d2a-5949bbb9adef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 271b4d84689068824a6e46095a5ed93462f49e2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773256"
---
# <a name="detecting-and-avoiding-replication-latency"></a><span data-ttu-id="746f1-103">Обнаружение и предотвращение задержки репликации</span><span class="sxs-lookup"><span data-stu-id="746f1-103">Detecting and Avoiding Replication Latency</span></span>

<span data-ttu-id="746f1-104">Задержка репликации является фактом жизни в слабо связанном распределенной системе.</span><span class="sxs-lookup"><span data-stu-id="746f1-104">Replication latency is a fact of life in a loosely coupled distributed system.</span></span> <span data-ttu-id="746f1-105">Эти приложения должны соответствовать этим требованиям.</span><span class="sxs-lookup"><span data-stu-id="746f1-105">Applications must accommodate this.</span></span> <span data-ttu-id="746f1-106">Лучшим способом обеспечить задержку репликации является проектирование приложений для снижения влияния.</span><span class="sxs-lookup"><span data-stu-id="746f1-106">The best way to accommodate replication latency is to design applications to minimize the effects.</span></span> <span data-ttu-id="746f1-107">Идеальное приложение с поддержкой каталогов:</span><span class="sxs-lookup"><span data-stu-id="746f1-107">The ideal directory-enabled application:</span></span>

-   <span data-ttu-id="746f1-108">Не учитывается при отклонении версий.</span><span class="sxs-lookup"><span data-stu-id="746f1-108">Is insensitive to version skew.</span></span>
-   <span data-ttu-id="746f1-109">Не зависит от связей между несколькими объектами.</span><span class="sxs-lookup"><span data-stu-id="746f1-109">Does not depend on relationships among multiple objects.</span></span>
-   <span data-ttu-id="746f1-110">Не имеет требований к согласованности внутри или между объектами.</span><span class="sxs-lookup"><span data-stu-id="746f1-110">Has no intra- or inter-object consistency requirements.</span></span>

<span data-ttu-id="746f1-111">Приложения и службы, которые соответствуют этому профилю, не должны беспокоиться о задержке репликации.</span><span class="sxs-lookup"><span data-stu-id="746f1-111">Applications and services that fit this profile need not be concerned with replication latency.</span></span> <span data-ttu-id="746f1-112">Другие приложения должны быть спроектированы с учетом задержки репликации.</span><span class="sxs-lookup"><span data-stu-id="746f1-112">Other applications must be designed with replication latency in mind.</span></span> <span data-ttu-id="746f1-113">Ключом к успешному проектированию такого приложения является информированность процесса репликации.</span><span class="sxs-lookup"><span data-stu-id="746f1-113">The key to success in designing such an application is awareness of the replication process.</span></span> <span data-ttu-id="746f1-114">Шаги, выполняемые во время разработки для уменьшения зависимостей между объектами, и свертывание окон частичного обновления будут оплачиваться крупные дивиденды во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="746f1-114">Steps taken at design time to reduce inter-object dependencies and minimize partial update windows will pay large dividends at run time.</span></span> <span data-ttu-id="746f1-115">Подходы к работе с задержкой репликации делятся на два класса — избежать стратегий, снижающих влияние задержки и стратегии обнаружения, которые позволяют приложению обнаруживать состояния, вызывающие задержки.</span><span class="sxs-lookup"><span data-stu-id="746f1-115">Approaches to dealing with replication latency are divided into two classes—avoidance strategies that reduce the impact of latency and detection strategies that allow an application to detect latency-induced states.</span></span>

 

 




