---
title: КУСТОМСЛИДЕР. Поситионимаже
description: Атрибут Поситионимаже указывает или получает карту изображения, используемую для определения того, какое изображение должно быть отображено из файла изображения.
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- Проигрыватель Windows Media КУСТОМСЛИДЕР. Поситионимаже
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694405"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="be8c4-104">КУСТОМСЛИДЕР. Поситионимаже</span><span class="sxs-lookup"><span data-stu-id="be8c4-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="be8c4-105">Атрибут **поситионимаже** указывает или получает карту изображения, используемую для определения того, какое изображение должно быть отображено из файла изображения.</span><span class="sxs-lookup"><span data-stu-id="be8c4-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="be8c4-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="be8c4-106">Possible Values</span></span>

<span data-ttu-id="be8c4-107">Этот атрибут является **строкой** для чтения и записи, содержащей имя файла изображения.</span><span class="sxs-lookup"><span data-stu-id="be8c4-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="be8c4-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be8c4-108">Remarks</span></span>

<span data-ttu-id="be8c4-109">Этот атрибут является обязательным и должен быть указан.</span><span class="sxs-lookup"><span data-stu-id="be8c4-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="be8c4-110">**Поситионимаже** не отображается.</span><span class="sxs-lookup"><span data-stu-id="be8c4-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="be8c4-111">Вместо этого он выступает в качестве схемы, определяющей щелчки отображаемых областей изображения.</span><span class="sxs-lookup"><span data-stu-id="be8c4-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="be8c4-112">Отображаемое изображение является одним из подизображений файла изображения и представляет фактическое состояние ползунка.</span><span class="sxs-lookup"><span data-stu-id="be8c4-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="be8c4-113">**Поситионимаже** содержит несколько серых регионов масштабирования, равных количеству этих подобразов.</span><span class="sxs-lookup"><span data-stu-id="be8c4-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="be8c4-114">Подизображения должны иметь те же размеры, что и **поситионимаже** , или пользовательский ползунок будет работать неправильно.</span><span class="sxs-lookup"><span data-stu-id="be8c4-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="be8c4-115">Любой регион, не являющийся серой шкалой, не будет щелкать.</span><span class="sxs-lookup"><span data-stu-id="be8c4-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="be8c4-116">Для областей, используемых для щелчков, должно быть задано цветовое значение, которое равномерно распределяется между черным спектром в оттенках серого, а первый регион — чистым черным, а последний регион — чистым белым.</span><span class="sxs-lookup"><span data-stu-id="be8c4-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="be8c4-117">Значения цвета каждой последующей области должны увеличиваться на величину, равную 255, деленную на общее число регионов минус единица, округление до ближайшего целого числа.</span><span class="sxs-lookup"><span data-stu-id="be8c4-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="be8c4-118">Например, если имеется шесть регионов, то приращение будет 51 (255, деленное на 5), а шесть значений оттенков серого — 0, 51, 102, 153, 204 и 255.</span><span class="sxs-lookup"><span data-stu-id="be8c4-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="be8c4-119">Затем шестнадцатеричные значения цвета для шести регионов будут \# 000000, \# 333333, \# 666666, \# 999999, \# кккккк и \# FFFFFF.</span><span class="sxs-lookup"><span data-stu-id="be8c4-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="be8c4-120">Таким образом, регионы будут иметь последовательность, определяемую значениями цвета серого масштаба, и эта последовательность будет соответствовать последовательности подизображений в файле изображения.</span><span class="sxs-lookup"><span data-stu-id="be8c4-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="be8c4-121">При щелчке по одному из регионов отображается соответствующее подизображение, а **значение** настраиваемого ползунка соответствующим образом обновляется.</span><span class="sxs-lookup"><span data-stu-id="be8c4-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="be8c4-122">Поддерживаются следующие типы файлов изображений: BMP, JPG, PNG и GIF (не включая анимированные GIF).</span><span class="sxs-lookup"><span data-stu-id="be8c4-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="be8c4-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="be8c4-123">Examples</span></span>

<span data-ttu-id="be8c4-124">Ниже приведен пример настраиваемого ползунка **поситионимаже**.</span><span class="sxs-lookup"><span data-stu-id="be8c4-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="be8c4-125">Соответствующее изображение показано в разделе "пример" свойства **Image** .</span><span class="sxs-lookup"><span data-stu-id="be8c4-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![Образец графика поситионимаже](images/dialmap.png)

<span data-ttu-id="be8c4-127">В следующем коде показано использование атрибутов **кустомслидер** .</span><span class="sxs-lookup"><span data-stu-id="be8c4-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="be8c4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="be8c4-128">Requirements</span></span>



| <span data-ttu-id="be8c4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="be8c4-129">Requirement</span></span> | <span data-ttu-id="be8c4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="be8c4-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="be8c4-131">Версия</span><span class="sxs-lookup"><span data-stu-id="be8c4-131">Version</span></span><br/> | <span data-ttu-id="be8c4-132">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="be8c4-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be8c4-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be8c4-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be8c4-134">**КУСТОМСЛИДЕР, элемент**</span><span class="sxs-lookup"><span data-stu-id="be8c4-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="be8c4-135">**КУСТОМСЛИДЕР. Image**</span><span class="sxs-lookup"><span data-stu-id="be8c4-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





