---
description: Объявление сведений о фильтре
ms.assetid: ed3c1d44-ccef-4dde-819b-f5d4d3be6d1e
title: Объявление сведений о фильтре
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8975217f1b7746b26dc5dd16ce9f4e7f694f44bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806707"
---
# <a name="declaring-filter-information"></a><span data-ttu-id="a95dc-103">Объявление сведений о фильтре</span><span class="sxs-lookup"><span data-stu-id="a95dc-103">Declaring Filter Information</span></span>

<span data-ttu-id="a95dc-104">Первый шаг — объявить сведения о фильтре, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="a95dc-104">The first step is to declare the filter information, if needed.</span></span> <span data-ttu-id="a95dc-105">DirectShow определяет следующие структуры для описания фильтров, ПИН-кодов и типов мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="a95dc-105">DirectShow defines the following structures for describing filters, pins, and media types:</span></span>



| <span data-ttu-id="a95dc-106">Структура</span><span class="sxs-lookup"><span data-stu-id="a95dc-106">Structure</span></span>                                               | <span data-ttu-id="a95dc-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a95dc-107">Description</span></span>             |
|---------------------------------------------------------|-------------------------|
| [<span data-ttu-id="a95dc-108">**\_Фильтр амовиесетуп**</span><span class="sxs-lookup"><span data-stu-id="a95dc-108">**AMOVIESETUP\_FILTER**</span></span>](amoviesetup-filter.md)       | <span data-ttu-id="a95dc-109">Описывает фильтр.</span><span class="sxs-lookup"><span data-stu-id="a95dc-109">Describes a filter.</span></span>     |
| [<span data-ttu-id="a95dc-110">**\_ПИН-код амовиесетуп**</span><span class="sxs-lookup"><span data-stu-id="a95dc-110">**AMOVIESETUP\_PIN**</span></span>](amoviesetup-pin.md)             | <span data-ttu-id="a95dc-111">Описывает ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="a95dc-111">Describes a pin.</span></span>        |
| [<span data-ttu-id="a95dc-112">**АМОВИЕСЕТУП \_ MEDIATYPE**</span><span class="sxs-lookup"><span data-stu-id="a95dc-112">**AMOVIESETUP\_MEDIATYPE**</span></span>](amoviesetup-mediatype.md) | <span data-ttu-id="a95dc-113">Описывает тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a95dc-113">Describes a media type.</span></span> |



 

<span data-ttu-id="a95dc-114">Эти структуры являются вложенными.</span><span class="sxs-lookup"><span data-stu-id="a95dc-114">These structures are nested.</span></span> <span data-ttu-id="a95dc-115">Структура **\_ фильтра амовеиесетуп** имеет указатель на массив амовиесетупных координатных структур, и каждый из них имеет указатель на массив из **амовеиесетупных структур \_ MEDIATYPE** . **\_**</span><span class="sxs-lookup"><span data-stu-id="a95dc-115">The **AMOVEIESETUP\_FILTER** structure has a pointer to an array of **AMOVIESETUP\_PIN** structures, and each of these has a pointer to an array of **AMOVEIESETUP\_MEDIATYPE** structures.</span></span> <span data-ttu-id="a95dc-116">Вместе эти структуры предоставляют достаточно информации для того, чтобы интерфейс [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) обнаружил фильтр.</span><span class="sxs-lookup"><span data-stu-id="a95dc-116">Taken together, these structures provide enough information for the [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) interface to locate a filter.</span></span> <span data-ttu-id="a95dc-117">Они не являются полным описанием фильтра.</span><span class="sxs-lookup"><span data-stu-id="a95dc-117">They are not a complete description of a filter.</span></span> <span data-ttu-id="a95dc-118">Например, если фильтр создает несколько экземпляров одного и того же ПИН-кода, следует объявить для него только одну [**амовиесетупую структуру \_ ПИН**](amoviesetup-pin.md) -кода.</span><span class="sxs-lookup"><span data-stu-id="a95dc-118">For example, if the filter creates multiple instances of the same pin, you should declare only one [**AMOVIESETUP\_PIN**](amoviesetup-pin.md) structure for that pin.</span></span> <span data-ttu-id="a95dc-119">Кроме того, фильтр не требуется для поддержки каждого сочетания типов файлов мультимедиа, которые он регистрирует. Кроме того, не требуется регистрировать каждый поддерживаемый тип мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a95dc-119">Also, a filter is not required to support every combination of media types that it registers; nor is required to register every media type that it supports.</span></span>

<span data-ttu-id="a95dc-120">Объявите структуры Set-up в виде глобальных переменных в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="a95dc-120">Declare the set-up structures as global variables within your DLL.</span></span> <span data-ttu-id="a95dc-121">В следующем примере показан фильтр с одним выходным закреплением:</span><span class="sxs-lookup"><span data-stu-id="a95dc-121">The following example shows a filter with one output pin:</span></span>


```C++
static const WCHAR g_wszName[] = L"Some Filter";

AMOVIESETUP_MEDIATYPE sudMediaTypes[] = {
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB24 },
    { &MEDIATYPE_Video, &MEDIASUBTYPE_RGB32 },
};

AMOVIESETUP_PIN sudOutputPin = {
    L"",            // Obsolete, not used.
    FALSE,          // Is this pin rendered?
    TRUE,           // Is it an output pin?
    FALSE,          // Can the filter create zero instances?
    FALSE,          // Does the filter create multiple instances?
    &GUID_NULL,     // Obsolete.
    NULL,           // Obsolete.
    2,              // Number of media types.
    sudMediaTypes   // Pointer to media types.
};

AMOVIESETUP_FILTER sudFilterReg = {
    &CLSID_SomeFilter,      // Filter CLSID.
    g_wszName,              // Filter name.
    MERIT_NORMAL,           // Merit.
    1,                      // Number of pin types.
    &sudOutputPin           // Pointer to pin information.
};
```



<span data-ttu-id="a95dc-122">Имя фильтра объявляется как статическая глобальная переменная, так как она будет использоваться в других местах.</span><span class="sxs-lookup"><span data-stu-id="a95dc-122">The filter name is declared as a static global variable, because it will be used again elsewhere.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a95dc-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a95dc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a95dc-124">Как зарегистрировать фильтры DirectShow</span><span class="sxs-lookup"><span data-stu-id="a95dc-124">How to Register DirectShow Filters</span></span>](how-to-register-directshow-filters.md)
</dt> </dl>

 

 



