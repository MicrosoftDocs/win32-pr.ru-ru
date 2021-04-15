---
title: Список воспроизведения. backgroundImage
description: Атрибут backgroundImage указывает или получает фоновое изображение.
ms.assetid: d4efa774-d42e-4415-a487-1e858d984075
keywords:
- Проигрыватель Windows Media. backgroundImage
topic_type:
- apiref
api_name:
- PLAYLIST.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eca04f47f6e157d5ede529c47fb6ae65b4333cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708331"
---
# <a name="playlistbackgroundimage"></a><span data-ttu-id="ca17f-104">Список воспроизведения. backgroundImage</span><span class="sxs-lookup"><span data-stu-id="ca17f-104">PLAYLIST.backgroundImage</span></span>

<span data-ttu-id="ca17f-105">Атрибут **backgroundImage** указывает или получает фоновое изображение.</span><span class="sxs-lookup"><span data-stu-id="ca17f-105">The **backgroundImage** attribute specifies or retrieves the background image.</span></span>

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a><span data-ttu-id="ca17f-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="ca17f-106">Possible Values</span></span>

<span data-ttu-id="ca17f-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="ca17f-107">This attribute is a read/write **String** containing the name of an image file.</span></span> <span data-ttu-id="ca17f-108">У него нет значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca17f-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca17f-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca17f-109">Remarks</span></span>

<span data-ttu-id="ca17f-110">Если высота и ширина изображения меньше, чем высота и ширина элемента **списка воспроизведения** , изображение будет мозаичным.</span><span class="sxs-lookup"><span data-stu-id="ca17f-110">If the image height and width are smaller than the height and width of the **PLAYLIST** element, the image is tiled.</span></span> <span data-ttu-id="ca17f-111">Поддерживаются форматы BMP, JPG, GIF и PNG.</span><span class="sxs-lookup"><span data-stu-id="ca17f-111">The supported formats are BMP, JPG, GIF and PNG.</span></span>

<span data-ttu-id="ca17f-112">Указание значения "градиент" для фонового изображения приводит к тому, что фон списка воспроизведения отображается как цветовой градиент.</span><span class="sxs-lookup"><span data-stu-id="ca17f-112">Specifying a value of "gradient" for the background image causes the background of the playlist to display as a color gradient.</span></span> <span data-ttu-id="ca17f-113">Это означает, что цвет фона постепенно переходит между [списком воспроизведения. backgroundColor](playlist-backgroundcolor.md) (в верхней части фона) и значениями [списка воспроизведения. статусколор](playlist-statuscolor.md) .</span><span class="sxs-lookup"><span data-stu-id="ca17f-113">This means the background color gradually transitions between the [PLAYLIST.backgroundColor](playlist-backgroundcolor.md) (at the top of the background) and [PLAYLIST.statusColor](playlist-statuscolor.md) values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca17f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ca17f-114">Requirements</span></span>



| <span data-ttu-id="ca17f-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ca17f-115">Requirement</span></span> | <span data-ttu-id="ca17f-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ca17f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca17f-117">Версия</span><span class="sxs-lookup"><span data-stu-id="ca17f-117">Version</span></span><br/> | <span data-ttu-id="ca17f-118">Проигрыватель Windows Media версии 7,0 или более поздней, проигрыватель Windows Media 10 для функции градиента</span><span class="sxs-lookup"><span data-stu-id="ca17f-118">Windows Media Player version 7.0 or later, Windows Media Player 10 for the gradient feature</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca17f-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca17f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca17f-120">**Элемент списка воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="ca17f-120">**PLAYLIST Element**</span></span>](playlist-element.md)
</dt> </dl>

 

 





