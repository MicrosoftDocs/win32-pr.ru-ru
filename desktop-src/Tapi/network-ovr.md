---
description: Сеть просматривается в качестве механизма транспорта, который передает данные из одной точки в другую.
ms.assetid: 88374ac9-81c3-48c3-bf1a-5cfd734c257c
title: Сеть
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d25f0c643ed1b54edb0ec45d47abfdc2f29fd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497739"
---
# <a name="network"></a><span data-ttu-id="6e5ed-103">Сеть</span><span class="sxs-lookup"><span data-stu-id="6e5ed-103">Network</span></span>

<span data-ttu-id="6e5ed-104">Сеть просматривается в качестве механизма транспорта, который передает данные из одной точки в другую.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-104">A network is viewed as the transport mechanism that conveys data from one point to another.</span></span> <span data-ttu-id="6e5ed-105">Поставщики услуг TAPI обработают конкретные протоколы, необходимые для выполнения таких операций, как установка сеанса связи в определенной сети.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-105">TAPI service providers handle the specific protocols required to perform operations such as establishing a communications session on a given network.</span></span> <span data-ttu-id="6e5ed-106">Обычно для конечного пользователя или сервера требуется лишь очень общая сетевая информация, например тип адреса.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-106">An end-user or server application normally requires only very general network information, such as address type.</span></span>

<span data-ttu-id="6e5ed-107">Некоторые распространенные типы сетей:</span><span class="sxs-lookup"><span data-stu-id="6e5ed-107">Some common types of networks:</span></span>

-   <span data-ttu-id="6e5ed-108">**POTS (обычная старая телефонная служба):** Голоса и данные передаются в аналоговом формате в *локальном цикле* и передаются в другое место.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-108">**POTS (Plain Old Telephone Service):** Voice and data are transmitted in analog format while in the *local loop* and are digitally transmitted elsewhere.</span></span> <span data-ttu-id="6e5ed-109">Как правило, по одному типу носителя на каждый вызов по одному каналу в строке.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-109">Typically, one media type per call, one channel per line.</span></span>
-   <span data-ttu-id="6e5ed-110">**ISDN (цифровая сеть интегрированных служб):** Передано в цифровом виде.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-110">**ISDN (Integrated Services Digital Network):** Transmitted digitally.</span></span> <span data-ttu-id="6e5ed-111">Скорость до 128 кбит/с в линиях интерфейса Basic Rate (Анд-ISDN) и значительно выше в линиях интерфейса основной частоты (PRI-ISDN).</span><span class="sxs-lookup"><span data-stu-id="6e5ed-111">Speeds of up to 128 Kbps on Basic Rate Interface (BRI-ISDN) lines and much higher on Primary Rate Interface (PRI-ISDN) lines.</span></span> <span data-ttu-id="6e5ed-112">По крайней мере три канала и столько же, сколько 32 каналов, для одновременной передачи голоса и данных.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-112">At least three channels and as many as 32 channels, for simultaneous, independently operated transmission of voice and data.</span></span> <span data-ttu-id="6e5ed-113">Международный стандарт.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-113">International standard.</span></span>
-   <span data-ttu-id="6e5ed-114">**T1/E1:** Передано в цифровом виде.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-114">**T1/E1:** Transmitted digitally.</span></span> <span data-ttu-id="6e5ed-115">T1 — это канал передачи с емкостью 1,544 Мбит/с, обычно используемый для соединения сетей между удаленными расстояниями.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-115">T1 is a transmission link with a capacity of 1.544 Mbps, typically used for connecting networks across remote distances.</span></span> <span data-ttu-id="6e5ed-116">В Европейского союза T1 называется E1.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-116">In the European Union T1 is called E1.</span></span>
-   <span data-ttu-id="6e5ed-117">**Переключенный 56:** Сигнал 56 кбит/с при коммутируемых телефонных линиях, но требует специального оборудования.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-117">**Switched 56:** Signaling at 56 Kbps over dial-up telephone lines, but requires special equipment.</span></span> <span data-ttu-id="6e5ed-118">Ограничено вызовами других специально оснащенных средств.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-118">Limited to calls to other specially equipped facilities.</span></span>
-   <span data-ttu-id="6e5ed-119">**Центрекс:** Централизованные сетевые службы по обычным телефонным линиям и использованию оборудования телефонной компании.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-119">**CENTREX:** Centralized network services through regular telephone lines and using telephone company equipment.</span></span> <span data-ttu-id="6e5ed-120">Специальное оборудование не требуется.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-120">No special equipment required.</span></span>
-   <span data-ttu-id="6e5ed-121">**Цифровые АТС (обмен частными филиалами) и ключевые системы:** Голоса и данные, передаваемые частным телефонным системам с помощью собственных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-121">**Digital PBXs (private branch exchanges) and key systems:** Voice and data transmitted on private telephone systems using proprietary interfaces.</span></span>
-   <span data-ttu-id="6e5ed-122">**IP-сети:** Голоса и данные, передаваемые в сети по протоколу IP (например, Интернет или интрасеть).</span><span class="sxs-lookup"><span data-stu-id="6e5ed-122">**IP Networks:** Voice and data transmitted on networks using the Internet Protocol (IP), such as the Internet itself or a corporate intranet.</span></span>

<span data-ttu-id="6e5ed-123">Обратите внимание, что здесь представлен не полный список.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-123">Please note that this list is not exhaustive.</span></span> <span data-ttu-id="6e5ed-124">Любой механизм сетевого транспорта может поддерживаться с учетом соответствующих поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="6e5ed-124">Any network transport mechanism can be supported, given appropriate service providers.</span></span>

 

 



