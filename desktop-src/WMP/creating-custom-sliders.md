---
title: Создание настраиваемых ползунков
description: Создание настраиваемых ползунков
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- Создание обложек, ползунков
- Обложки проигрывателя Windows Media, ползунки
- обложки, ползунки
- Ползунки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532297"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="044ad-107">Создание настраиваемых ползунков</span><span class="sxs-lookup"><span data-stu-id="044ad-107">Creating Custom Sliders</span></span>

<span data-ttu-id="044ad-108">Вы можете создавать настраиваемые ползунки в любой форме.</span><span class="sxs-lookup"><span data-stu-id="044ad-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="044ad-109">В этом примере выбирается простая полоса, но фактическая фигура может быть любой.</span><span class="sxs-lookup"><span data-stu-id="044ad-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="044ad-110">Ниже приведен код для элемента **кустомслидер** :</span><span class="sxs-lookup"><span data-stu-id="044ad-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="044ad-111">Настраивает начальное значение для ползунка.</span><span class="sxs-lookup"><span data-stu-id="044ad-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="044ad-112">Появились два новых точечных рисунка.</span><span class="sxs-lookup"><span data-stu-id="044ad-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="044ad-113">Один из них — точечный рисунок в градациях серого (slider.bmp), который определяет, какие значения будут использоваться при щелчке, а другая (slider.bmp), определяющая изображение, которое будет отображаться при нажатии на определенную часть оттенков серого.</span><span class="sxs-lookup"><span data-stu-id="044ad-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="044ad-114">Начальное значение определяется путем прослушивания тома с помощью вмппроп, а затем том может быть изменен, когда пользователь щелкает часть ползунка, которая активирует изменение значения.</span><span class="sxs-lookup"><span data-stu-id="044ad-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="044ad-115">Аналогичную обложку рабочего ползунка можно увидеть в разделе примеров пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="044ad-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="044ad-116">См. также</span><span class="sxs-lookup"><span data-stu-id="044ad-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="044ad-117">**Руководством по созданию обложки**</span><span class="sxs-lookup"><span data-stu-id="044ad-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




