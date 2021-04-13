---
title: Источник изображения для отключенной кнопки
description: Источник изображения для отключенной кнопки
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Обложки мобильных устройств проигрывателя Windows Media, источник изображения кнопки
- обложки, источник изображения кнопки
- Справочник по обложкам, кнопкам
- кнопки в обложках, источник изображения
- Источник изображения для обложек, кнопок
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410975"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="58836-108">Источник изображения для отключенной кнопки</span><span class="sxs-lookup"><span data-stu-id="58836-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="58836-109">Необходимо определить источник изображения, которое должно отображаться, когда кнопка отключена или находится в состоянии, соответствующем Off.</span><span class="sxs-lookup"><span data-stu-id="58836-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="58836-110">Образ берется из файла, который вы определили как отключенный в разделе "точечные рисунки".</span><span class="sxs-lookup"><span data-stu-id="58836-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="58836-111">Необходимо ввести тип образа, за которым следует пробел, символ @ и еще один пробел.</span><span class="sxs-lookup"><span data-stu-id="58836-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="58836-112">Затем необходимо ввести два положительных целых числа, которые определяют координаты (в пикселях) изображения, которое будет использоваться в файле точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="58836-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="58836-113">Расположение, в котором будет отображаться изображение, берется из координат, определенных для кнопки относительно фонового изображения, но местоположение, из которого оно берется, определяется двумя числами, приведенными ниже "Disabled @", и определяется по отключенному точечному рисунку, из которого считывается изображение.</span><span class="sxs-lookup"><span data-stu-id="58836-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="58836-114">Например, чтобы использовать изображение из отключенного точечного рисунка, расположенного в отключенном файле, сверху и слева от 50, 60 пикселей, используйте следующий код:</span><span class="sxs-lookup"><span data-stu-id="58836-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="58836-115">Необходимо определить отключенный точечный рисунок.</span><span class="sxs-lookup"><span data-stu-id="58836-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="58836-116">Если вы не хотите отображать другое изображение, можно определить фоновый рисунок в качестве отключенного точечного рисунка со смещением 0, 0:</span><span class="sxs-lookup"><span data-stu-id="58836-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="58836-117">В предыдущем примере 50, 60 — это расположение кнопки, с которой вы работаете, в отключенном файле (в данном случае это то же расположение, что и кнопка на фоновом рисунке).</span><span class="sxs-lookup"><span data-stu-id="58836-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="58836-118">Однако настоятельно рекомендуется отображать отключенный образ для всех кнопок, чтобы дать пользователям визуальную индикацию, так как многие кнопки не будут работать при определенных условиях, таких как пустой список воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="58836-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="58836-119">Если пользователи узнают, что кнопка отключена, они не будут пытаться щелкнуть ее или подумать, что обложка не работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="58836-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58836-120">См. также</span><span class="sxs-lookup"><span data-stu-id="58836-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58836-121">**Кнопки**</span><span class="sxs-lookup"><span data-stu-id="58836-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




