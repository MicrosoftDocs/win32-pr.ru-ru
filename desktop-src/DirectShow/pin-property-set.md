---
description: Закрепить набор свойств
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Закрепить набор свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53955ba1f075094c4fb2f6324ed143ca54f72c2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909622"
---
# <a name="pin-property-set"></a><span data-ttu-id="d1ea4-103">Закрепить набор свойств</span><span class="sxs-lookup"><span data-stu-id="d1ea4-103">Pin Property Set</span></span>

<span data-ttu-id="d1ea4-104">Набор свойств закрепления Возвращает категорию закрепления для ПИН-кода в фильтре.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-104">The pin property set returns the pin category for a pin on a filter.</span></span> <span data-ttu-id="d1ea4-105">Категория задается фильтром при создании ПИН-кода. Категория указывает, какой тип данных будет доставлен или получен ПИН-кодом.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-105">The category is set by the filter when it creates the pin; the category indicates what type of data the pin is delivered or receives by this pin.</span></span>



| <span data-ttu-id="d1ea4-106">Метка</span><span class="sxs-lookup"><span data-stu-id="d1ea4-106">Label</span></span> | <span data-ttu-id="d1ea4-107">Значение</span><span class="sxs-lookup"><span data-stu-id="d1ea4-107">Value</span></span> |
|-------------------|----------------------|
| <span data-ttu-id="d1ea4-108">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="d1ea4-108">Property Set GUID</span></span> | <span data-ttu-id="d1ea4-109">**\_ПИН-код ампропсетид**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-109">**AMPROPSETID\_Pin**</span></span> |



 



| <span data-ttu-id="d1ea4-110">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="d1ea4-110">Property ID</span></span>                   | <span data-ttu-id="d1ea4-111">Описание</span><span class="sxs-lookup"><span data-stu-id="d1ea4-111">Description</span></span>                      |
|-------------------------------|----------------------------------|
| <span data-ttu-id="d1ea4-112">**\_Категория закрепления ампроперти \_**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-112">**AMPROPERTY\_PIN\_CATEGORY**</span></span> | <span data-ttu-id="d1ea4-113">Задает категорию ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-113">Specifies the category of a pin.</span></span> |



 

<span data-ttu-id="d1ea4-114">DirectShow определяет следующие категории закрепления в файле заголовка UUID. h.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-114">DirectShow defines the following pin categories in the Uuids.h header file.</span></span>



| <span data-ttu-id="d1ea4-115">GUID категории</span><span class="sxs-lookup"><span data-stu-id="d1ea4-115">Category GUID</span></span>                     | <span data-ttu-id="d1ea4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="d1ea4-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ea4-117">**закрепить \_ категорию \_ аналогвидеоин**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-117">**PIN\_CATEGORY\_ANALOGVIDEOIN**</span></span>  | <span data-ttu-id="d1ea4-118">Входной закрепления фильтра захвата, который принимает его аналоговый и дигитайзер.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-118">Input pin of the capture filter that takes analog and digitizes it.</span></span>                                                                                                                                                                                                                                                     |
| <span data-ttu-id="d1ea4-119">**закрепить \_ \_ запись категорий**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-119">**PIN\_CATEGORY\_CAPTURE**</span></span>        | <span data-ttu-id="d1ea4-120">Захватить ПИН-код.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-120">Capture pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d1ea4-121">**закрепить \_ категорию \_ CC**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-121">**PIN\_CATEGORY\_CC**</span></span>             | <span data-ttu-id="d1ea4-122">Закрепление предоставления данных о закрытых субтитрах из строки 21.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-122">Pin providing closed captioning data from Line 21.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d1ea4-123">**закрепить \_ категорию \_ EDS**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-123">**PIN\_CATEGORY\_EDS**</span></span>            | <span data-ttu-id="d1ea4-124">Закрепление предоставления расширенных служб данных (строка 21, даже поля).</span><span class="sxs-lookup"><span data-stu-id="d1ea4-124">Pin providing Extended Data Services (Line 21, even fields).</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d1ea4-125">**закрепить \_ категорию \_ набтс**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-125">**PIN\_CATEGORY\_NABTS**</span></span>          | <span data-ttu-id="d1ea4-126">ПИН-код, предоставляющий стандартные данные для Северной Америки видеотекст.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-126">Pin providing North American Videotext Standard data.</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d1ea4-127">**\_ \_ Предварительный просмотр категории закрепления**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-127">**PIN\_CATEGORY\_PREVIEW**</span></span>        | <span data-ttu-id="d1ea4-128">Предварительный просмотр ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-128">Preview pin.</span></span>                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d1ea4-129">**ПИН-код \_ категории \_**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-129">**PIN\_CATEGORY\_STILL**</span></span>          | <span data-ttu-id="d1ea4-130">ПИН-код, который предоставляет образ.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-130">Pin that provides a still image.</span></span> <span data-ttu-id="d1ea4-131">ПИН-код записи фильтра должен быть подключен перед подключением ПИН-кода по прежнему образу.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-131">The filter's capture pin must be connected before the still-image pin is connected.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="d1ea4-132">**закрепить \_ категорию \_ телетекста**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-132">**PIN\_CATEGORY\_TELETEXT**</span></span>       | <span data-ttu-id="d1ea4-133">Закрепление телетекста (вариант субтитров).</span><span class="sxs-lookup"><span data-stu-id="d1ea4-133">Pin providing teletext (a closed captioning variant).</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d1ea4-134">**закрепить \_ временной код категории \_**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-134">**PIN\_CATEGORY\_TIMECODE**</span></span>       | <span data-ttu-id="d1ea4-135">Закрепление предоставления данных кода времени.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-135">Pin providing timecode data.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="d1ea4-136">**закрепить \_ категорию \_ ВБИ**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-136">**PIN\_CATEGORY\_VBI**</span></span>            | <span data-ttu-id="d1ea4-137">Закрепление для предоставления вертикальных пустых данных интервала.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-137">Pin providing vertical blanking interval data.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d1ea4-138">**закрепить \_ категорию \_ видеопорт**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-138">**PIN\_CATEGORY\_VIDEOPORT**</span></span>      | <span data-ttu-id="d1ea4-139">Закрепление вывода видео, которое подключается к нулевому ПИН-коду [микшера наложения](overlay-mixer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="d1ea4-139">Video output pin to be connected to input pin zero on the [Overlay Mixer](overlay-mixer-filter.md).</span></span>                                                                                                                                                                                                                    |
| <span data-ttu-id="d1ea4-140">**закрепить \_ категорию \_ видеопорт \_ ВБИ**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-140">**PIN\_CATEGORY\_VIDEOPORT\_VBI**</span></span> | <span data-ttu-id="d1ea4-141">Закрепите для подключения к [распределительу ВБИ Surface](vbi-surface-allocator.md), фильтр распределителя ВБИ, необходимый для выделения правильной видеопамяти для таких объектов, как скрытые субтитры, в сценариях, где используется видеопорт.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-141">Pin to be connected to the [VBI Surface Allocator](vbi-surface-allocator.md), the VBI surface allocator filter that is needed to allocate the correct video memory for things like closed captioning overlays in scenarios where a video port is being used.</span></span> <span data-ttu-id="d1ea4-142">В сценариях PCI, IEEE 1394 и USB этот фильтр не используется.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-142">PCI, IEEE 1394, and USB scenarios do not use this filter.</span></span> |
| <span data-ttu-id="d1ea4-143">**\_ \_ запись копии пиннаме \_ видео**</span><span class="sxs-lookup"><span data-stu-id="d1ea4-143">**PINNAME\_VIDEO\_CC\_CAPTURE**</span></span>   | <span data-ttu-id="d1ea4-144">Оборудование. закрепление для срезов с замкнутым титром</span><span class="sxs-lookup"><span data-stu-id="d1ea4-144">Hardware slicing closed-captioning pin</span></span>                                                                                                                                                                                                                                                                                  |



 

<span data-ttu-id="d1ea4-145">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-145">This property is read-only.</span></span>

### <a name="example-code"></a><span data-ttu-id="d1ea4-146">Пример кода</span><span class="sxs-lookup"><span data-stu-id="d1ea4-146">Example Code</span></span>

<span data-ttu-id="d1ea4-147">В следующем коде показано, как проверить, поддерживает ли ПИН-код этот набор свойств, и, если да, как получить категорию ПИН-кода:</span><span class="sxs-lookup"><span data-stu-id="d1ea4-147">The following code shows how to check whether a pin supports this property set, and if so, how to obtain the pin category:</span></span>


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
> <span data-ttu-id="d1ea4-148">В этом примере функция [саферелеасе](../medfound/saferelease.md) используется для высвобождения указателей интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d1ea4-148">This example uses the [SafeRelease](../medfound/saferelease.md) function to release interface pointers.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="d1ea4-149">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="d1ea4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1ea4-150">Требования к ПИН-коду для фильтров захвата</span><span class="sxs-lookup"><span data-stu-id="d1ea4-150">Pin Requirements for Capture Filters</span></span>](pin-requirements-for-capture-filters.md)
</dt> <dt>

[<span data-ttu-id="d1ea4-151">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="d1ea4-151">Property Sets</span></span>](property-sets.md)
</dt> <dt>

[<span data-ttu-id="d1ea4-152">Работа с категориями ПИН-кодов</span><span class="sxs-lookup"><span data-stu-id="d1ea4-152">Working with Pin Categories</span></span>](working-with-pin-categories.md)
</dt> </dl>

 

 
