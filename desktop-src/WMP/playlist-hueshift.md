---
title: Список воспроизведения. Хуешифт
description: Атрибут Хуешифт указывает или получает величину, на которую смещается оттенок раскрывающихся изображений.
ms.assetid: 9d4d8b73-527e-43f3-a921-0576b8897918
keywords:
- Проигрыватель Windows Media Player. Хуешифт
topic_type:
- apiref
api_name:
- PLAYLIST.hueShift
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99e9dbe89989ddd8f02d67ac8f14532b9b1fbf15
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704132"
---
# <a name="playlisthueshift"></a><span data-ttu-id="b214b-104">Список воспроизведения. Хуешифт</span><span class="sxs-lookup"><span data-stu-id="b214b-104">PLAYLIST.hueShift</span></span>

<span data-ttu-id="b214b-105">Атрибут **хуешифт** указывает или получает величину, на которую смещается оттенок раскрывающихся изображений.</span><span class="sxs-lookup"><span data-stu-id="b214b-105">The **hueShift** attribute specifies or retrieves the amount by which the hue of the drop-down images is shifted.</span></span>

``` syntax
        elementID.hueShift
```

## <a name="possible-values"></a><span data-ttu-id="b214b-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="b214b-106">Possible Values</span></span>

<span data-ttu-id="b214b-107">Этот атрибут является **числом** для чтения и записи (**float**) со значением в диапазоне от 0,0 до 360,0 со значением по умолчанию 0,0.</span><span class="sxs-lookup"><span data-stu-id="b214b-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 360.0 with a default value of 0.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b214b-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b214b-108">Remarks</span></span>

<span data-ttu-id="b214b-109">Этот атрибут изменяет значение оттенка изображений, заданных атрибутами **дропдовнбаккграундимаже** и **дропдовнимаже** , если они заданы и ссылаются на 8-битные изображения BMP.</span><span class="sxs-lookup"><span data-stu-id="b214b-109">This attribute changes the hue value of the images specified by the **dropDownBackgroundImage** and **dropDownImage** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="b214b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="b214b-110">Requirements</span></span>



| <span data-ttu-id="b214b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="b214b-111">Requirement</span></span> | <span data-ttu-id="b214b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b214b-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="b214b-113">Версия</span><span class="sxs-lookup"><span data-stu-id="b214b-113">Version</span></span><br/> | <span data-ttu-id="b214b-114">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b214b-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b214b-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b214b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b214b-116">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="b214b-116">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="b214b-117">**Список воспроизведения. Дропдовнбаккграундимаже**</span><span class="sxs-lookup"><span data-stu-id="b214b-117">**PLAYLIST.dropDownBackgroundImage**</span></span>](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[<span data-ttu-id="b214b-118">**Список воспроизведения. Дропдовнимаже**</span><span class="sxs-lookup"><span data-stu-id="b214b-118">**PLAYLIST.dropDownImage**</span></span>](playlist-dropdownimage.md)
</dt> <dt>

[<span data-ttu-id="b214b-119">**Список воспроизведения. насыщенность**</span><span class="sxs-lookup"><span data-stu-id="b214b-119">**PLAYLIST.saturation**</span></span>](playlist-saturation.md)
</dt> </dl>

 

 





