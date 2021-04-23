---
title: Добавление ползунка
description: Добавление ползунка
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- Создание обложек, ползунков
- Обложки проигрывателя Windows Media, ползунки
- обложки, ползунки
- Ползунки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068228"
---
# <a name="adding-a-slider"></a><span data-ttu-id="e8720-107">Добавление ползунка</span><span class="sxs-lookup"><span data-stu-id="e8720-107">Adding a Slider</span></span>

<span data-ttu-id="e8720-108">Можно добавить ползунок для отображения текущего положения носителя, а также разрешить пользователю изменять положение в текущем файле мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e8720-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="e8720-109">Сначала необходимо добавить элемент **Slider** :</span><span class="sxs-lookup"><span data-stu-id="e8720-109">First you must add the **SLIDER** element:</span></span>


```C++
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
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="e8720-110">Это задает максимальное значение в зависимости от продолжительности текущего файла мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="e8720-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="e8720-111">При этом используется миниатюрное растровое изображение с незначительным размером в 10 пикселей на 10 пикселов зеленого квадрата.</span><span class="sxs-lookup"><span data-stu-id="e8720-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="e8720-112">Фон ползунка будет красным, а передний цвет будет синим.</span><span class="sxs-lookup"><span data-stu-id="e8720-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="e8720-113">Когда пользователь перетаскивает изображение бегунка в новую точку и позволяет нажать кнопку мыши, носитель изменится на эту точку.</span><span class="sxs-lookup"><span data-stu-id="e8720-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="e8720-114">Но ползунок не будет перемещаться сам по себе, если только не измеряется текущая позиция с помощью атрибута **CurrentPosition \_ onChange** элемента **Controls** , который внедряется в элемент **Player** .</span><span class="sxs-lookup"><span data-stu-id="e8720-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="e8720-115">При изменении положения носителя вызывается событие, которое затем запускает строку кода, которая изменяет значение ползунка на текущее положение носителя.</span><span class="sxs-lookup"><span data-stu-id="e8720-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="e8720-116">Аналогичную обложку рабочего ползунка можно увидеть в разделе примеров пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="e8720-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8720-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e8720-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8720-118">**Руководством по созданию обложки**</span><span class="sxs-lookup"><span data-stu-id="e8720-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




