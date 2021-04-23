---
title: Зоны DNS
description: Зона DNS — это набор файлов или записей (точнее, база данных записей ресурсов), которая соответствует части иерархического пространства имен DNS.
ms.assetid: fc24bcd0-854d-4452-9c81-f344b52c7b4e
keywords:
- зоны DNS DNS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba8914e699e00cbbc2e699c2b36d40c8d00b87c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654222"
---
# <a name="dns-zones"></a><span data-ttu-id="fdbe5-104">Зоны DNS</span><span class="sxs-lookup"><span data-stu-id="fdbe5-104">DNS Zones</span></span>

<span data-ttu-id="fdbe5-105">Зона DNS — это набор файлов или записей (точнее, база данных записей ресурсов), которая соответствует части иерархического пространства имен DNS.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-105">A DNS zone is a set of files or records (more precisely, a database of resource record entries) that corresponds to part of the DNS hierarchical namespace.</span></span> <span data-ttu-id="fdbe5-106">Зоны DNS используются для определения того, какие DNS-серверы являются ответственными (полномочными) для разрешения запросов разрешения имен для определенного раздела иерархии DNS.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-106">DNS zones are used to delineate which DNS Servers are responsible (authoritative) for resolving name-resolution queries for a given section of the DNS hierarchy.</span></span> <span data-ttu-id="fdbe5-107">Зоны DNS отличаются от структуры доменов следующим образом: зоны могут состоять из одного или нескольких доменов DNS.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-107">DNS zones differ from the domain structure in the following fashion: zones can be composed of one or more DNS domains.</span></span> <span data-ttu-id="fdbe5-108">Одна зона в дереве доменов gadgets.widgets.microsoft.com может быть полномочной для мини-приложений и доменов widgets.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-108">One zone in the gadgets.widgets.microsoft.com domain tree might be authoritative for the gadgets and widgets domains.</span></span> <span data-ttu-id="fdbe5-109">Иными словами, нет необходимости, чтобы зоны DNS имели связь "один к одному" с доменами DNS.</span><span class="sxs-lookup"><span data-stu-id="fdbe5-109">In other words, there is not a requirement for DNS zones to have a one-to-one relationship with DNS domains.</span></span>

 

 




