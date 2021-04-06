---
description: Распределитель поверхности ВБИ
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Распределитель поверхности ВБИ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815257"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="a6b0b-103">Распределитель поверхности ВБИ</span><span class="sxs-lookup"><span data-stu-id="a6b0b-103">VBI Surface Allocator</span></span>

<span data-ttu-id="a6b0b-104">Распределитель поверхности ВБИ управляет выделением буферов ВБИ в аналоговых телевизионных диаграммах с помощью аппаратных сценариев записи видеопортов.</span><span class="sxs-lookup"><span data-stu-id="a6b0b-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="a6b0b-105">При использовании таких устройств, как декодер Bt829, буфер кадров может содержать несколько буферов записи ВБИ, доступ к которым осуществляется через собственный механизм на основе оборудования, известный как универсальный порт видео.</span><span class="sxs-lookup"><span data-stu-id="a6b0b-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="a6b0b-106">Фильтр распределителя ВБИ Surface соединяется дальше от фильтра записи и не имеет выходного ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="a6b0b-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="a6b0b-107">Фильтр тесно работает с [микшером наложения](overlay-mixer-filter.md) (с помощью DirectDraw) для выполнения согласованных операций с аппаратным портом оборудования, используя тот же ограниченный буфер памяти проигрывателя SVGA.</span><span class="sxs-lookup"><span data-stu-id="a6b0b-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a6b0b-108">Интерфейсы фильтра</span><span class="sxs-lookup"><span data-stu-id="a6b0b-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="a6b0b-109">**ибасефилтер**</span><span class="sxs-lookup"><span data-stu-id="a6b0b-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="a6b0b-110">Типы носителей входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a6b0b-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="a6b0b-111">МУЛЬТИМЕДИЙное \_ видео, медиасубтипе \_ впвби</span><span class="sxs-lookup"><span data-stu-id="a6b0b-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="a6b0b-112">Интерфейсы входных закрепления</span><span class="sxs-lookup"><span data-stu-id="a6b0b-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="a6b0b-113">**икспропертисет**</span><span class="sxs-lookup"><span data-stu-id="a6b0b-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="a6b0b-114">Типы носителей для выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a6b0b-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="a6b0b-115">MEDIATYPE \_ null, медиасубтипе \_ null.</span><span class="sxs-lookup"><span data-stu-id="a6b0b-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="a6b0b-116">(Ни один из контактов не подключается к выходному ПИН-коду.)</span><span class="sxs-lookup"><span data-stu-id="a6b0b-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="a6b0b-117">Интерфейсы выходного ПИН-кода</span><span class="sxs-lookup"><span data-stu-id="a6b0b-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a6b0b-118">Не применяется</span><span class="sxs-lookup"><span data-stu-id="a6b0b-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="a6b0b-119">Фильтровать CLSID</span><span class="sxs-lookup"><span data-stu-id="a6b0b-119">Filter CLSID</span></span>                             | <span data-ttu-id="a6b0b-120">\_ВБИСУРФАЦЕС CLSID</span><span class="sxs-lookup"><span data-stu-id="a6b0b-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="a6b0b-121">CLSID страницы свойств</span><span class="sxs-lookup"><span data-stu-id="a6b0b-121">Property Page CLSID</span></span>                      | <span data-ttu-id="a6b0b-122">Нет страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="a6b0b-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="a6b0b-123">Исполняемый объект</span><span class="sxs-lookup"><span data-stu-id="a6b0b-123">Executable</span></span>                               | <span data-ttu-id="a6b0b-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="a6b0b-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="a6b0b-125">Заслуживают</span><span class="sxs-lookup"><span data-stu-id="a6b0b-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="a6b0b-126">неуспешный \_ режим</span><span class="sxs-lookup"><span data-stu-id="a6b0b-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="a6b0b-127">Категория фильтра</span><span class="sxs-lookup"><span data-stu-id="a6b0b-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a6b0b-128">\_ЛЕГАЦИАМФИЛТЕРКАТЕГОРИ CLSID</span><span class="sxs-lookup"><span data-stu-id="a6b0b-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="a6b0b-129">См. также</span><span class="sxs-lookup"><span data-stu-id="a6b0b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a6b0b-130">Фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a6b0b-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



