---
description: Распределитель поверхности ВБИ
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Распределитель поверхности ВБИ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909012"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="ed250-103">Распределитель поверхности ВБИ</span><span class="sxs-lookup"><span data-stu-id="ed250-103">VBI Surface Allocator</span></span>

<span data-ttu-id="ed250-104">Распределитель поверхности ВБИ управляет выделением буферов ВБИ в аналоговых телевизионных диаграммах с помощью аппаратных сценариев записи видеопортов.</span><span class="sxs-lookup"><span data-stu-id="ed250-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="ed250-105">При использовании таких устройств, как декодер Bt829, буфер кадров может содержать несколько буферов записи ВБИ, доступ к которым осуществляется через собственный механизм на основе оборудования, известный как универсальный порт видео.</span><span class="sxs-lookup"><span data-stu-id="ed250-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="ed250-106">Фильтр распределителя ВБИ Surface соединяется дальше от фильтра записи и не имеет выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="ed250-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="ed250-107">Фильтр тесно работает с [микшером наложения](overlay-mixer-filter.md) (с помощью DirectDraw) для выполнения согласованных операций с аппаратным портом оборудования, используя тот же ограниченный буфер памяти проигрывателя SVGA.</span><span class="sxs-lookup"><span data-stu-id="ed250-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="ed250-108">Метка</span><span class="sxs-lookup"><span data-stu-id="ed250-108">Label</span></span> | <span data-ttu-id="ed250-109">Значение</span><span class="sxs-lookup"><span data-stu-id="ed250-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ed250-110">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="ed250-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="ed250-111">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="ed250-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="ed250-112">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="ed250-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="ed250-113">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ впвби</span><span class="sxs-lookup"><span data-stu-id="ed250-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="ed250-114">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="ed250-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="ed250-115">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="ed250-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="ed250-116">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="ed250-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="ed250-117">MEDIATYPE \_ null, медиасубтипе \_ null.</span><span class="sxs-lookup"><span data-stu-id="ed250-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="ed250-118">(Ни один из контактов не подключается к выходному ПИН-коду.)</span><span class="sxs-lookup"><span data-stu-id="ed250-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="ed250-119">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="ed250-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="ed250-120">Не применяется</span><span class="sxs-lookup"><span data-stu-id="ed250-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="ed250-121">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="ed250-121">Filter CLSID</span></span>                             | <span data-ttu-id="ed250-122">\_ВБИСУРФАЦЕС CLSID</span><span class="sxs-lookup"><span data-stu-id="ed250-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="ed250-123">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="ed250-123">Property Page CLSID</span></span>                      | <span data-ttu-id="ed250-124">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="ed250-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="ed250-125">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="ed250-125">Executable</span></span>                               | <span data-ttu-id="ed250-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="ed250-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="ed250-127">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="ed250-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="ed250-128">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="ed250-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="ed250-129">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="ed250-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="ed250-130">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="ed250-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="ed250-131">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="ed250-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed250-132">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="ed250-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



