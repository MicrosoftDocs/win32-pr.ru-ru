---
title: ВИДЕО. Zoom
description: Атрибут Zoom задает процент масштабирования видео.
ms.assetid: 71c0e5a6-f7c4-46cf-a180-083d2926ba20
keywords:
- ВИДЕО. масштаб проигрывателя Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.zoom
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b989cabcf84244976bda728d12c97697338f742
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704056"
---
# <a name="videozoom"></a><span data-ttu-id="5cab8-104">ВИДЕО. Zoom</span><span class="sxs-lookup"><span data-stu-id="5cab8-104">VIDEO.zoom</span></span>

<span data-ttu-id="5cab8-105">Атрибут **Zoom** задает процент масштабирования видео.</span><span class="sxs-lookup"><span data-stu-id="5cab8-105">The **zoom** attribute specifies the percentage by which to scale the video.</span></span>

``` syntax
        elementID.zoom
```

## <a name="possible-values"></a><span data-ttu-id="5cab8-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="5cab8-106">Possible Values</span></span>

<span data-ttu-id="5cab8-107">Этот атрибут является **числом** для чтения и записи (**длинное**) в диапазоне от 1 до максимального размера, который соответствует ширине и высоте элемента управления видео.</span><span class="sxs-lookup"><span data-stu-id="5cab8-107">This attribute is a read/write **Number** (**long**) ranging from 1 to the maximum size accommodated by the width and height of the Video control.</span></span> <span data-ttu-id="5cab8-108">Он имеет значение по умолчанию 100.</span><span class="sxs-lookup"><span data-stu-id="5cab8-108">It has a default value of 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cab8-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5cab8-109">Remarks</span></span>

<span data-ttu-id="5cab8-110">Этот атрибут нельзя использовать в сочетании с атрибутом " **полноэкранный** ".</span><span class="sxs-lookup"><span data-stu-id="5cab8-110">This attribute cannot be used in conjunction with the **fullScreen** attribute.</span></span>

<span data-ttu-id="5cab8-111">Если заданы значения **Width** и **Height** , а результирующее окно видео больше, чем воспроизводимое видео, его можно увеличить, увеличив масштаб до максимального размера, подходящим для окна.</span><span class="sxs-lookup"><span data-stu-id="5cab8-111">If **width** and **height** are specified, and the resulting video window is larger than the video being played, the video can be enlarged by scaling up to the maximum size accommodated by the window.</span></span> <span data-ttu-id="5cab8-112">Если **Ширина** и **Высота** не указаны, то **масштаб** может не превышать 100.</span><span class="sxs-lookup"><span data-stu-id="5cab8-112">If **width** and **height** are not specified, **zoom** is limited to values of 100 or less.</span></span>

<span data-ttu-id="5cab8-113">Если свойство **шринктофит** имеет значение false, то во время масштабирования видео будет изменяться пропорционально размеру доступного пространства.</span><span class="sxs-lookup"><span data-stu-id="5cab8-113">If the **shrinkToFit** property is false, the video will change proportion upon zooming, to fit itself to the available space.</span></span> <span data-ttu-id="5cab8-114">Если **шринктофит** имеет значение true, видео будет сжиматься в соответствии с наиболее ограниченным измерением, сохраняя первоначальные пропорции.</span><span class="sxs-lookup"><span data-stu-id="5cab8-114">If **shrinkToFit** is true, the video will shrink to fit within the most restrictive dimension, while retaining its original proportions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cab8-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5cab8-115">Requirements</span></span>



| <span data-ttu-id="5cab8-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5cab8-116">Requirement</span></span> | <span data-ttu-id="5cab8-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5cab8-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="5cab8-118">Версия</span><span class="sxs-lookup"><span data-stu-id="5cab8-118">Version</span></span><br/> | <span data-ttu-id="5cab8-119">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="5cab8-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cab8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5cab8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cab8-121">**Элемент VIDEO**</span><span class="sxs-lookup"><span data-stu-id="5cab8-121">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="5cab8-122">**ВИДЕО. полноэкранный режим**</span><span class="sxs-lookup"><span data-stu-id="5cab8-122">**VIDEO.fullScreen**</span></span>](video-fullscreen.md)
</dt> <dt>

[<span data-ttu-id="5cab8-123">**ВИДЕО. Шринктофит**</span><span class="sxs-lookup"><span data-stu-id="5cab8-123">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> </dl>

 

 





