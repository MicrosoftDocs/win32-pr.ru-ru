---
title: Описание (пакет SDK для проигрывателя Windows Media)
description: Описание
ms.assetid: 940ef0bf-d651-411a-b36d-99dcc01d8508
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, раздел описания
- обложки, раздел описания
- Справочник по обложкам, разделу описания
- Раздел описания в обложках
- файлы определения обложки, раздел описания
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4a1b714fb917f9d13ee710509cfc5bf696e3eef
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104414553"
---
# <a name="description-windows-media-player-sdk"></a><span data-ttu-id="8f59f-108">Описание (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="8f59f-108">Description (Windows Media Player SDK)</span></span>

<span data-ttu-id="8f59f-109">При создании обложки для проигрывателя Windows Media 9 Series для Windows Mobile 2003 или более поздней версии необходимо включить раздел Description.</span><span class="sxs-lookup"><span data-stu-id="8f59f-109">When you create a skin for Windows Media Player 9 Series for Windows Mobile 2003 or later, you must include a Description section.</span></span> <span data-ttu-id="8f59f-110">Раздел Description (описание) позволяет задать ширину и высоту дисплея, разрешение экрана и ориентацию экрана, для которой была разработана обложка.</span><span class="sxs-lookup"><span data-stu-id="8f59f-110">The Description section enables you to specify the width and height of the display, the display resolution, and the display orientation for which the skin was designed.</span></span> <span data-ttu-id="8f59f-111">Раздел Description должен появиться в файле определения обложки перед любым другим разделом и сразу после объявления начальной версии.</span><span class="sxs-lookup"><span data-stu-id="8f59f-111">The Description section must appear in the skin definition file before any other section, and just after the initial version declaration.</span></span>

<span data-ttu-id="8f59f-112">Раздел Description файла определения обложки должен начинаться со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="8f59f-112">The Description section of the skin definition file must begin with the following line:</span></span>


```C++
[ Description ]

```



<span data-ttu-id="8f59f-113">Затем необходимо добавить сведения об измерениях обложки и разрешении экрана.</span><span class="sxs-lookup"><span data-stu-id="8f59f-113">You then must add information about the dimensions of the skin and the display resolution.</span></span> <span data-ttu-id="8f59f-114">В следующем примере показано, как задать измерения:</span><span class="sxs-lookup"><span data-stu-id="8f59f-114">The following example shows how to specify dimensions:</span></span>


```C++
//              <X,Y>       <DPI>

//              -------     -----

    Dimensions  240,320      96

```



<span data-ttu-id="8f59f-115">Это означает, что вы разработали обложку для отображения в 240 пикселей в ширину, 320 пикселей в высоком уровне и при использовании разрешения дисплея 96 DPI.</span><span class="sxs-lookup"><span data-stu-id="8f59f-115">This specifies that you designed the skin to be displayed 240 pixels wide, 320 pixels high, and using 96 DPI display resolution.</span></span> <span data-ttu-id="8f59f-116">Обратите внимание, что это подразумевает ориентацию в портретном режиме.</span><span class="sxs-lookup"><span data-stu-id="8f59f-116">Note that this implies a portrait mode orientation.</span></span>

<span data-ttu-id="8f59f-117">В разделе Описание можно дополнительно указать режим ориентации, для которого была разработана обложка.</span><span class="sxs-lookup"><span data-stu-id="8f59f-117">You may optionally specify the orientation mode for which you designed the skin in the description section.</span></span> <span data-ttu-id="8f59f-118">В следующем примере показано, как задать ориентацию:</span><span class="sxs-lookup"><span data-stu-id="8f59f-118">The following example shows how to specify orientation:</span></span>


```C++
//     <Orientation>

//     -------------

    Orientation Portrait

```



<span data-ttu-id="8f59f-119">В следующей таблице перечислены значения, которые можно использовать для ориентации.</span><span class="sxs-lookup"><span data-stu-id="8f59f-119">The following table lists the values you may use for Orientation.</span></span>



| <span data-ttu-id="8f59f-120">Ориентация</span><span class="sxs-lookup"><span data-stu-id="8f59f-120">Orientation</span></span> | <span data-ttu-id="8f59f-121">Описание</span><span class="sxs-lookup"><span data-stu-id="8f59f-121">Description</span></span>                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f59f-122">Альбомная</span><span class="sxs-lookup"><span data-stu-id="8f59f-122">Landscape</span></span>   | <span data-ttu-id="8f59f-123">Ширина обложки больше, чем высота обложки.</span><span class="sxs-lookup"><span data-stu-id="8f59f-123">The width of the skin is greater than height of the skin.</span></span> <span data-ttu-id="8f59f-124">Дисплей ориентирован горизонтально.</span><span class="sxs-lookup"><span data-stu-id="8f59f-124">The display is oriented in a horizontal fashion.</span></span>   |
| <span data-ttu-id="8f59f-125">Книжная</span><span class="sxs-lookup"><span data-stu-id="8f59f-125">Portrait</span></span>    | <span data-ttu-id="8f59f-126">Высота обложки больше ширины обложки.</span><span class="sxs-lookup"><span data-stu-id="8f59f-126">The height of the skin is greater than the width of the skin.</span></span> <span data-ttu-id="8f59f-127">Отображение ориентировано по вертикали.</span><span class="sxs-lookup"><span data-stu-id="8f59f-127">The display is oriented in a vertical fashion.</span></span> |
| <span data-ttu-id="8f59f-128">Square</span><span class="sxs-lookup"><span data-stu-id="8f59f-128">Square</span></span>      | <span data-ttu-id="8f59f-129">Высота обложки равна ширине обложки.</span><span class="sxs-lookup"><span data-stu-id="8f59f-129">The height of the skin is equal to the width of the skin.</span></span> <span data-ttu-id="8f59f-130">У дисплея нет ориентации.</span><span class="sxs-lookup"><span data-stu-id="8f59f-130">The display has no orientation.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="8f59f-131">Проигрыватель Windows Media 9 Series для Windows Mobile 2003 будет отображать определенную обложку только в том случае, если раздел Description, указанный в файле определения обложки, соответствует текущему состоянию устройства.</span><span class="sxs-lookup"><span data-stu-id="8f59f-131">Windows Media Player 9 Series for Windows Mobile 2003 will only display a particular skin when the description section specified in the skin definition file matches the current state of the device.</span></span>

 

<span data-ttu-id="8f59f-132">Необходимо всегда указывать правильные размеры, разрешение и ориентацию, для которых была создана обложка.</span><span class="sxs-lookup"><span data-stu-id="8f59f-132">You should be careful to always specify the correct dimensions, resolution, and orientation for which your skin was authored.</span></span> <span data-ttu-id="8f59f-133">Например, если измерения, указанные в обложке, описывают альбомную ориентацию, то обложка не будет доступна, если устройство находится в книжной ориентации, даже если в линии ориентации указана книжная ориентация.</span><span class="sxs-lookup"><span data-stu-id="8f59f-133">For example, if the dimensions specified by your skin describe a landscape orientation, your skin will not be available when the device is in portrait mode, even if you specify Portrait in the orientation line.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f59f-134">См. также</span><span class="sxs-lookup"><span data-stu-id="8f59f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f59f-135">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="8f59f-135">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




