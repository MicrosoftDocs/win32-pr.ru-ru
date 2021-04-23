---
description: Фильтр WST декодера
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Фильтр WST декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908482"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="7885a-103">Фильтр WST декодера</span><span class="sxs-lookup"><span data-stu-id="7885a-103">WST Decoder Filter</span></span>

<span data-ttu-id="7885a-104">Этот компонент был удален из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="7885a-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="7885a-105">Он доступен для использования в операционных системах Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="7885a-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="7885a-106">Начиная с Windows Vista, DirectShow не предоставляет фильтр для расшифровки стандартного телетекста (WST).</span><span class="sxs-lookup"><span data-stu-id="7885a-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="7885a-107">WST декодер — это фильтр в режиме ядра, который принимает декодированные стандартные телетекстовые телепрограммы из [кодека WST](wst-codec-filter.md) и доставляет точечные рисунки для крепления 2 в [микшере наложения](overlay-mixer-filter.md) с помощью шрифтов, предоставляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="7885a-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="7885a-108">В настоящее время поддерживаются только Западноевропейские языки; в настоящее время шрифты Юникода не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="7885a-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="7885a-109">Этот фильтр можно автоматически добавить в граф, вызвав метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), используя выходной ПИН-код WST.</span><span class="sxs-lookup"><span data-stu-id="7885a-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



| <span data-ttu-id="7885a-110">Метка</span><span class="sxs-lookup"><span data-stu-id="7885a-110">Label</span></span> | <span data-ttu-id="7885a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="7885a-111">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="7885a-112">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="7885a-112">Filter Interfaces</span></span>                        | <span data-ttu-id="7885a-113">ИспеЦифипропертипажес, [ **иамвстдекодер**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="7885a-113">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="7885a-114">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7885a-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="7885a-115">MEDIATYPE \_ ВБИ, медиасубтипе \_ телетекст</span><span class="sxs-lookup"><span data-stu-id="7885a-115">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="7885a-116">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="7885a-116">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="7885a-117">**ипин**</span><span class="sxs-lookup"><span data-stu-id="7885a-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="7885a-118">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7885a-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="7885a-119">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="7885a-119">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="7885a-120">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="7885a-120">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="7885a-121">**ипин**</span><span class="sxs-lookup"><span data-stu-id="7885a-121">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="7885a-122">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="7885a-122">Filter CLSID</span></span>                             | <span data-ttu-id="7885a-123">\_ВСТДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="7885a-123">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="7885a-124">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="7885a-124">Property Page CLSID</span></span>                      | <span data-ttu-id="7885a-125">\_ВСТДЕКОДЕРПРОПЕРТИПАЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="7885a-125">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="7885a-126">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="7885a-126">Executable</span></span>                               | <span data-ttu-id="7885a-127">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="7885a-127">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="7885a-128">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="7885a-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="7885a-129">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="7885a-129">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="7885a-130">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="7885a-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="7885a-131">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="7885a-131">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="7885a-132">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="7885a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7885a-133">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="7885a-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="7885a-134">Просмотр стандартного телетекста в мире</span><span class="sxs-lookup"><span data-stu-id="7885a-134">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



