---
description: Общая широковещательная рассылка через Интернет достигается путем установки \_ полей SA нетнум и SA \_ ноденум в двоичные файлы (1).
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: Широковещательная рассылка всех маршрутов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15830ad4f82a3cc5d93e84762c8c17ed0cfd85bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497475"
---
# <a name="all-routes-broadcast"></a><span data-ttu-id="c5c71-103">Широковещательная рассылка всех маршрутов</span><span class="sxs-lookup"><span data-stu-id="c5c71-103">All Routes Broadcast</span></span>

<span data-ttu-id="c5c71-104">Общая широковещательная рассылка через Интернет достигается путем установки полей **SA \_ нетнум** и **SA \_ ноденум** в двоичные файлы (1).</span><span class="sxs-lookup"><span data-stu-id="c5c71-104">A general broadcast through the Internet is achieved by setting the **sa\_netnum** and **sa\_nodenum** fields to binary ones (1).</span></span> <span data-ttu-id="c5c71-105">Поставщик услуг преобразует этот запрос в пакет типа 20, который распознает и пересылает IPX-маршрутизаторы.</span><span class="sxs-lookup"><span data-stu-id="c5c71-105">The service provider translates this request to a type-20 packet, which IPX routers recognize and forward.</span></span> <span data-ttu-id="c5c71-106">Пакет посещает все подсети и может дублироваться несколько раз.</span><span class="sxs-lookup"><span data-stu-id="c5c71-106">The packet visits all subnets and may be duplicated several times.</span></span> <span data-ttu-id="c5c71-107">Приемники должны поддерживать несколько повторяющихся копий датаграммы.</span><span class="sxs-lookup"><span data-stu-id="c5c71-107">Receivers must handle several duplicate copies of the datagram.</span></span>

<span data-ttu-id="c5c71-108">Использование этого типа вещания не является популярным среди сетевых администраторов, поэтому его использование должно быть чрезвычайно ограниченным.</span><span class="sxs-lookup"><span data-stu-id="c5c71-108">Use of this broadcast type is unpopular among network administrators, so its use should be extremely limited.</span></span> <span data-ttu-id="c5c71-109">Многие маршрутизаторы отключают такой тип вещания, в результате чего части подсети невидимы для пакета.</span><span class="sxs-lookup"><span data-stu-id="c5c71-109">Many routers disable this type of broadcast, leaving parts of the subnet invisible to the packet.</span></span>

 

 



