---
title: КУСТОМСЛИДЕР. Ховеримаже
description: Атрибут Ховеримаже указывает или получает изображение, которое отображается при наведении мыши на пользовательский ползунок.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- Проигрыватель Windows Media КУСТОМСЛИДЕР. Ховеримаже
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698949"
---
# <a name="customsliderhoverimage"></a><span data-ttu-id="320be-104">КУСТОМСЛИДЕР. Ховеримаже</span><span class="sxs-lookup"><span data-stu-id="320be-104">CUSTOMSLIDER.hoverImage</span></span>

<span data-ttu-id="320be-105">Атрибут **ховеримаже** указывает или получает изображение, которое отображается при наведении мыши на пользовательский ползунок.</span><span class="sxs-lookup"><span data-stu-id="320be-105">The **hoverImage** attribute specifies or retrieves the image that appears when the mouse is over the custom slider.</span></span>

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a><span data-ttu-id="320be-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="320be-106">Possible Values</span></span>

<span data-ttu-id="320be-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="320be-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="320be-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="320be-108">Remarks</span></span>

<span data-ttu-id="320be-109">Этот атрибут является необязательным.</span><span class="sxs-lookup"><span data-stu-id="320be-109">This attribute is optional.</span></span> <span data-ttu-id="320be-110">Если он не указан, будет использоваться файл, указанный в атрибуте **Image** .</span><span class="sxs-lookup"><span data-stu-id="320be-110">If it not specified, the file specified in the **image** attribute will be used.</span></span>

<span data-ttu-id="320be-111">**Ховеримаже** представляет состояние наведения указателя мыши на элемент управления кустомслидер; то есть состояние, отображаемое при наведении курсора мыши на него.</span><span class="sxs-lookup"><span data-stu-id="320be-111">The **hoverImage** represents the hover state of the CUSTOMSLIDER control; that is, the state that is shown when the mouse cursor hovers over it.</span></span> <span data-ttu-id="320be-112">Это может быть один образ или несколько изображений, представляющих различные состояния ползунка.</span><span class="sxs-lookup"><span data-stu-id="320be-112">It can be a single image or a series of images representing the various states of the slider.</span></span> <span data-ttu-id="320be-113">Если используется несколько образов, они упорядочиваются так же, как и файл **изображения**</span><span class="sxs-lookup"><span data-stu-id="320be-113">If multiple images are used, they are arranged in the same way as the **image** file</span></span>

<span data-ttu-id="320be-114">Поддерживаются следующие типы файлов изображений: BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="320be-114">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="320be-115">Требования</span><span class="sxs-lookup"><span data-stu-id="320be-115">Requirements</span></span>



| <span data-ttu-id="320be-116">Требование</span><span class="sxs-lookup"><span data-stu-id="320be-116">Requirement</span></span> | <span data-ttu-id="320be-117">Значение</span><span class="sxs-lookup"><span data-stu-id="320be-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="320be-118">Версия</span><span class="sxs-lookup"><span data-stu-id="320be-118">Version</span></span><br/> | <span data-ttu-id="320be-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="320be-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="320be-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="320be-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="320be-121">**КУСТОМСЛИДЕР, элемент**</span><span class="sxs-lookup"><span data-stu-id="320be-121">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="320be-122">**КУСТОМСЛИДЕР. Image**</span><span class="sxs-lookup"><span data-stu-id="320be-122">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





