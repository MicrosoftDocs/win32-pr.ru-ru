---
description: Фильтр ТВ-звука
ms.assetid: 882e03d4-5574-4b0f-b965-63ff9dbb7852
title: Фильтр ТВ-звука
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 059898b0a342dd4a5bd02d2ced1fe9dd25402921
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909212"
---
# <a name="tv-audio-filter"></a><span data-ttu-id="83eff-103">Фильтр ТВ-звука</span><span class="sxs-lookup"><span data-stu-id="83eff-103">TV Audio Filter</span></span>

<span data-ttu-id="83eff-104">Фильтр ТВ-звука обеспечивает управление телевизионным декодированием, стерео или моноаурал, а также выбором дополнительного аудио программы (SAP).</span><span class="sxs-lookup"><span data-stu-id="83eff-104">The TV Audio filter provides control of television audio decoding, stereo or monoaural selection, and secondary audio program (SAP) selection.</span></span>



| <span data-ttu-id="83eff-105">Метка</span><span class="sxs-lookup"><span data-stu-id="83eff-105">Label</span></span> | <span data-ttu-id="83eff-106">Значение</span><span class="sxs-lookup"><span data-stu-id="83eff-106">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83eff-107">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="83eff-107">Filter Interfaces</span></span>                        | <span data-ttu-id="83eff-108">[**Иамтваудио**](/windows/desktop/api/Strmif/nn-strmif-iamtvaudio), **IPersistPropertyBag**, **испеЦифипропертипажес**, [**икспропертисет**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="83eff-108">[**IAMTVAudio**](/windows/desktop/api/Strmif/nn-strmif-iamtvaudio), **IPersistPropertyBag**, **ISpecifyPropertyPages**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="83eff-109">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="83eff-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="83eff-110">MEDIATYPE \_ аналогаудио</span><span class="sxs-lookup"><span data-stu-id="83eff-110">MEDIATYPE\_AnalogAudio</span></span>                                                                                                         |
| <span data-ttu-id="83eff-111">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="83eff-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="83eff-112">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="83eff-112">**IKsPropertySet**</span></span>                                                                                                             |
| <span data-ttu-id="83eff-113">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="83eff-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="83eff-114">MEDIATYPE \_ аналогаудио</span><span class="sxs-lookup"><span data-stu-id="83eff-114">MEDIATYPE\_AnalogAudio</span></span>                                                                                                         |
| <span data-ttu-id="83eff-115">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="83eff-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="83eff-116">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="83eff-116">**IKsPropertySet**</span></span>                                                                                                             |
| <span data-ttu-id="83eff-117">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="83eff-117">Filter CLSID</span></span>                             | <span data-ttu-id="83eff-118">\_ТВАУДИОФИЛТЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="83eff-118">CLSID\_TVAudioFilter</span></span>                                                                                                           |
| <span data-ttu-id="83eff-119">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="83eff-119">Property Page CLSID</span></span>                      | <span data-ttu-id="83eff-120">\_кскатегори \_ тваудио</span><span class="sxs-lookup"><span data-stu-id="83eff-120">AM\_KSCATEGORY\_TVAUDIO</span></span>                                                                                                        |
| [<span data-ttu-id="83eff-121">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="83eff-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="83eff-122">\_ \_ не \_ использовать</span><span class="sxs-lookup"><span data-stu-id="83eff-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                            |
| [<span data-ttu-id="83eff-123">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="83eff-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="83eff-124">\_АУДИОИНПУТДЕВИЦЕКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="83eff-124">CLSID\_AudioInputDeviceCategory</span></span>                                                                                                |



 

## <a name="related-topics"></a><span data-ttu-id="83eff-125">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="83eff-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83eff-126">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="83eff-126">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



