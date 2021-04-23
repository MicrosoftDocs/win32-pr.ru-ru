---
title: Интерфейс (RRAS)
description: Интерфейс — это логическое подключение к сети. Каждый интерфейс идентифицируется по уникальному индексу. Протоколы многоадресной маршрутизации (например, МОСПФ) работают со всеми типами интерфейсов аналогичным образом.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "103988093"
---
# <a name="interface-rras"></a><span data-ttu-id="a7779-105">Интерфейс (RRAS)</span><span class="sxs-lookup"><span data-stu-id="a7779-105">Interface (RRAS)</span></span>

<span data-ttu-id="a7779-106">Интерфейс — это логическое подключение к сети.</span><span class="sxs-lookup"><span data-stu-id="a7779-106">An interface is a logical connection to a network.</span></span> <span data-ttu-id="a7779-107">Каждый интерфейс идентифицируется по уникальному индексу.</span><span class="sxs-lookup"><span data-stu-id="a7779-107">Each interface is identified by a unique index.</span></span> <span data-ttu-id="a7779-108">Протоколы многоадресной маршрутизации (например, МОСПФ) работают со всеми типами интерфейсов аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="a7779-108">Multicast routing protocols (such as MOSPF) deal with all types of interfaces similarly.</span></span>

<span data-ttu-id="a7779-109">В случае с интерфейсом локальной сети интерфейс соответствует фактическому физическому устройству на компьютере (адаптер локальной сети).</span><span class="sxs-lookup"><span data-stu-id="a7779-109">In the case of a LAN interface, the interface corresponds to an actual physical device in the computer (the LAN adapter).</span></span> <span data-ttu-id="a7779-110">В случае с интерфейсом глобальной сети интерфейс сопоставляется с портом при установлении соединения.</span><span class="sxs-lookup"><span data-stu-id="a7779-110">In the case of a WAN interface, the interface is mapped to a port when a connection is established.</span></span> <span data-ttu-id="a7779-111">Интерфейсы глобальной сети могут основываться на туннелях, а порт может быть портом виртуальной частной сети (VPN).</span><span class="sxs-lookup"><span data-stu-id="a7779-111">WAN interfaces can be based on tunnels and the port could be a virtual private network (VPN) port.</span></span>

<span data-ttu-id="a7779-112">Операционная система Windows 2000 и более поздних версий поддерживает интерфейс "точка — MultiPoint".</span><span class="sxs-lookup"><span data-stu-id="a7779-112">Windows 2000 and later operating systems support a "point-to-multipoint" interface.</span></span> <span data-ttu-id="a7779-113">Этот тип интерфейса можно просмотреть в виде коллекции ссылок типа "точка-точка", совместно использующих одну точку завершения.</span><span class="sxs-lookup"><span data-stu-id="a7779-113">This type of interface can be viewed as a collection of point-to-point links that share a single termination point.</span></span>

<span data-ttu-id="a7779-114">Чтобы однозначно идентифицировать точную ссылку в интерфейсе типа "точка — MultiPoint", API МГМ использует адрес следующего прыжка идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a7779-114">To uniquely identify an exact link in a point-to-multipoint interface, the MGM API uses the next hop address of the interface ID.</span></span> <span data-ttu-id="a7779-115">Для поддержки этой идентификации API МГМ использует идентификатор расширенного интерфейса, который включает адрес [следующего прыжка](next-hop.md) .</span><span class="sxs-lookup"><span data-stu-id="a7779-115">To support this identification, the MGM API uses an extended interface ID, which includes a [next hop](next-hop.md) address.</span></span>

 

 




