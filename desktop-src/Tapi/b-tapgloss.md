---
description: Следующие термины полезны для понимания технологии TAPI.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: fa94cbaf-8772-4cc6-ad20-f48cbe79a20a
title: B (API телефонии)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d97debd1c11e6cc70e164e080d4e292eee8ac83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674080"
---
# <a name="b-telephony-api"></a><span data-ttu-id="8c404-103">B (API телефонии)</span><span class="sxs-lookup"><span data-stu-id="8c404-103">B (Telephony API)</span></span>

<span data-ttu-id="8c404-104">[A](a-tapgloss.md) B [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [р](h-tapgloss.md) [.](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="8c404-104">[A](a-tapgloss.md) B [C](c-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="8c404-105"><span id="tapi2.b_channel_tapgloss"></span><span id="TAPI2.B_CHANNEL_TAPGLOSS"></span>**Канал B**</span><span class="sxs-lookup"><span data-stu-id="8c404-105"><span id="tapi2.b_channel_tapgloss"></span><span id="TAPI2.B_CHANNEL_TAPGLOSS"></span>**B channel**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-106">Канал *носителя* , который является фундаментальным компонентом интерфейсов ISDN.</span><span class="sxs-lookup"><span data-stu-id="8c404-106">A *bearer* channel that is a fundamental component of ISDN interfaces.</span></span> <span data-ttu-id="8c404-107">Он включает в себя 64 000 бит/с (бит/с) в обоих направлениях, переключается в цепь и может содержать голоса или данные.</span><span class="sxs-lookup"><span data-stu-id="8c404-107">It carries 64,000 bits per second (bps) in both directions, is circuit-switched, and is able to carry either voice or data.</span></span> <span data-ttu-id="8c404-108">Дополнительные сведения см. в разделе [режим носителя](./bearer-mode-ovr.md).</span><span class="sxs-lookup"><span data-stu-id="8c404-108">For additional information, see [Bearer Mode](./bearer-mode-ovr.md).</span></span> <span data-ttu-id="8c404-109">См. раздел [*D Channel*](d-tapgloss.md), [*Integrated Services Digital Network (ISDN)*](i-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="8c404-109">See [*D channel*](d-tapgloss.md), [*Integrated Services Digital Network (ISDN)*](i-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c404-110"><span id="tapi2.band_tapgloss"></span><span id="TAPI2.BAND_TAPGLOSS"></span>**строки**</span><span class="sxs-lookup"><span data-stu-id="8c404-110"><span id="tapi2.band_tapgloss"></span><span id="TAPI2.BAND_TAPGLOSS"></span>**band**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-111">Диапазон частот между двумя определенными точками.</span><span class="sxs-lookup"><span data-stu-id="8c404-111">The range of frequencies between two defined points.</span></span>

</dd> <dt>

<span data-ttu-id="8c404-112"><span id="tapi2.bandwidth_tapgloss"></span><span id="TAPI2.BANDWIDTH_TAPGLOSS"></span>**связи**</span><span class="sxs-lookup"><span data-stu-id="8c404-112"><span id="tapi2.bandwidth_tapgloss"></span><span id="TAPI2.BANDWIDTH_TAPGLOSS"></span>**bandwidth**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-113">В связи разница между самой высокой и минимальной частотой в заданном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="8c404-113">In communications, the difference between the highest and lowest frequencies in a given range.</span></span> <span data-ttu-id="8c404-114">Например, Телефон включает пропускную способность 3000 Гц, разницу между самой низкой (300 Гц) и максимальной (3300 Гц) частотой, которую он может выполнять.</span><span class="sxs-lookup"><span data-stu-id="8c404-114">For example, a telephone accommodates a bandwidth of 3000 Hz, the difference between the lowest (300 Hz) and highest (3300 Hz) frequencies it can carry.</span></span>

</dd> <dt>

<span data-ttu-id="8c404-115"><span id="tapi2.bandwidth_allocation_control_protocol_bacp__tapgloss"></span><span id="TAPI2.BANDWIDTH_ALLOCATION_CONTROL_PROTOCOL_BACP__TAPGLOSS"></span>**Протокол управления распределением пропускной способности (BACP)**</span><span class="sxs-lookup"><span data-stu-id="8c404-115"><span id="tapi2.bandwidth_allocation_control_protocol_bacp__tapgloss"></span><span id="TAPI2.BANDWIDTH_ALLOCATION_CONTROL_PROTOCOL_BACP__TAPGLOSS"></span>**Bandwidth Allocation Control Protocol (BACP)**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-116">Набор правил, который управляет пропускной способностью по динамическим подключениям PPP с несколькими ссылками.</span><span class="sxs-lookup"><span data-stu-id="8c404-116">The set of rules that manages bandwidth over dynamic multi-link PPP connections.</span></span> <span data-ttu-id="8c404-117">См. раздел [*многоканальный PPP*](m-tapgloss.md), [*протокол PPP*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="8c404-117">See [*multi-link PPP*](m-tapgloss.md), [*point-to-point protocol (PPP)*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c404-118"><span id="tapi2.basic_rate_interface_bri_isdn__tapgloss"></span><span id="TAPI2.BASIC_RATE_INTERFACE_BRI_ISDN__TAPGLOSS"></span>**Интерфейс Basic Rate (Анд-ISDN)**</span><span class="sxs-lookup"><span data-stu-id="8c404-118"><span id="tapi2.basic_rate_interface_bri_isdn__tapgloss"></span><span id="TAPI2.BASIC_RATE_INTERFACE_BRI_ISDN__TAPGLOSS"></span>**Basic Rate Interface (BRI-ISDN)**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-119">Стандартная линия ISDN, состоящая из двух каналов B и одного канала D.</span><span class="sxs-lookup"><span data-stu-id="8c404-119">The standard ISDN line, consisting of two B channels and one D channel.</span></span> <span data-ttu-id="8c404-120">См. раздел [*интегрированная служба Digital Network (ISDN)*](i-tapgloss.md), [*интерфейс основной частоты (PRI-ISDN)*](p-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="8c404-120">See [*Integrated Services Digital Network (ISDN)*](i-tapgloss.md), [*Primary Rate Interface (PRI-ISDN)*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c404-121"><span id="tapi2.basic_telephony_tapgloss"></span><span id="TAPI2.BASIC_TELEPHONY_TAPGLOSS"></span>**Базовая телефония**</span><span class="sxs-lookup"><span data-stu-id="8c404-121"><span id="tapi2.basic_telephony_tapgloss"></span><span id="TAPI2.BASIC_TELEPHONY_TAPGLOSS"></span>**Basic Telephony**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-122">Простейший уровень службы телефонии с минимальным набором функций, который предоставляет минимальный набор функций, соответствующих обычной старой телефонной службе (POTS).</span><span class="sxs-lookup"><span data-stu-id="8c404-122">An elementary level of telephony service, with a minimal subset of features, that provides a minimum set of functions that corresponds to Plain Old Telephone Service (POTS).</span></span> <span data-ttu-id="8c404-123">Поставщики услуг TAPI необходимы для поддержки всех основных функций телефонии.</span><span class="sxs-lookup"><span data-stu-id="8c404-123">TAPI service providers are required to support all Basic Telephony functions.</span></span> <span data-ttu-id="8c404-124">См. раздел Поддержка [телефонии](./assisted-telephony-overview.md), [*Расширенная телефония*](e-tapgloss.md), [*Дополнительная телефония*](s-tapgloss.md).</span><span class="sxs-lookup"><span data-stu-id="8c404-124">See [Assisted Telephony](./assisted-telephony-overview.md), [*Extended Telephony*](e-tapgloss.md), [*Supplementary Telephony*](s-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="8c404-125"><span id="tapi2.bri_isdn_tapgloss"></span><span id="TAPI2.BRI_ISDN_TAPGLOSS"></span>**АНД-ISDN**</span><span class="sxs-lookup"><span data-stu-id="8c404-125"><span id="tapi2.bri_isdn_tapgloss"></span><span id="TAPI2.BRI_ISDN_TAPGLOSS"></span>**BRI-ISDN**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-126">См. раздел *базовый интерфейс Rate (Анд-ISDN)*.</span><span class="sxs-lookup"><span data-stu-id="8c404-126">See *Basic Rate Interface (BRI-ISDN)*.</span></span>

</dd> <dt>

<span data-ttu-id="8c404-127"><span id="tapi2.bps_tapgloss"></span><span id="TAPI2.BPS_TAPGLOSS"></span>**/**</span><span class="sxs-lookup"><span data-stu-id="8c404-127"><span id="tapi2.bps_tapgloss"></span><span id="TAPI2.BPS_TAPGLOSS"></span>**bps**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-128">Просмотр *битов в секунду (бит/с)*.</span><span class="sxs-lookup"><span data-stu-id="8c404-128">See *bits per second (bps)*.</span></span>

</dd> <dt>

<span data-ttu-id="8c404-129"><span id="tapi2.bits_per_second_bps__tapgloss"></span><span id="TAPI2.BITS_PER_SECOND_BPS__TAPGLOSS"></span>**бит в секунду (бит/с)**</span><span class="sxs-lookup"><span data-stu-id="8c404-129"><span id="tapi2.bits_per_second_bps__tapgloss"></span><span id="TAPI2.BITS_PER_SECOND_BPS__TAPGLOSS"></span>**bits per second (bps)**</span></span>
</dt> <dd>

<span data-ttu-id="8c404-130">Измерение скорости передачи, показывающее, сколько бит данных компьютера отправляется в течение одной секунды через модем по телефонной линии.</span><span class="sxs-lookup"><span data-stu-id="8c404-130">Transfer-rate measurement indicating how many bits of computer data are sent in a one-second period through a modem over a telephone line.</span></span>

</dd> </dl>

 

 
