---
title: BUTTONGROUP. Маппингимаже
description: Атрибут Маппингимаже указывает или получает имя изображения, представляющего карту кнопок BUTTONGROUP.
ms.assetid: bfea52d1-0e7f-4f77-a212-d34e356a4d85
keywords:
- Проигрыватель Windows Media BUTTONGROUP. Маппингимаже
topic_type:
- apiref
api_name:
- BUTTONGROUP.mappingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4afc44a00d5ce9b15ee01d4a0dc1aff52c555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698809"
---
# <a name="buttongroupmappingimage"></a><span data-ttu-id="ab1ef-104">BUTTONGROUP. Маппингимаже</span><span class="sxs-lookup"><span data-stu-id="ab1ef-104">BUTTONGROUP.mappingImage</span></span>

<span data-ttu-id="ab1ef-105">Атрибут **маппингимаже** указывает или получает имя изображения, представляющего карту кнопок **BUTTONGROUP**.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-105">The **mappingImage** attribute specifies or retrieves the name of the image representing the button map of the **BUTTONGROUP**.</span></span>

``` syntax
        elementID.mappingImage
```

## <a name="possible-values"></a><span data-ttu-id="ab1ef-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ab1ef-106">Possible Values</span></span>

<span data-ttu-id="ab1ef-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab1ef-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab1ef-108">Remarks</span></span>

<span data-ttu-id="ab1ef-109">Это обязательный атрибут, который должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-109">This is a mandatory attribute that must be specified.</span></span>

<span data-ttu-id="ab1ef-110">Изображение сопоставления должно совпадать с размерами основного **изображения**.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-110">The mapping image should be the same dimensions as the main **image**.</span></span> <span data-ttu-id="ab1ef-111">Он представляет собой карту областей, которые щелкнули в основном изображении.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-111">It is a map of the clickable areas of the main image.</span></span> <span data-ttu-id="ab1ef-112">Создайте карту, заполняя каждую область щелчка другим цветом.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-112">Construct the map by filling each clickable area with a different color.</span></span>

<span data-ttu-id="ab1ef-113">При определении каждого **буттонелемент** назначьте его цвет из схемы с помощью атрибута **маппингколор** .</span><span class="sxs-lookup"><span data-stu-id="ab1ef-113">When defining each **BUTTONELEMENT**, designate its color from the map using the **mappingColor** attribute.</span></span> <span data-ttu-id="ab1ef-114">Например, если в основном изображении есть кнопка "присутствовать в форме", можно создать карту с областью красного знака.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-114">For example, if you have a stop-sign-shaped button graphic in the main image, you can create a map with the area of the sign colored red.</span></span> <span data-ttu-id="ab1ef-115">После этого атрибут **буттонелемент** необходимо указать как красный, чтобы сделать изображение «конец-знак» недоступным для щелчка.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-115">The **BUTTONELEMENT** attribute must then be specified as red to make the stop-sign image clickable.</span></span>

<span data-ttu-id="ab1ef-116">Поддерживаются форматы изображений BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="ab1ef-116">The supported image formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span> <span data-ttu-id="ab1ef-117">Так как Жпгс являются утерянными и поэтому подвержены непредвиденным изменениям цвета, их не рекомендуется использовать для сопоставления изображений.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-117">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for mapping images.</span></span>

## <a name="examples"></a><span data-ttu-id="ab1ef-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab1ef-118">Examples</span></span>

<span data-ttu-id="ab1ef-119">На следующем рисунке показан пример **маппингимаже** и видимого изображения, к которому он соответствует.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-119">The following illustration is an example of a **mappingImage** and the visible image it corresponds to.</span></span> <span data-ttu-id="ab1ef-120">Эти образы являются частью обложки в маленькую папку, включенную в пакет SDK.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-120">These images are part of the skin in the Tiny folder included with the SDK.</span></span>

![Пример изображения сопоставления](images/absam01m.png)![образец фонового изображения](images/absam01f.png)

<span data-ttu-id="ab1ef-123">См. *буттонелемент*. атрибут [маппингколор](buttonelement-mappingcolor.md) для примера кода, иллюстрирующий использование этого атрибута.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-123">See the *BUTTONELEMENT*.[mappingColor](buttonelement-mappingcolor.md) attribute for a code sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1ef-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ab1ef-124">Requirements</span></span>



| <span data-ttu-id="ab1ef-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ab1ef-125">Requirement</span></span> | <span data-ttu-id="ab1ef-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ab1ef-126">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ab1ef-127">Версия</span><span class="sxs-lookup"><span data-stu-id="ab1ef-127">Version</span></span><br/> | <span data-ttu-id="ab1ef-128">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="ab1ef-128">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab1ef-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab1ef-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1ef-130">**БУТТОНЕЛЕМЕНТ. Маппингколор**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-130">**BUTTONELEMENT.mappingColor**</span></span>](buttonelement-mappingcolor.md)
</dt> <dt>

[<span data-ttu-id="ab1ef-131">**BUTTONGROUP, элемент**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-131">**BUTTONGROUP Element**</span></span>](buttongroup-element.md)
</dt> <dt>

[<span data-ttu-id="ab1ef-132">**BUTTONGROUP. Image**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-132">**BUTTONGROUP.image**</span></span>](buttongroup-image.md)
</dt> <dt>

[<span data-ttu-id="ab1ef-133">**BUTTONGROUP. Транспаренциколор**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-133">**BUTTONGROUP.transparencyColor**</span></span>](buttongroup-transparencycolor.md)
</dt> </dl>

 

 





