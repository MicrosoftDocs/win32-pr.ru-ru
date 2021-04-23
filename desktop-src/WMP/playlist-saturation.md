---
title: Список воспроизведения. насыщенность
description: Атрибут насыщенности указывает или получает значение насыщенности раскрывающихся изображений.
ms.assetid: 4c5dd3d9-828a-45c9-896a-9a702d354544
keywords:
- Проигрыватель Windows Media в списке воспроизведения. насыщенность
topic_type:
- apiref
api_name:
- PLAYLIST.saturation
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eb53afeafb0754f0e754f68fd5ff785eaade8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704255"
---
# <a name="playlistsaturation"></a><span data-ttu-id="954d0-104">Список воспроизведения. насыщенность</span><span class="sxs-lookup"><span data-stu-id="954d0-104">PLAYLIST.saturation</span></span>

<span data-ttu-id="954d0-105">Атрибут **насыщенности** указывает или получает значение насыщенности раскрывающихся изображений.</span><span class="sxs-lookup"><span data-stu-id="954d0-105">The **saturation** attribute specifies or retrieves the saturation value of the drop-down images.</span></span>

``` syntax
        elementID.saturation
```

## <a name="possible-values"></a><span data-ttu-id="954d0-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="954d0-106">Possible Values</span></span>

<span data-ttu-id="954d0-107">Этот атрибут является **числом** для чтения и записи (**float**) со значением в диапазоне от 0,0 до 2,0 со значением по умолчанию 1,0.</span><span class="sxs-lookup"><span data-stu-id="954d0-107">This attribute is a read/write **Number** (**float**) with a value ranging from 0.0 to 2.0 with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="954d0-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="954d0-108">Remarks</span></span>

<span data-ttu-id="954d0-109">Этот атрибут изменяет значение насыщенности изображений, заданных атрибутами **дропдовнбаккграундимаже** и **дропдовнимаже** , если они заданы и ссылаются на 8-битные изображения BMP.</span><span class="sxs-lookup"><span data-stu-id="954d0-109">This attribute changes the saturation value of the images specified by the **dropDownBackgroundImage** and **dropDownImage** attributes if they have been specified and they refer to 8-bit BMP images.</span></span>

## <a name="requirements"></a><span data-ttu-id="954d0-110">Требования</span><span class="sxs-lookup"><span data-stu-id="954d0-110">Requirements</span></span>



| <span data-ttu-id="954d0-111">Требование</span><span class="sxs-lookup"><span data-stu-id="954d0-111">Requirement</span></span> | <span data-ttu-id="954d0-112">Значение</span><span class="sxs-lookup"><span data-stu-id="954d0-112">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="954d0-113">Версия</span><span class="sxs-lookup"><span data-stu-id="954d0-113">Version</span></span><br/> | <span data-ttu-id="954d0-114">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="954d0-114">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="954d0-115">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="954d0-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="954d0-116">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="954d0-116">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> <dt>

[<span data-ttu-id="954d0-117">**Список воспроизведения. Дропдовнбаккграундимаже**</span><span class="sxs-lookup"><span data-stu-id="954d0-117">**PLAYLIST.dropDownBackgroundImage**</span></span>](playlist-dropdownbackgroundimage.md)
</dt> <dt>

[<span data-ttu-id="954d0-118">**Список воспроизведения. Дропдовнимаже**</span><span class="sxs-lookup"><span data-stu-id="954d0-118">**PLAYLIST.dropDownImage**</span></span>](playlist-dropdownimage.md)
</dt> <dt>

[<span data-ttu-id="954d0-119">**Список воспроизведения. Хуешифт**</span><span class="sxs-lookup"><span data-stu-id="954d0-119">**PLAYLIST.hueShift**</span></span>](playlist-hueshift.md)
</dt> </dl>

 

 





