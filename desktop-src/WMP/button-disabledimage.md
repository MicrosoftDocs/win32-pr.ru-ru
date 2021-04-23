---
title: КНОПКА. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает изображение, отображаемое при отключенной КНОПКе.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- КНОПКА. Дисабледимаже Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694522"
---
# <a name="buttondisabledimage"></a><span data-ttu-id="e7936-104">КНОПКА. Дисабледимаже</span><span class="sxs-lookup"><span data-stu-id="e7936-104">BUTTON.disabledImage</span></span>

<span data-ttu-id="e7936-105">Атрибут **дисабледимаже** указывает или получает изображение, отображаемое при отключенной **кнопке** .</span><span class="sxs-lookup"><span data-stu-id="e7936-105">The **disabledImage** attribute specifies or retrieves the image that displays when the **BUTTON** is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="e7936-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e7936-106">Possible Values</span></span>

<span data-ttu-id="e7936-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="e7936-107">This attribute is a read/write **String** containing the image file name.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7936-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7936-108">Remarks</span></span>

<span data-ttu-id="e7936-109">Поддерживаются форматы изображений BMP, JPG, PNG и GIF.</span><span class="sxs-lookup"><span data-stu-id="e7936-109">The supported image formats are BMP, JPG, PNG, and GIF.</span></span>

<span data-ttu-id="e7936-110">Это изображение будет отображаться каждый раз, когда **отключенный** атрибут элемента управления имеет значение true.</span><span class="sxs-lookup"><span data-stu-id="e7936-110">This image will be displayed whenever the **disabled** attribute of the control is set to true.</span></span> <span data-ttu-id="e7936-111">Если отключенный образ больше, чем заданный регион, отключенный образ будет обрезан.</span><span class="sxs-lookup"><span data-stu-id="e7936-111">If the disabled image is larger than the defined region, the disabled image will be cropped.</span></span>

<span data-ttu-id="e7936-112">Если изображение не может быть получено, отображается изображение по умолчанию (изображение Красного x).</span><span class="sxs-lookup"><span data-stu-id="e7936-112">If the image cannot be retrieved, a default image (the red-x image) is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7936-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e7936-113">Requirements</span></span>



| <span data-ttu-id="e7936-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e7936-114">Requirement</span></span> | <span data-ttu-id="e7936-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e7936-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e7936-116">Версия</span><span class="sxs-lookup"><span data-stu-id="e7936-116">Version</span></span><br/> | <span data-ttu-id="e7936-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e7936-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7936-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7936-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7936-119">**BUTTON, элемент**</span><span class="sxs-lookup"><span data-stu-id="e7936-119">**BUTTON Element**</span></span>](button-element.md)
</dt> </dl>

 

 





