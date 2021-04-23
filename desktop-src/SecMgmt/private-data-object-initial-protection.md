---
description: При создании закрытого объекта данных ему назначается Стандартная защита.
ms.assetid: 7aed8c42-ffa8-43ea-b36e-d894c2ed6bf9
title: Начальная Защита объекта закрытых данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4324a0e147eaa36d2bf42b90b2597a91852183f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662303"
---
# <a name="private-data-object-initial-protection"></a><span data-ttu-id="c10d8-103">Начальная Защита объекта закрытых данных</span><span class="sxs-lookup"><span data-stu-id="c10d8-103">Private Data Object Initial Protection</span></span>

<span data-ttu-id="c10d8-104">При создании закрытого объекта данных ему назначается Стандартная защита следующим образом:</span><span class="sxs-lookup"><span data-stu-id="c10d8-104">When a Private Data object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="c10d8-105">Локальной группе «WORLD» предоставляется универсальный \_ доступ для выполнения.</span><span class="sxs-lookup"><span data-stu-id="c10d8-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="c10d8-106">Локальной \_ группе локального администратора предоставляется разрешение Удаление, универсальное \_ чтение, универсальная \_ запись и универсальный \_ доступ на выполнение.</span><span class="sxs-lookup"><span data-stu-id="c10d8-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="c10d8-107">Локальная \_ Группа локального администратора назначается как владелец и основная группа объекта.</span><span class="sxs-lookup"><span data-stu-id="c10d8-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 



