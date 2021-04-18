---
title: ВИДЕО. backgroundColor
description: Атрибут backgroundColor указывает или получает цвет фона элемента управления видео.
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- Проигрыватель Windows Media VIDEO. backgroundColor
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 992ffd881498c3670eaaf5c075db9c6432cc1496
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704541"
---
# <a name="videobackgroundcolor"></a><span data-ttu-id="c078c-104">ВИДЕО. backgroundColor</span><span class="sxs-lookup"><span data-stu-id="c078c-104">VIDEO.backgroundColor</span></span>

<span data-ttu-id="c078c-105">Атрибут **backgroundColor** указывает или получает цвет фона элемента управления видео.</span><span class="sxs-lookup"><span data-stu-id="c078c-105">The **backgroundColor** attribute specifies or retrieves the background color of the Video control.</span></span>

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a><span data-ttu-id="c078c-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="c078c-106">Possible Values</span></span>

<span data-ttu-id="c078c-107">Этот атрибут является **строкой** для чтения и записи, содержащей любое значение цвета Microsoft Internet Explorer, или значение None.</span><span class="sxs-lookup"><span data-stu-id="c078c-107">This attribute is a read/write **String** containing any Microsoft Internet Explorer color value or the value "none".</span></span> <span data-ttu-id="c078c-108">Он имеет значение по умолчанию "нет". Это означает, что при отсутствии видео, связанного с элементом управления видео, элемент управления "видео" прозрачен, а фоновый рисунок — через.</span><span class="sxs-lookup"><span data-stu-id="c078c-108">It has a default value of "none", which means that if there is no video associated with the video control, the Video control is transparent and the background shows through.</span></span>

## <a name="remarks"></a><span data-ttu-id="c078c-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c078c-109">Remarks</span></span>

<span data-ttu-id="c078c-110">Если видео меньше, чем окно, а **стретчтофит** имеет значение false, цвет фона отображается вокруг видео.</span><span class="sxs-lookup"><span data-stu-id="c078c-110">When the video is smaller than the window and **stretchToFit** is false, the background color appears around the video.</span></span>

## <a name="requirements"></a><span data-ttu-id="c078c-111">Требования</span><span class="sxs-lookup"><span data-stu-id="c078c-111">Requirements</span></span>



| <span data-ttu-id="c078c-112">Требование</span><span class="sxs-lookup"><span data-stu-id="c078c-112">Requirement</span></span> | <span data-ttu-id="c078c-113">Значение</span><span class="sxs-lookup"><span data-stu-id="c078c-113">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c078c-114">Версия</span><span class="sxs-lookup"><span data-stu-id="c078c-114">Version</span></span><br/> | <span data-ttu-id="c078c-115">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="c078c-115">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c078c-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c078c-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c078c-117">**Ссылка на цвет**</span><span class="sxs-lookup"><span data-stu-id="c078c-117">**Color Reference**</span></span>](color-reference.md)
</dt> <dt>

[<span data-ttu-id="c078c-118">**Элемент VIDEO**</span><span class="sxs-lookup"><span data-stu-id="c078c-118">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="c078c-119">**ВИДЕО. Стретчтофит**</span><span class="sxs-lookup"><span data-stu-id="c078c-119">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





