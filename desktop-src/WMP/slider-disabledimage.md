---
title: ПОЛЗУНок. Дисабледимаже
description: Атрибут Дисабледимаже указывает или получает изображение ползунка, используемого при отключенном элементе управления "ползунок".
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- ПОЛЗУНок. Дисабледимаже Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1b90dcbd551ca0f8bb332f858eac0b69c46733
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657112"
---
# <a name="sliderdisabledimage"></a><span data-ttu-id="338a9-104">ПОЛЗУНок. Дисабледимаже</span><span class="sxs-lookup"><span data-stu-id="338a9-104">SLIDER.disabledImage</span></span>

<span data-ttu-id="338a9-105">Атрибут **дисабледимаже** указывает или получает изображение ползунка, используемого при отключенном элементе управления "ползунок".</span><span class="sxs-lookup"><span data-stu-id="338a9-105">The **disabledImage** attribute specifies or retrieves the image of the slider that is used when the slider control is disabled.</span></span>

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a><span data-ttu-id="338a9-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="338a9-106">Possible Values</span></span>

<span data-ttu-id="338a9-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="338a9-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="338a9-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="338a9-108">Remarks</span></span>

<span data-ttu-id="338a9-109">**Дисабледимаже** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="338a9-109">The **disabledImage** is optional.</span></span> <span data-ttu-id="338a9-110">Если он не указан, **фоновый** режим используется для всех отключенных состояний.</span><span class="sxs-lookup"><span data-stu-id="338a9-110">If it is not provided, the **backgroundImage** is used for all disabled states.</span></span> <span data-ttu-id="338a9-111">Если элемент управления "ползунок" отключен, изображение переднего плана не отображается.</span><span class="sxs-lookup"><span data-stu-id="338a9-111">When a slider control is disabled, no foreground image is visible.</span></span>

<span data-ttu-id="338a9-112">Поддерживаются форматы BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="338a9-112">The supported formats are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="requirements"></a><span data-ttu-id="338a9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="338a9-113">Requirements</span></span>



| <span data-ttu-id="338a9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="338a9-114">Requirement</span></span> | <span data-ttu-id="338a9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="338a9-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="338a9-116">Версия</span><span class="sxs-lookup"><span data-stu-id="338a9-116">Version</span></span><br/> | <span data-ttu-id="338a9-117">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="338a9-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="338a9-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="338a9-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="338a9-119">**Элемент SLIDER**</span><span class="sxs-lookup"><span data-stu-id="338a9-119">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="338a9-120">**ПОЛЗУНок. backgroundImage**</span><span class="sxs-lookup"><span data-stu-id="338a9-120">**SLIDER.backgroundImage**</span></span>](slider-backgroundimage.md)
</dt> </dl>

 

 





