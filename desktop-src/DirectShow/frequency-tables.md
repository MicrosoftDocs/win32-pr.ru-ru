---
description: Частоты таблиц
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Частоты таблиц
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104139359"
---
# <a name="frequency-tables"></a><span data-ttu-id="413d3-103">Частоты таблиц</span><span class="sxs-lookup"><span data-stu-id="413d3-103">Frequency Tables</span></span>

<span data-ttu-id="413d3-104">Фильтр ТВ-тюнера (kstvtune.ax) содержит внутренний список таблиц с частотой.</span><span class="sxs-lookup"><span data-stu-id="413d3-104">The TV Tuner filter (kstvtune.ax) has an internal list of frequency tables.</span></span> <span data-ttu-id="413d3-105">Каждая таблица Frequency содержит список частот и соответствует частоте вещания или кабелей для определенной страны или региона.</span><span class="sxs-lookup"><span data-stu-id="413d3-105">Each frequency table contains a list of frequencies, and corresponds to the broadcast or cable frequencies for a given country/region.</span></span> <span data-ttu-id="413d3-106">Приложение подстраивается к определенной частоте, вызывая метод [**иамтунер::p UT \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) с индексом нужной частоты.</span><span class="sxs-lookup"><span data-stu-id="413d3-106">An application tunes to a particular frequency by calling the [**IAMTuner::put\_Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) method with the index of the desired frequency.</span></span>

<span data-ttu-id="413d3-107">Для некоторых стран и регионов номера индексов таблиц частоты сопоставляются непосредственно с номерами каналов.</span><span class="sxs-lookup"><span data-stu-id="413d3-107">For some countries/regions, the index numbers of the frequency tables map directly to channel numbers.</span></span> <span data-ttu-id="413d3-108">Однако фиксированные номера каналов не подходят для всех рынков.</span><span class="sxs-lookup"><span data-stu-id="413d3-108">Fixed channel numbers are not appropriate for all markets, however.</span></span> <span data-ttu-id="413d3-109">Например, европейские номера каналов на самом деле не используются потребителями.</span><span class="sxs-lookup"><span data-stu-id="413d3-109">For instance, the European channel numbers are not actually used by consumers.</span></span> <span data-ttu-id="413d3-110">Вместо этого потребители хотят выбирать и назначать собственные номера каналов для частот, используемых операторами вещания или кабелей в их области.</span><span class="sxs-lookup"><span data-stu-id="413d3-110">Instead, consumers expect to choose and assign their own channel numbers for the frequencies that are used by the broadcast or cable operators in their area.</span></span> <span data-ttu-id="413d3-111">В этих странах и регионах приложения не должны предоставлять номера индексов непосредственно пользователю.</span><span class="sxs-lookup"><span data-stu-id="413d3-111">For these countries/regions, applications should not expose the index numbers directly to the user.</span></span> <span data-ttu-id="413d3-112">Инстреад, приложение должно удерживать внутреннее сопоставление между номерами каналов (представленными пользователю) и индексами частоты (для настройки).</span><span class="sxs-lookup"><span data-stu-id="413d3-112">Instread, the application should keep an internal mapping between channel numbers (presented to the user) and frequency indexes (for tuning).</span></span>

<span data-ttu-id="413d3-113">Большинство операторов кабелей, не связанных с США, можно рассылать по частоте их выбора, часто смешивание частот из разных стандартов в одном и том же канале.</span><span class="sxs-lookup"><span data-stu-id="413d3-113">Most non-US cable operators are free to broadcast on frequencies of their choosing, often mixing frequencies from different standards into the same channel lineup.</span></span> <span data-ttu-id="413d3-114">Таким образом, таблица частоты "Уникабле" используется для любой страны или региона, где отсутствует стандартный центр стандартов кабельного канала.</span><span class="sxs-lookup"><span data-stu-id="413d3-114">Therefore, a "Unicable" frequency table is used for any country/region that lacks a standard cable channel standards authority.</span></span> <span data-ttu-id="413d3-115">Кроме того, предоставляется механизм переопределения отдельных частот в таблицах частоты.</span><span class="sxs-lookup"><span data-stu-id="413d3-115">Also, a mechanism is provided to override individual frequencies in the frequency tables.</span></span> <span data-ttu-id="413d3-116">Этот механизм описан в следующем разделе: [переопределение частоты](frequency-overrides.md).</span><span class="sxs-lookup"><span data-stu-id="413d3-116">This mechanism is described in the following section, [Frequency Overrides](frequency-overrides.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="413d3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="413d3-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="413d3-118">Международная Настройка аналогового ТВ</span><span class="sxs-lookup"><span data-stu-id="413d3-118">International Analog TV Tuning</span></span>](international-analog-tv-tuning.md)
</dt> </dl>

 

 



