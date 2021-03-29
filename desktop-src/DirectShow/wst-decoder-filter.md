---
description: Фильтр WST декодера
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Фильтр WST декодера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898150"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="0bf5e-103">Фильтр WST декодера</span><span class="sxs-lookup"><span data-stu-id="0bf5e-103">WST Decoder Filter</span></span>

<span data-ttu-id="0bf5e-104">Этот компонент был удален из Windows Vista и более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="0bf5e-105">Он доступен для использования в операционных системах Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="0bf5e-106">Начиная с Windows Vista, DirectShow не предоставляет фильтр для расшифровки стандартного телетекста (WST).</span><span class="sxs-lookup"><span data-stu-id="0bf5e-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="0bf5e-107">WST декодер — это фильтр в режиме ядра, который принимает декодированные стандартные телетекстовые телепрограммы из [кодека WST](wst-codec-filter.md) и доставляет точечные рисунки для крепления 2 в [микшере наложения](overlay-mixer-filter.md) с помощью шрифтов, предоставляемых корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="0bf5e-108">В настоящее время поддерживаются только Западноевропейские языки; в настоящее время шрифты Юникода не предоставляются.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="0bf5e-109">Этот фильтр можно автоматически добавить в граф, вызвав метод [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), используя выходной ПИН-код WST.</span><span class="sxs-lookup"><span data-stu-id="0bf5e-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="0bf5e-110">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="0bf5e-110">Filter Interfaces</span></span>                        | <span data-ttu-id="0bf5e-111">ИспеЦифипропертипажес, [ **иамвстдекодер**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="0bf5e-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="0bf5e-112">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="0bf5e-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="0bf5e-113">MEDIATYPE \_ ВБИ, медиасубтипе \_ телетекст</span><span class="sxs-lookup"><span data-stu-id="0bf5e-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="0bf5e-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="0bf5e-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="0bf5e-115">**ипин**</span><span class="sxs-lookup"><span data-stu-id="0bf5e-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="0bf5e-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="0bf5e-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="0bf5e-117">\_Видео MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="0bf5e-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="0bf5e-118">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="0bf5e-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="0bf5e-119">**ипин**</span><span class="sxs-lookup"><span data-stu-id="0bf5e-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="0bf5e-120">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="0bf5e-120">Filter CLSID</span></span>                             | <span data-ttu-id="0bf5e-121">\_ВСТДЕКОДЕР CLSID</span><span class="sxs-lookup"><span data-stu-id="0bf5e-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="0bf5e-122">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="0bf5e-122">Property Page CLSID</span></span>                      | <span data-ttu-id="0bf5e-123">\_ВСТДЕКОДЕРПРОПЕРТИПАЖЕ CLSID</span><span class="sxs-lookup"><span data-stu-id="0bf5e-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="0bf5e-124">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="0bf5e-124">Executable</span></span>                               | <span data-ttu-id="0bf5e-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="0bf5e-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="0bf5e-126">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="0bf5e-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="0bf5e-127">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="0bf5e-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="0bf5e-128">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="0bf5e-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0bf5e-129">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="0bf5e-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="0bf5e-130">См. также</span><span class="sxs-lookup"><span data-stu-id="0bf5e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bf5e-131">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="0bf5e-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="0bf5e-132">Просмотр стандартного телетекста в мире</span><span class="sxs-lookup"><span data-stu-id="0bf5e-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



