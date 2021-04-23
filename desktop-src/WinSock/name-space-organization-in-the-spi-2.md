---
description: Организация пространства имен в сокетах Windows (Winsock) SPI.
ms.assetid: c369a476-23e4-48a1-912b-2d876deb0b88
title: Организация пространства имен в SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a572ad86299f0bf5ba3e7f95662e1616da520608
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647166"
---
# <a name="namespace-organization-in-the-spi"></a><span data-ttu-id="a41f0-103">Организация пространства имен в SPI</span><span class="sxs-lookup"><span data-stu-id="a41f0-103">Namespace Organization in the SPI</span></span>

<span data-ttu-id="a41f0-104">Многие пространства имен упорядочиваются иерархически.</span><span class="sxs-lookup"><span data-stu-id="a41f0-104">Many namespaces are arranged hierarchically.</span></span> <span data-ttu-id="a41f0-105">Некоторые, такие как X. 500 и NDS, разрешают неограниченное вложение.</span><span class="sxs-lookup"><span data-stu-id="a41f0-105">Some, such as X.500 and NDS, allow unlimited nesting.</span></span> <span data-ttu-id="a41f0-106">Другие позволяют объединять службы в один уровень иерархии или группы.</span><span class="sxs-lookup"><span data-stu-id="a41f0-106">Others allow services to be combined into a single level of hierarchy or group.</span></span> <span data-ttu-id="a41f0-107">Обычно это называется рабочей группой.</span><span class="sxs-lookup"><span data-stu-id="a41f0-107">This is typically referred to as a workgroup.</span></span> <span data-ttu-id="a41f0-108">При создании запроса часто бывает необходимо установить контекстную точку внутри иерархии пространства имен, из которой начнется поиск.</span><span class="sxs-lookup"><span data-stu-id="a41f0-108">When constructing a query, it is often necessary to establish a context point within a namespace hierarchy from which the search will begin.</span></span>

 

 



