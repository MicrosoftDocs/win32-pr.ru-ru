---
title: Дата и время вступления в силу
description: Эффективная дата и время — это стратегия предотвращения, которая предотвращает отклонение версий и частичные обновления, откладывая актуальные данные на некоторый момент в будущем, когда изменение дает высокую вероятность полной репликации.
ms.assetid: 5e24f90a-dd53-4720-815e-9a1db51847a3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448941b7ab0d85d50123985a120beb04f256d877
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067390"
---
# <a name="effective-date-and-time"></a><span data-ttu-id="d9ac7-103">Дата и время вступления в силу</span><span class="sxs-lookup"><span data-stu-id="d9ac7-103">Effective Date and Time</span></span>

<span data-ttu-id="d9ac7-104">*Эффективная дата и время* — это стратегия предотвращения, которая предотвращает отклонение версий и частичные обновления, откладывая актуальные данные на некоторый момент в будущем, когда изменение дает высокую вероятность полной репликации.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-104">*Effective date and time* is an avoidance strategy that prevents version skew and partial updates by deferring the effective data of information to some point in the future when the change has a high probability of being fully replicated.</span></span> <span data-ttu-id="d9ac7-105">Чтобы реализовать эффективные даты, объекты приложения должны включать метку времени начала действия, которая заполняется при создании или изменении объекта.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-105">To implement effective dates, the application objects must include an effective date timestamp, which is filled in when the object is created or changed.</span></span> <span data-ttu-id="d9ac7-106">Потребители объектов проверяют отметку времени и откладывают использование объектов до тех пор, пока не будет достигнута дата и время.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-106">Consumers of the objects verify the timestamp and defer use of the objects until that date and time are reached.</span></span>

<span data-ttu-id="d9ac7-107">Важные сведения</span><span class="sxs-lookup"><span data-stu-id="d9ac7-107">Some important considerations:</span></span>

-   <span data-ttu-id="d9ac7-108">Приложения, которые выбирают этот подход, должны гарантировать, что существует набор применимых данных для использования, пока обновленные объекты не вступят в силу.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-108">Applications that choose this approach must ensure that there is a set of applicable data to use until the updated objects become effective.</span></span>
-   <span data-ttu-id="d9ac7-109">Распределенная служба времени в Windows NT 4,0 позволяет синхронизировать часы подключенных Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-109">Distributed time service in Windows NT 4.0 keeps the clocks of the connected Windows 2000 synchronized.</span></span> <span data-ttu-id="d9ac7-110">Однако служба времени не идеальна, поэтому для неравномерного распределения версий существует небольшое окно.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-110">No time service is perfect, however, so there is a small window for version skew.</span></span>
-   <span data-ttu-id="d9ac7-111">Установка хорошей эффективной даты предполагает знание общей задержки репликации для распределенной системы.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-111">Setting a good effective date presumes knowledge of the overall replication latency for the distributed system in question.</span></span> <span data-ttu-id="d9ac7-112">В стабильной сети хорошим правилом для дат вступления в силу является (время обновления) + (2 \* (Средняя общая задержка)).</span><span class="sxs-lookup"><span data-stu-id="d9ac7-112">In a stable network a good rule of thumb for effective dates is the (time of the update) + (2\*(average overall latency)).</span></span> <span data-ttu-id="d9ac7-113">Таким образом, для системы, Общая задержка в среднем 4 часа, приемлема задержка в 8 часов.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-113">So, for a system whose overall latency averages 4 hours, a delay of 8 hours is reasonable.</span></span>
-   <span data-ttu-id="d9ac7-114">В нестабильной сети определение «хорошего» значения для эффективных дат гораздо сложнее, так как задержка может быть очень высокой.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-114">In an unstable network, determining a "good" value for effective dates is much more difficult, since the latency may be highly variable.</span></span> <span data-ttu-id="d9ac7-115">Эффективная дата является наиболее эффективным в нестабильной сети в сочетании с другими стратегиями предотвращения или обнаружения, такими как контрольные суммы или идентификаторы GUID согласованности.</span><span class="sxs-lookup"><span data-stu-id="d9ac7-115">Effective date is most "effective" in an unstable network when combined with other avoidance or detection strategies such as checksums or consistency GUIDs.</span></span> <span data-ttu-id="d9ac7-116">Дополнительные сведения см. в разделе [контрольные суммы и счетчики объектов](checksums-and-object-counts.md).</span><span class="sxs-lookup"><span data-stu-id="d9ac7-116">For more information, see [Checksums and Object Counts](checksums-and-object-counts.md).</span></span>

 

 




