---
description: Перечисление устройств и фильтров
ms.assetid: 334bba2a-7477-4115-9ce0-d4495c1fc290
title: Перечисление устройств и фильтров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e69997a4af4f3160f0b338bc9c595adea83a5354
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894953"
---
# <a name="enumerating-devices-and-filters"></a><span data-ttu-id="3e6c5-103">Перечисление устройств и фильтров</span><span class="sxs-lookup"><span data-stu-id="3e6c5-103">Enumerating Devices and Filters</span></span>

<span data-ttu-id="3e6c5-104">Иногда приложению необходимо выбрать определенный фильтр в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-104">Sometimes an application needs to locate a particular filter on the user's system.</span></span> <span data-ttu-id="3e6c5-105">Например, приложение для записи видео может отображать список доступных устройств записи.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-105">For example, a video capture application might display a list of available capture devices.</span></span> <span data-ttu-id="3e6c5-106">Так как DirectShow использует архитектуру на основе компонентов, вы не сможете во время разработки использовать фильтры, установленные в системе пользователя.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-106">Because DirectShow uses a component-based architecture, you cannot know at design time which filters are installed on the user's system.</span></span> <span data-ttu-id="3e6c5-107">Это особенно справедливо для фильтров, представляющих аппаратные устройства.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-107">This is particularly true for filters that represent hardware devices.</span></span> <span data-ttu-id="3e6c5-108">DirectShow предоставляет два компонента, которые находят зарегистрированные фильтры:</span><span class="sxs-lookup"><span data-stu-id="3e6c5-108">DirectShow provides two components that locate registered filters:</span></span>

-   <span data-ttu-id="3e6c5-109">[Перечислитель системных устройств](system-device-enumerator.md) находит фильтры по их категориям.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-109">The [System Device Enumerator](system-device-enumerator.md) finds filters by their category.</span></span>
-   <span data-ttu-id="3e6c5-110">Средство [сопоставления фильтров](filter-mapper.md) находит фильтры в соответствии с критериями поиска, предоставленными приложением.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-110">The [Filter Mapper](filter-mapper.md) finds filters according to search criteria supplied by the application.</span></span>

<span data-ttu-id="3e6c5-111">Перечислители, обсуждаемые в этом разделе, следуют стандартной форме, используемой интерфейсами перечисления COM.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-111">The enumerators discussed in this section follow the standard form used by COM enumeration interfaces.</span></span> <span data-ttu-id="3e6c5-112">Дополнительные сведения см. в разделе «Иенумкскскскс» пакета средств разработки программного обеспечения (SDK) платформы Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-112">For more information, see the "IEnumXXXX" topic in the Microsoft Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="3e6c5-113">В этом разделе рассматриваются следующие вопросы.</span><span class="sxs-lookup"><span data-stu-id="3e6c5-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="3e6c5-114">Использование перечислителя системных устройств</span><span class="sxs-lookup"><span data-stu-id="3e6c5-114">Using the System Device Enumerator</span></span>](using-the-system-device-enumerator.md)
-   [<span data-ttu-id="3e6c5-115">Использование средства сопоставления фильтров</span><span class="sxs-lookup"><span data-stu-id="3e6c5-115">Using the Filter Mapper</span></span>](using-the-filter-mapper.md)

## <a name="related-topics"></a><span data-ttu-id="3e6c5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3e6c5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e6c5-117">Основные задачи DirectShow</span><span class="sxs-lookup"><span data-stu-id="3e6c5-117">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> </dl>

 

 



