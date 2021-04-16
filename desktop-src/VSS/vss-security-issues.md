---
description: Проблемы безопасности VSS
ms.assetid: 99dacdbb-9c40-48dd-b5fe-2f13de7af140
title: Проблемы безопасности VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af561b512dd5dbaec954707a813c76391c1ee43a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692365"
---
# <a name="vss-security-issues"></a><span data-ttu-id="e7a11-103">Проблемы безопасности VSS</span><span class="sxs-lookup"><span data-stu-id="e7a11-103">VSS Security Issues</span></span>

<span data-ttu-id="e7a11-104">Инфраструктура VSS внутренне основана на модели COM и поэтому модули записи и запрашивающие объекты должны взаимодействовать с системой безопасности на основе COM.</span><span class="sxs-lookup"><span data-stu-id="e7a11-104">The VSS infrastructure is internally based on COM, and therefore allowing writers and requesters to communicate requires COM-based security.</span></span> <span data-ttu-id="e7a11-105">Безопасность COM предоставляет механизмы и рекомендации, которые должен учитывать разработчик VSS:</span><span class="sxs-lookup"><span data-stu-id="e7a11-105">COM security provides mechanisms and guidelines that a VSS developer should consider:</span></span>

-   [<span data-ttu-id="e7a11-106">Вопросы безопасности для модулей записи</span><span class="sxs-lookup"><span data-stu-id="e7a11-106">Security Considerations for Writers</span></span>](security-considerations-for-writers.md)
-   [<span data-ttu-id="e7a11-107">Вопросы безопасности для запрашивающих стороны</span><span class="sxs-lookup"><span data-stu-id="e7a11-107">Security Considerations for Requesters</span></span>](security-considerations-for-requestors.md)

 

 



