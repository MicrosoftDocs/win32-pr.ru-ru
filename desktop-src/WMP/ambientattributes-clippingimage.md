---
title: Амбиентаттрибутес. Клиппингимаже
description: Атрибут Клиппингимаже указывает или получает область для обрезки элемента управления.
ms.assetid: e4b51d31-f9c7-4398-983d-95867a2cab45
keywords:
- Проигрыватель Windows Media Амбиентаттрибутес. Клиппингимаже
topic_type:
- apiref
api_name:
- AmbientAttributes.clippingImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e05e05ca9c7c3efdf842ffd4297da6f9fee035d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698928"
---
# <a name="ambientattributesclippingimage"></a><span data-ttu-id="59a17-104">Амбиентаттрибутес. Клиппингимаже</span><span class="sxs-lookup"><span data-stu-id="59a17-104">AmbientAttributes.clippingImage</span></span>

<span data-ttu-id="59a17-105">Атрибут **клиппингимаже** указывает или получает область для обрезки элемента управления.</span><span class="sxs-lookup"><span data-stu-id="59a17-105">The **clippingImage** attribute specifies or retrieves the region to clip the control to.</span></span>

``` syntax
        elementID.clippingImage
```

## <a name="possible-values"></a><span data-ttu-id="59a17-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="59a17-106">Possible Values</span></span>

<span data-ttu-id="59a17-107">Этот атрибут является **строкой** для чтения и записи, указывающей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="59a17-107">This attribute is a read/write **String** indicating the image file name.</span></span> <span data-ttu-id="59a17-108">У него нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="59a17-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59a17-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59a17-109">Remarks</span></span>

<span data-ttu-id="59a17-110">Атрибут **клиппингимаже** поддерживает файлы PNG, JPG, BMP и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="59a17-110">The **clippingImage** attribute supports PNG, JPG, BMP, and GIF files (not including animated GIFs).</span></span> <span data-ttu-id="59a17-111">Так как Жпгс являются утерянными и поэтому подвержены непредвиденному изменению цвета, их не рекомендуется использовать для обрезки изображений.</span><span class="sxs-lookup"><span data-stu-id="59a17-111">Because JPGs are lossy and therefore subject to unexpected color change, they are not recommended for clipping images.</span></span>

<span data-ttu-id="59a17-112">Этот атрибут полезен, если требуется отобразить только часть изображения элемента управления, а не всю прямоугольную область.</span><span class="sxs-lookup"><span data-stu-id="59a17-112">This attribute is useful when you want to display only a part of the control image and not the entire rectangular area.</span></span> <span data-ttu-id="59a17-113">Атрибут **клиппингколор** указывает регионы обрезки изображения, которые соответствуют прозрачным нещелчкам части элемента управления.</span><span class="sxs-lookup"><span data-stu-id="59a17-113">The **clippingColor** attribute indicates the regions of the clipping image that correspond to transparent, non-clickable portions of the control.</span></span> <span data-ttu-id="59a17-114">Таким образом, элемент управления может быть любой формой.</span><span class="sxs-lookup"><span data-stu-id="59a17-114">The control can therefore be of any shape.</span></span> <span data-ttu-id="59a17-115">Для достижения лучших результатов изображение обрезки должно иметь тот же размер, что и изображение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="59a17-115">For best results, the clipping image should be the same size as the control image.</span></span>

<span data-ttu-id="59a17-116">Атрибут **клиппингимаже** не поддерживается элементами **списка воспроизведения**, **представления** и вложенного **представления** .</span><span class="sxs-lookup"><span data-stu-id="59a17-116">The **clippingImage** attribute is not supported by the **PLAYLIST**, **VIEW**, and **SUBVIEW** elements.</span></span> <span data-ttu-id="59a17-117">Обрезка изображения не будет работать с элементом **видео** , если *видео*. **окно без окон** имеет значение false или элемент **Effects** , если он имеет *эффект*. для **окон** задано значение true.</span><span class="sxs-lookup"><span data-stu-id="59a17-117">A clipping image will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

<span data-ttu-id="59a17-118">Поскольку использование обреза изображений приводит к снижению производительности, их не следует использовать, если эффективность является проблемой.</span><span class="sxs-lookup"><span data-stu-id="59a17-118">Because the use of clipping images imposes a performance penalty, they should not be used when efficiency is an issue.</span></span>

## <a name="examples"></a><span data-ttu-id="59a17-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="59a17-119">Examples</span></span>

<span data-ttu-id="59a17-120">Пример, иллюстрирующий использование этого атрибута, см. в атрибуте [буттонелемент. маппингколор](buttonelement-mappingcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="59a17-120">See the [BUTTONELEMENT.mappingColor](buttonelement-mappingcolor.md) attribute for a sample illustrating the use of this attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="59a17-121">Требования</span><span class="sxs-lookup"><span data-stu-id="59a17-121">Requirements</span></span>



| <span data-ttu-id="59a17-122">Требование</span><span class="sxs-lookup"><span data-stu-id="59a17-122">Requirement</span></span> | <span data-ttu-id="59a17-123">Значение</span><span class="sxs-lookup"><span data-stu-id="59a17-123">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="59a17-124">Версия</span><span class="sxs-lookup"><span data-stu-id="59a17-124">Version</span></span><br/> | <span data-ttu-id="59a17-125">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="59a17-125">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59a17-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59a17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59a17-127">**Атрибуты окружения**</span><span class="sxs-lookup"><span data-stu-id="59a17-127">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> <dt>

[<span data-ttu-id="59a17-128">**Амбиентаттрибутес. Клиппингколор**</span><span class="sxs-lookup"><span data-stu-id="59a17-128">**AmbientAttributes.clippingColor**</span></span>](ambientattributes-clippingcolor.md)
</dt> </dl>

 

 





