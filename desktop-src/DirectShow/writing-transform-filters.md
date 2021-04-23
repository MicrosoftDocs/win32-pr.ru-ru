---
description: Написание фильтров преобразования
ms.assetid: ce84756b-34ee-4710-8f0f-7553733ca10a
title: Написание фильтров преобразования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d007181e437ef5691f532fec00923aa2b8012f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998697"
---
# <a name="writing-transform-filters"></a><span data-ttu-id="65747-103">Написание фильтров преобразования</span><span class="sxs-lookup"><span data-stu-id="65747-103">Writing Transform Filters</span></span>

<span data-ttu-id="65747-104">В этом разделе описывается написание фильтра преобразования, определенного как фильтр, имеющий ровно один входной ПИН-код и один выходной ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="65747-104">This section describes how to write a transform filter, defined as a filter that has exactly one input pin and one output pin.</span></span> <span data-ttu-id="65747-105">Чтобы проиллюстрировать эти шаги, в этом разделе описывается гипотетический фильтр преобразования, который выводит видео с кодировкой длины выполнения (RLE).</span><span class="sxs-lookup"><span data-stu-id="65747-105">To illustrate the steps, this section describes a hypothetical transform filter that outputs run-length encoded (RLE) video.</span></span> <span data-ttu-id="65747-106">Он не описывает сам алгоритм RLE-Encoding, а только задачи, характерные для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="65747-106">It does not describe the RLE-encoding algorithm itself, only the tasks that are specific to DirectShow.</span></span> <span data-ttu-id="65747-107">(DirectShow уже предоставляет кодек RLE через фильтр [сжатия AVI](avi-compressor-filter.md) .)</span><span class="sxs-lookup"><span data-stu-id="65747-107">(DirectShow already provides an RLE codec through the [AVI Compressor](avi-compressor-filter.md) filter.)</span></span>

<span data-ttu-id="65747-108">В этом разделе предполагается, что для создания фильтров будет использоваться Библиотека базовых классов DirectShow.</span><span class="sxs-lookup"><span data-stu-id="65747-108">This section assumes that you will use the DirectShow base class library to create filters.</span></span> <span data-ttu-id="65747-109">Хотя можно написать фильтр без него, настоятельно рекомендуется использовать библиотеку базовых классов.</span><span class="sxs-lookup"><span data-stu-id="65747-109">Although you can write a filter without it, the base class library is strongly recommended.</span></span>

> [!Note]  
> <span data-ttu-id="65747-110">Прежде чем писать фильтр преобразования, подумайте, будет ли объект мультимедиа DirectX (DMO) соответствовать вашим требованиям.</span><span class="sxs-lookup"><span data-stu-id="65747-110">Before writing a transform filter, consider whether a DirectX Media Object (DMO) would fulfill your requirements.</span></span> <span data-ttu-id="65747-111">Дмос может выполнять многие из тех же действий, что и фильтры, и модель программирования для дмос проще.</span><span class="sxs-lookup"><span data-stu-id="65747-111">DMOs can do many of the same things as filters, and the programming model for DMOs is simpler.</span></span> <span data-ttu-id="65747-112">Дмос размещаются в DirectShow через фильтр [оболочки DMO](dmo-wrapper-filter.md) , но также можно использовать за пределами DirectShow.</span><span class="sxs-lookup"><span data-stu-id="65747-112">DMOs are hosted in DirectShow through the [DMO Wrapper](dmo-wrapper-filter.md) filter, but can also be used outside of DirectShow.</span></span> <span data-ttu-id="65747-113">Дмос теперь является рекомендуемым решением для кодировщиков и декодеров.</span><span class="sxs-lookup"><span data-stu-id="65747-113">DMOs are now the recommended solution for encoders and decoders.</span></span>

 

<span data-ttu-id="65747-114">Этот раздел содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="65747-114">This section includes the following topics:</span></span>

-   [<span data-ttu-id="65747-115">Шаг 1. Выбор базового класса</span><span class="sxs-lookup"><span data-stu-id="65747-115">Step 1. Choose a Base Class</span></span>](step-1--choose-a-base-class.md)
-   [<span data-ttu-id="65747-116">Шаг 2. Объявление класса фильтра</span><span class="sxs-lookup"><span data-stu-id="65747-116">Step 2. Declare the Filter Class</span></span>](step-2--declare-the-filter-class.md)
-   [<span data-ttu-id="65747-117">Шаг 3. Поддержка согласования типов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="65747-117">Step 3. Support Media Type Negotiation</span></span>](step-3--support-media-type-negotiation.md)
-   [<span data-ttu-id="65747-118">Шаг 4. Задание свойств распределителя</span><span class="sxs-lookup"><span data-stu-id="65747-118">Step 4. Set Allocator Properties</span></span>](step-4--set-allocator-properties.md)
-   [<span data-ttu-id="65747-119">Шаг 5. Преобразование изображения</span><span class="sxs-lookup"><span data-stu-id="65747-119">Step 5. Transform the Image</span></span>](step-5--transform-the-image.md)
-   [<span data-ttu-id="65747-120">Шаг 6. Добавление поддержки для COM</span><span class="sxs-lookup"><span data-stu-id="65747-120">Step 6. Add Support for COM</span></span>](step-6--add-support-for-com.md)

## <a name="related-topics"></a><span data-ttu-id="65747-121">См. также</span><span class="sxs-lookup"><span data-stu-id="65747-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65747-122">Создание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="65747-122">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="65747-123">Базовые классы DirectShow</span><span class="sxs-lookup"><span data-stu-id="65747-123">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> <dt>

[<span data-ttu-id="65747-124">Написание фильтров DirectShow</span><span class="sxs-lookup"><span data-stu-id="65747-124">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



