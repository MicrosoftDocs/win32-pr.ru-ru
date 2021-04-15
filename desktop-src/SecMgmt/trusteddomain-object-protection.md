---
description: При создании объекта Трустеддомаин ему назначается Стандартная защита.
ms.assetid: cc554630-7be7-4657-90f2-ce5fa81731b2
title: Защита объектов Трустеддомаин
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd27a01c1bcfde12fd062f2e8ae7c92a979991a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682573"
---
# <a name="trusteddomain-object-protection"></a><span data-ttu-id="2ccf1-103">Защита объектов Трустеддомаин</span><span class="sxs-lookup"><span data-stu-id="2ccf1-103">TrustedDomain Object Protection</span></span>

<span data-ttu-id="2ccf1-104">При создании объекта [**трустеддомаин**](trusteddomain-object.md) ему присваивается стандартная защита следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2ccf1-104">When a [**TrustedDomain**](trusteddomain-object.md) object is created, it is assigned a standard protection as follows:</span></span>

-   <span data-ttu-id="2ccf1-105">Локальной группе «WORLD» предоставляется универсальный \_ доступ для выполнения.</span><span class="sxs-lookup"><span data-stu-id="2ccf1-105">The WORLD local group is granted GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="2ccf1-106">Локальной \_ группе локального администратора предоставляется разрешение Удаление, универсальное \_ чтение, универсальная \_ запись и универсальный \_ доступ на выполнение.</span><span class="sxs-lookup"><span data-stu-id="2ccf1-106">The LOCAL\_ADMIN local group is granted DELETE, GENERIC\_READ, GENERIC\_WRITE, and GENERIC\_EXECUTE access.</span></span>
-   <span data-ttu-id="2ccf1-107">Локальная \_ Группа локального администратора назначается как владелец и основная группа объекта.</span><span class="sxs-lookup"><span data-stu-id="2ccf1-107">The LOCAL\_ADMIN local group is assigned as owner and primary group of the object.</span></span>

 

 



