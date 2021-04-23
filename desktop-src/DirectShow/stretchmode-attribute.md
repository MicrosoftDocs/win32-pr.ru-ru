---
description: Атрибут стретчмоде указывает, как растянуть изображение, которое не соответствует выходным измерениям.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Атрибут стретчмоде
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911703"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="adc2a-103">Атрибут стретчмоде</span><span class="sxs-lookup"><span data-stu-id="adc2a-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="adc2a-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="adc2a-104">\[Deprecated.</span></span> <span data-ttu-id="adc2a-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="adc2a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="adc2a-106">`stretchmode`Атрибут указывает, как растянуть изображение, которое не соответствует выходным измерениям.</span><span class="sxs-lookup"><span data-stu-id="adc2a-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="adc2a-107">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="adc2a-107">Possible Values</span></span>

<span data-ttu-id="adc2a-108">Должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="adc2a-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="adc2a-109">"Stretch": изображение растягивается в соответствии с размером выходного кадра без сохранения пропорций.</span><span class="sxs-lookup"><span data-stu-id="adc2a-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="adc2a-110">(по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="adc2a-110">(Default)</span></span>
-   <span data-ttu-id="adc2a-111">"обрезать": изображение обрезается в соответствии с размером выходного кадра.</span><span class="sxs-lookup"><span data-stu-id="adc2a-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="adc2a-112">"пресервеаспектратио": исходные пропорции сохраняются, а черная леттербокс — в более коротком измерении.</span><span class="sxs-lookup"><span data-stu-id="adc2a-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="adc2a-113">"пресервеаспектратионолеттербокс": Размер изображения изменяется для заполнения всего целевого кадра с сохранением пропорций.</span><span class="sxs-lookup"><span data-stu-id="adc2a-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="adc2a-114">Применение</span><span class="sxs-lookup"><span data-stu-id="adc2a-114">Applies To</span></span>

[<span data-ttu-id="adc2a-115">**clip**</span><span class="sxs-lookup"><span data-stu-id="adc2a-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="adc2a-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adc2a-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adc2a-117">Атрибуты КСТЛ</span><span class="sxs-lookup"><span data-stu-id="adc2a-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="adc2a-118">**Иамтимелинесрк:: Сетстретчмоде**</span><span class="sxs-lookup"><span data-stu-id="adc2a-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



