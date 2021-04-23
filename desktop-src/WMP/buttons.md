---
title: Кнопки (Windows Media Player SDK)
description: Кнопки
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Общие сведения об обложках проигрывателя Windows Media для мобильных устройств, кнопка "Обзор"
- обложки, обзор кнопок
- Справочник по обложкам, кнопкам
- кнопки в обложках, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134991"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="4a3e6-107">Кнопки (Windows Media Player SDK)</span><span class="sxs-lookup"><span data-stu-id="4a3e6-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="4a3e6-108">Вам потребуется использовать одну или несколько кнопок в обложке, и каждая кнопка должна быть определена в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="4a3e6-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="4a3e6-109">Если в этом разделе не определена кнопка, Обложка не сможет ее использовать.</span><span class="sxs-lookup"><span data-stu-id="4a3e6-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="4a3e6-110">Раздел Buttons файла определения обложки начинается со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="4a3e6-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="4a3e6-111">Затем необходимо добавить одну или несколько строк, содержащих сведения о каждой из кнопок в обложке.</span><span class="sxs-lookup"><span data-stu-id="4a3e6-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="4a3e6-112">Типичная строка может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="4a3e6-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="4a3e6-113">Обратите внимание, что этот код должен вводиться в виде одной строки, начинающейся с "Плайпаусе", и заканчиваться на "Отправлено @ 160, 98".</span><span class="sxs-lookup"><span data-stu-id="4a3e6-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="4a3e6-114">Для раздела Button в файле определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="4a3e6-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="4a3e6-115">Опять же, обратите внимание, что они должны быть введены в виде отдельных строк, первая начинается с символа "// <Function> " и заканчиваться на " &lt; Push 2 Image src &gt; ".</span><span class="sxs-lookup"><span data-stu-id="4a3e6-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="4a3e6-116">Вторая строка начинается с "//----------" и заканчивается на "------------------."</span><span class="sxs-lookup"><span data-stu-id="4a3e6-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="4a3e6-117">Сведения о кнопке для каждой строки в разделе кнопки должны отображаться в следующем порядке.</span><span class="sxs-lookup"><span data-stu-id="4a3e6-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="4a3e6-118">Требуются только первые шесть частей строки.</span><span class="sxs-lookup"><span data-stu-id="4a3e6-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="4a3e6-119">Дополнительные образы не включаются, если они не нужны.</span><span class="sxs-lookup"><span data-stu-id="4a3e6-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="4a3e6-120">Функция Button</span><span class="sxs-lookup"><span data-stu-id="4a3e6-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="4a3e6-121">Тип кнопки</span><span class="sxs-lookup"><span data-stu-id="4a3e6-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="4a3e6-122">Расположение кнопки</span><span class="sxs-lookup"><span data-stu-id="4a3e6-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="4a3e6-123">Источник отправленного изображения</span><span class="sxs-lookup"><span data-stu-id="4a3e6-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="4a3e6-124">Источник изображения для отключенной кнопки</span><span class="sxs-lookup"><span data-stu-id="4a3e6-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="4a3e6-125">Цвет попадания в RGB</span><span class="sxs-lookup"><span data-stu-id="4a3e6-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="4a3e6-126">Нормальный источник вторичного образа</span><span class="sxs-lookup"><span data-stu-id="4a3e6-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="4a3e6-127">Нормальный источник третьего образа</span><span class="sxs-lookup"><span data-stu-id="4a3e6-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="4a3e6-128">Источник отправленного дополнительного образа</span><span class="sxs-lookup"><span data-stu-id="4a3e6-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="4a3e6-129">Источник отправленного третьего образа</span><span class="sxs-lookup"><span data-stu-id="4a3e6-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="4a3e6-130">Пример кода кнопки см. в разделе « [Пример кнопки»](sample-button-section.md).</span><span class="sxs-lookup"><span data-stu-id="4a3e6-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a3e6-131">См. также</span><span class="sxs-lookup"><span data-stu-id="4a3e6-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a3e6-132">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="4a3e6-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




