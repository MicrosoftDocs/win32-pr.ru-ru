---
title: Контрольные суммы и счетчики объектов
description: Контрольные суммы и счетчики объектов — это стратегии обнаружения, которые позволяют приложению обнаруживать состояние частичного обновления.
ms.assetid: 14829a74-c186-4250-beac-036c5ecc5913
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc643ec7cd896a7c73df0be5738887a330392140
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486540"
---
# <a name="checksums-and-object-counts"></a><span data-ttu-id="fd7af-103">Контрольные суммы и счетчики объектов</span><span class="sxs-lookup"><span data-stu-id="fd7af-103">Checksums and Object Counts</span></span>

<span data-ttu-id="fd7af-104">Контрольные суммы и счетчики объектов — это стратегии обнаружения, которые позволяют приложению обнаруживать состояние частичного обновления.</span><span class="sxs-lookup"><span data-stu-id="fd7af-104">Checksums and object counts are detection strategies that allow an application to detect a partial update state.</span></span> <span data-ttu-id="fd7af-105">Контрольные суммы можно также использовать для обнаружения несоответствий, появившихся при разрешении конфликтов.</span><span class="sxs-lookup"><span data-stu-id="fd7af-105">Checksums can also be used to detect inconsistencies introduced by collision resolution.</span></span> <span data-ttu-id="fd7af-106">Как контрольные суммы, так и счетчики объектов, для хранения значения, используемого для проверки контрольной суммы или числа объектов, требуется место.</span><span class="sxs-lookup"><span data-stu-id="fd7af-106">Both checksums and object counts require a place to store the value used for verifying a checksum or object count.</span></span> <span data-ttu-id="fd7af-107">Это может быть объект "Master", выбранный из других связанных с конкретным приложением связей или родительским объектом, в котором хранятся связанные объекты.</span><span class="sxs-lookup"><span data-stu-id="fd7af-107">This can be on a "master" object chosen from among those involved in the application-specific relationship or on a parent object under which the related objects are stored.</span></span>

<span data-ttu-id="fd7af-108">Для контрольных сумм приложения, считывающие связанные объекты, проверяют контрольную сумму, вычисляя локальный результат и сравнивая его с сохраненным значением.</span><span class="sxs-lookup"><span data-stu-id="fd7af-108">For checksums, applications reading the related objects verify the checksum by calculating a local result and comparing it with the stored value.</span></span> <span data-ttu-id="fd7af-109">Если значения не совпадают, реплика находится в состоянии частичного обновления, и объекты не могут быть использованы.</span><span class="sxs-lookup"><span data-stu-id="fd7af-109">If the values do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="fd7af-110">Для счетчиков объектов приложения подсчитываются связанные объекты (обычно дочерние элементы одного родителя) и сравнивают количество с сохраненным значением.</span><span class="sxs-lookup"><span data-stu-id="fd7af-110">For object counts, applications count the related objects (typically children of a single parent) and compare the count with the stored value.</span></span> <span data-ttu-id="fd7af-111">Если счетчики не совпадают, реплика находится в состоянии частичного обновления, и объекты не могут быть использованы.</span><span class="sxs-lookup"><span data-stu-id="fd7af-111">If the counts do not match, the replica is in a partial update state and the objects cannot be used.</span></span>

<span data-ttu-id="fd7af-112">Важные сведения</span><span class="sxs-lookup"><span data-stu-id="fd7af-112">Some important considerations:</span></span>

-   <span data-ttu-id="fd7af-113">Для работы подхода к контрольной сумме необходимо обновить один или несколько атрибутов, используемых при вычислении контрольной суммы.</span><span class="sxs-lookup"><span data-stu-id="fd7af-113">For the checksum approach to work, the one or more attributes used in computing the checksum must be updated.</span></span> <span data-ttu-id="fd7af-114">Алгоритм, используемый для вычисления контрольной суммы, должен надежно отражать различия во входных данных.</span><span class="sxs-lookup"><span data-stu-id="fd7af-114">The algorithm used to compute the checksum must reliably reflect differences in input.</span></span> <span data-ttu-id="fd7af-115">Если одинаковая контрольная сумма имеет много различных входных продуктов, алгоритм не будет надежно обнаруживать частичные обновления.</span><span class="sxs-lookup"><span data-stu-id="fd7af-115">If many different inputs product the same checksum, the algorithm will not reliably detect partial updates.</span></span> <span data-ttu-id="fd7af-116">"Salt-код" — это также полезно ввод со значениями, такими как **objectGUID** исходного компьютера и Дата и время обновления.</span><span class="sxs-lookup"><span data-stu-id="fd7af-116">"Salting" the input with values like the **objectGUID** of the source computer and the date and time of the update is also helpful.</span></span>
-   <span data-ttu-id="fd7af-117">Счетчики объектов лучше работают при использовании с новыми наборами объектов или в сочетании с идентификаторами GUID согласованности (Дополнительные сведения см. в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="fd7af-117">Object counts work best when used with new sets of objects, or in combination with consistency GUIDs (see the next section for more information).</span></span> <span data-ttu-id="fd7af-118">Приложение, выполняющее обновление, должно либо заранее выяснить количество объектов, которые будут находиться в контейнере, после завершения обновления, либо использовать другие средства, помечающие контейнер как недопустимые при завершении обновления (например, установив значение счетчика равным нулю).</span><span class="sxs-lookup"><span data-stu-id="fd7af-118">The application performing the update must either know, in advance, the number of objects that will be in the container when the update is completed or use some other means of marking the container invalid while the update proceeds (for example, setting the count to zero).</span></span> <span data-ttu-id="fd7af-119">После завершения обновления Исходное приложение помечает контейнер на количество содержащихся в нем объектов.</span><span class="sxs-lookup"><span data-stu-id="fd7af-119">After completing the update the source application marks the container with the count of objects contained.</span></span>

 

 




