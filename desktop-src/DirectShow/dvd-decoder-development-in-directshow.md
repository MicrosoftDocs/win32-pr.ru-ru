---
description: Разработка декодеров DVD в DirectShow
ms.assetid: c00ff132-fee1-47b5-8a8a-df7cb920ad89
title: Разработка декодеров DVD в DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3de64b3c1d91dbf5f22ba3e4b4ae8fe78edda5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495576"
---
# <a name="dvd-decoder-development-in-directshow"></a><span data-ttu-id="b99be-103">Разработка декодеров DVD в DirectShow</span><span class="sxs-lookup"><span data-stu-id="b99be-103">DVD Decoder Development in DirectShow</span></span>

<span data-ttu-id="b99be-104">В этом разделе содержатся ссылки на справочные страницы для всех наборов свойств и интерфейсов DirectShow, которые относятся к DVD-диску или широко используются в декодировании DVD.</span><span class="sxs-lookup"><span data-stu-id="b99be-104">This section contains pointers to the reference pages for all the DirectShow property sets and interfaces that are either DVD-specific or else used extensively in DVD decoding.</span></span> <span data-ttu-id="b99be-105">Помимо перечисленных здесь декодер и его ПИН-коды также должны поддерживать универсальные интерфейсы фильтра DirectShow, как описано в статье [написание фильтров DirectShow](writing-directshow-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b99be-105">In addition to what is listed here, a decoder and its pins must also support the generic DirectShow filter interfaces as described in [Writing DirectShow Filters](writing-directshow-filters.md).</span></span>

<span data-ttu-id="b99be-106">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="b99be-106">This section contains the following topics.</span></span>

-   [<span data-ttu-id="b99be-107">Регулятор громкости декодера</span><span class="sxs-lookup"><span data-stu-id="b99be-107">Decoder Volume Control</span></span>](decoder-volume-control.md)
-   [<span data-ttu-id="b99be-108">Поддержка смены региона DVD в Windows</span><span class="sxs-lookup"><span data-stu-id="b99be-108">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)

<span data-ttu-id="b99be-109">См. также:</span><span class="sxs-lookup"><span data-stu-id="b99be-109">See also:</span></span>

-   [<span data-ttu-id="b99be-110">**Набор свойств караоке для DVD**</span><span class="sxs-lookup"><span data-stu-id="b99be-110">**DVD Karaoke Property Set**</span></span>](dvd-karaoke-property-set.md)
-   [<span data-ttu-id="b99be-111">**Набор свойств защиты копирования DVD-дисков**</span><span class="sxs-lookup"><span data-stu-id="b99be-111">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   [<span data-ttu-id="b99be-112">**Набор свойств подизображения DVD**</span><span class="sxs-lookup"><span data-stu-id="b99be-112">**DVD Subpicture Property Set**</span></span>](dvd-subpicture-property-set.md)
-   [<span data-ttu-id="b99be-113">Закрепить набор свойств</span><span class="sxs-lookup"><span data-stu-id="b99be-113">Pin Property Set</span></span>](pin-property-set.md)
-   [<span data-ttu-id="b99be-114">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="b99be-114">**IKsPropertySet**</span></span>](ikspropertyset.md)
-   <span data-ttu-id="b99be-115">[**Ивидеофраместеп**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (только аппаратные декодеры)</span><span class="sxs-lookup"><span data-stu-id="b99be-115">[**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) (hardware decoders only)</span></span>
-   <span data-ttu-id="b99be-116">[**Ивпконфиг**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (только аппаратные декодеры)</span><span class="sxs-lookup"><span data-stu-id="b99be-116">[**IVPConfig**](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig) (hardware decoders only)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b99be-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b99be-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b99be-118">Интерфейсы и спецификации декодера</span><span class="sxs-lookup"><span data-stu-id="b99be-118">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
</dt> </dl>

 

 



