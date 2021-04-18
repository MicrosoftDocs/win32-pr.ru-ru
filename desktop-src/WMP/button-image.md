---
title: BUTTON. Image
description: Атрибут Image указывает или получает изображение кнопки по умолчанию.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- КНОПКА. изображение проигрыватель Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698996"
---
# <a name="buttonimage"></a><span data-ttu-id="cfc43-104">BUTTON. Image</span><span class="sxs-lookup"><span data-stu-id="cfc43-104">BUTTON.image</span></span>

<span data-ttu-id="cfc43-105">Атрибут **Image** указывает или получает изображение **кнопки** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfc43-105">The **image** attribute specifies or retrieves the default image of the **BUTTON**.</span></span>

``` syntax
        elementID.image
```

## <a name="possible-values"></a><span data-ttu-id="cfc43-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="cfc43-106">Possible Values</span></span>

<span data-ttu-id="cfc43-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="cfc43-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfc43-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfc43-108">Remarks</span></span>

<span data-ttu-id="cfc43-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF (включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="cfc43-109">The supported image formats are BMP, JPG, PNG, and GIF (including animated GIFs).</span></span>

<span data-ttu-id="cfc43-110">Если изображение **кнопки** больше, чем область, заданную атрибутами **Width** и **Height** , изображение будет обрезано.</span><span class="sxs-lookup"><span data-stu-id="cfc43-110">If the **BUTTON** image is larger than the region defined by the **width** and **height** attributes, the image will be cropped.</span></span>

<span data-ttu-id="cfc43-111">Если изображение не задано, а **Высота** и **Ширина** заданы, то отображается изображение, расположенное непосредственно за этим элементом управления.</span><span class="sxs-lookup"><span data-stu-id="cfc43-111">If the image is not specified but the **height** and **width** are, then the image directly behind this control is displayed.</span></span> <span data-ttu-id="cfc43-112">Это может упростить рисование изображения в самом **представлении** , уменьшая количество отдельных необходимых файлов изображений.</span><span class="sxs-lookup"><span data-stu-id="cfc43-112">This can facilitate drawing the image on the **VIEW** itself, reducing the number of separate image files needed.</span></span>

<span data-ttu-id="cfc43-113">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="cfc43-113">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfc43-114">Требования</span><span class="sxs-lookup"><span data-stu-id="cfc43-114">Requirements</span></span>



| <span data-ttu-id="cfc43-115">Требование</span><span class="sxs-lookup"><span data-stu-id="cfc43-115">Requirement</span></span> | <span data-ttu-id="cfc43-116">Значение</span><span class="sxs-lookup"><span data-stu-id="cfc43-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="cfc43-117">Версия</span><span class="sxs-lookup"><span data-stu-id="cfc43-117">Version</span></span><br/> | <span data-ttu-id="cfc43-118">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="cfc43-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cfc43-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfc43-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfc43-120">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="cfc43-120">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





