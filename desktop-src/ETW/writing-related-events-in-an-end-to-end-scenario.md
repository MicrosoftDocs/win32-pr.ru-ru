---
description: ETW предоставляет способ группирования связанных событий из нескольких компонентов.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Написание связанных событий в комплексном сценарии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984544"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a><span data-ttu-id="37744-103">Написание связанных событий в комплексном сценарии</span><span class="sxs-lookup"><span data-stu-id="37744-103">Writing Related Events in an End-to-End Scenario</span></span>

<span data-ttu-id="37744-104">ETW предоставляет способ группирования связанных событий из нескольких компонентов.</span><span class="sxs-lookup"><span data-stu-id="37744-104">ETW provides a way to group related events from more than one component.</span></span> <span data-ttu-id="37744-105">Например, если несколько компонентов (на одном компьютере или на разных компьютерах) участвуют в обработке одних и тех же данных, и каждый компонент регистрирует события для своей части действия, можно сгруппировать все связанные события вместе.</span><span class="sxs-lookup"><span data-stu-id="37744-105">For example, if several components (either on the same computer or on different computers) are involved in processing the same data, and each component logs events for their portion of the activity, you can group all of the related events together.</span></span> <span data-ttu-id="37744-106">Это позволит потребителю использовать все события, от начала процесса до конца процесса.</span><span class="sxs-lookup"><span data-stu-id="37744-106">This will allow a consumer to consume all of the events, from the beginning of the process to the end of the process.</span></span>

<span data-ttu-id="37744-107">Сведения о записи связанных событий в поставщик [на основе манифеста](about-event-tracing.md) см. [в разделе запись связанных событий в поставщике на основе манифеста](writing-related-events-in-a-manifest-base-provider.md).</span><span class="sxs-lookup"><span data-stu-id="37744-107">To write related events in a [manifest-based](about-event-tracing.md) provider, see [Writing Related Events in a Manifest-based Provider](writing-related-events-in-a-manifest-base-provider.md).</span></span>

<span data-ttu-id="37744-108">Сведения о записи связанных событий в [классическом](about-event-tracing.md) поставщике см. в разделе [запись связанных событий в классическом поставщике](tracing-event-instances.md).</span><span class="sxs-lookup"><span data-stu-id="37744-108">To write related events in a [classic](about-event-tracing.md) provider, see [Writing Related Events in a Classic Provider](tracing-event-instances.md).</span></span>

 

 



