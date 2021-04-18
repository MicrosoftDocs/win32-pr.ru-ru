---
description: Закрепить набор свойств
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Закрепить набор свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104416588"
---
# <a name="pin-property-set"></a><span data-ttu-id="cd53c-103">Закрепить набор свойств</span><span class="sxs-lookup"><span data-stu-id="cd53c-103">Pin Property Set</span></span>

<span data-ttu-id="cd53c-104">Набор свойств закрепления Возвращает категорию закрепления для ПИН-кода в фильтре.</span><span class="sxs-lookup"><span data-stu-id="cd53c-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="cd53c-105">Категория задается фильтром при создании ПИН-кода. Категория указывает, какой тип данных будет доставлен или получен ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="cd53c-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



|                   |                      |
|-------------------|----------------------|
| <span data-ttu-id="cd53c-106">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="cd53c-106">Property Set GUID</span></span> | <span data-ttu-id="cd53c-107">**\_ПИН-код ампропсетид**</span><span class="sxs-lookup"><span data-stu-id="cd53c-107">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="cd53c-108">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="cd53c-108">Property ID</span></span>                   | <span data-ttu-id="cd53c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="cd53c-109">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="cd53c-110">**\_Категория закрепления ампроперти \_**</span><span class="sxs-lookup"><span data-stu-id="cd53c-110">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="cd53c-111">Задает категорию ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cd53c-111">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="cd53c-112">DirectShow определяет следующие категории закрепления в файле заголовка UUID. h.</span><span class="sxs-lookup"><span data-stu-id="cd53c-112">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="cd53c-113">GUID категории</span><span class="sxs-lookup"><span data-stu-id="cd53c-113">Category GUID</span></span>                     | <span data-ttu-id="cd53c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="cd53c-114">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd53c-115">**закрепить \_ категорию \_ аналогвидеоин**</span><span class="sxs-lookup"><span data-stu-id="cd53c-115">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="cd53c-116">Входной закрепления фильтра захвата, который принимает его аналоговый и дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="cd53c-116">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="cd53c-117">**закрепить \_ \_ запись категорий**</span><span class="sxs-lookup"><span data-stu-id="cd53c-117">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="cd53c-118">Захватить ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="cd53c-118">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cd53c-119">**закрепить \_ категорию \_ CC**</span><span class="sxs-lookup"><span data-stu-id="cd53c-119">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="cd53c-120">Закрепление предоставления данных о закрытых субтитрах из строки 21.</span><span class="sxs-lookup"><span data-stu-id="cd53c-120">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="cd53c-121">**закрепить \_ категорию \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="cd53c-121">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="cd53c-122">Закрепление предоставления расширенных служб данных (строка 21, даже поля).</span><span class="sxs-lookup"><span data-stu-id="cd53c-122">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cd53c-123">**закрепить \_ категорию \_ набтс**</span><span class="sxs-lookup"><span data-stu-id="cd53c-123">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="cd53c-124">ПИН-код, предоставляющий стандартные данные для Северной Америки видеотекст.</span><span class="sxs-lookup"><span data-stu-id="cd53c-124">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cd53c-125">**\_ \_ Предварительный просмотр категории закрепления**</span><span class="sxs-lookup"><span data-stu-id="cd53c-125">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="cd53c-126">Предварительный просмотр ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="cd53c-126">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cd53c-127">**ПИН-код \_ категории \_**</span><span class="sxs-lookup"><span data-stu-id="cd53c-127">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="cd53c-128">ПИН-код, который предоставляет образ.</span><span class="sxs-lookup"><span data-stu-id="cd53c-128">Pin that provides a still image.</span></span> <span data-ttu-id="cd53c-129">ПИН-код записи фильтра должен быть подключен перед подключением ПИН-кода по прежнему образу.</span><span class="sxs-lookup"><span data-stu-id="cd53c-129">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="cd53c-130">**закрепить \_ категорию \_ телетекста**</span><span class="sxs-lookup"><span data-stu-id="cd53c-130">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="cd53c-131">Закрепление телетекста (вариант субтитров).</span><span class="sxs-lookup"><span data-stu-id="cd53c-131">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="cd53c-132">**закрепить \_ временной код категории \_**</span><span class="sxs-lookup"><span data-stu-id="cd53c-132">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="cd53c-133">Закрепление предоставления данных кода времени.</span><span class="sxs-lookup"><span data-stu-id="cd53c-133">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="cd53c-134">**закрепить \_ категорию \_ ВБИ**</span><span class="sxs-lookup"><span data-stu-id="cd53c-134">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="cd53c-135">Закрепление для предоставления вертикальных пустых данных интервала.</span><span class="sxs-lookup"><span data-stu-id="cd53c-135">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="cd53c-136">**закрепить \_ категорию \_ видеопорт**</span><span class="sxs-lookup"><span data-stu-id="cd53c-136">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="cd53c-137">Закрепление вывода видео, которое подключается к нулевому ПИН-коду [микшера наложения](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="cd53c-137">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="cd53c-138">**закрепить \_ категорию \_ видеопорт \_ ВБИ**</span><span class="sxs-lookup"><span data-stu-id="cd53c-138">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="cd53c-139">Закрепите для подключения к [распределительу ВБИ Surface](vbi-surface-allocator.md), фильтр распределителя ВБИ, необходимый для выделения правильной видеопамяти для таких объектов, как скрытые субтитры, в сценариях, где используется видеопорт.</span><span class="sxs-lookup"><span data-stu-id="cd53c-139">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="cd53c-140">В сценариях PCI, IEEE 1394 и USB этот фильтр не используется.</span><span class="sxs-lookup"><span data-stu-id="cd53c-140">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="cd53c-141">**\_ \_ запись копии пиннаме \_ видео**</span><span class="sxs-lookup"><span data-stu-id="cd53c-141">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="cd53c-142">Оборудование. закрепление для срезов с замкнутым титром</span><span class="sxs-lookup"><span data-stu-id="cd53c-142">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="cd53c-143">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="cd53c-143">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="cd53c-144">Пример кода</span><span class="sxs-lookup"><span data-stu-id="cd53c-144">Example Code</span></span>

<span data-ttu-id="cd53c-145">В следующем коде показано, как проверить, поддерживает ли ПИН-код этот набор свойств, и, если да, как получить категорию ПИН-кода:</span><span class="sxs-lookup"><span data-stu-id="cd53c-145">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> <span data-ttu-id="cd53c-146">В этом примере функция [саферелеасе](../medfound/saferelease.md) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="cd53c-146">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="cd53c-147">См. также</span><span class="sxs-lookup"><span data-stu-id="cd53c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd53c-148">Требования к ПИН-коду для фильтров захвата</span><span class="sxs-lookup"><span data-stu-id="cd53c-148">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="cd53c-149">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="cd53c-149">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="cd53c-150">Работа с категориями ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="cd53c-150">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
