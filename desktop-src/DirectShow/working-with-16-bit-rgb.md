---
description: Работа с 16-разрядным RGB
ms.assetid: 0a245187-4120-4003-9a8f-6b1e8fa40d38
title: Работа с 16-разрядным RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f6bf4b3217af4d0261d4ab26ca011881762a2a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683627"
---
# <a name="working-with-16-bit-rgb"></a><span data-ttu-id="1b230-103">Работа с 16-разрядным RGB</span><span class="sxs-lookup"><span data-stu-id="1b230-103">Working with 16-bit RGB</span></span>

<span data-ttu-id="1b230-104">Для 16-битного RGB определены два формата:</span><span class="sxs-lookup"><span data-stu-id="1b230-104">Two formats are defined for 16-bit uncompressed RGB:</span></span>

-   <span data-ttu-id="1b230-105">МЕДИАСУБТИПЕ \_ 555 использует по пять бит для красного, зеленого и синего компонентов в пикселях.</span><span class="sxs-lookup"><span data-stu-id="1b230-105">MEDIASUBTYPE\_555 uses five bits each for the red, green, and blue components in a pixel.</span></span> <span data-ttu-id="1b230-106">Наиболее важный бит в **слове** игнорируется.</span><span class="sxs-lookup"><span data-stu-id="1b230-106">The most significant bit in the **WORD** is ignored.</span></span>
-   <span data-ttu-id="1b230-107">МЕДИАСУБТИПЕ \_ 565 использует пять бит для красного и синего компонентов и шесть бит для зеленого компонента.</span><span class="sxs-lookup"><span data-stu-id="1b230-107">MEDIASUBTYPE\_565 uses five bits for the red and blue components, and six bits for the green component.</span></span> <span data-ttu-id="1b230-108">Этот формат отражает тот факт, что человеческие концепции наиболее чувствительны к зеленым частям видимого спектра.</span><span class="sxs-lookup"><span data-stu-id="1b230-108">This format reflects the fact that human vision is most sensitive to the green portions of the visible spectrum.</span></span>

<span data-ttu-id="1b230-109">**RGB 565**</span><span class="sxs-lookup"><span data-stu-id="1b230-109">**RGB 565**</span></span>

<span data-ttu-id="1b230-110">Чтобы извлечь цветовые компоненты из изображения RGB 565, рассматривайте каждый пиксель как тип **слова** и используйте следующие битовые маски:</span><span class="sxs-lookup"><span data-stu-id="1b230-110">To extract the color components from an RGB 565 image, treat each pixel as a **WORD** type and use the following bit masks:</span></span>


```C++
WORD red_mask = 0xF800;
WORD green_mask = 0x7E0;
WORD blue_mask = 0x1F;
```



<span data-ttu-id="1b230-111">Получите цветовые компоненты из пикселя следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1b230-111">Get the color components from a pixel as follows:</span></span>


```C++
BYTE red_value = (pixel & red_mask) >> 11;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);
```



<span data-ttu-id="1b230-112">Помните, что красный и синий каналы имеют 5 бит, а зеленый канал — 6 бит.</span><span class="sxs-lookup"><span data-stu-id="1b230-112">Remember that the red and blue channels are 5 bits and the green channel is 6 bits.</span></span> <span data-ttu-id="1b230-113">Чтобы преобразовать эти значения в 8-разрядные компоненты (для 24-разрядного или 32-разрядного RGB), необходимо сдвинуть соответствующее число битов влево:</span><span class="sxs-lookup"><span data-stu-id="1b230-113">To convert these values to 8-bit components (for 24-bit or 32-bit RGB), you must left-shift the appropriate number of bits:</span></span>


```C++
// Expand to 8-bit values.
BYTE red   = red_value << 3;
BYTE green = green_value << 2;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="1b230-114">Отмените этот процесс, чтобы создать RGB 565 пикселей.</span><span class="sxs-lookup"><span data-stu-id="1b230-114">Reverse this process to create an RGB 565 pixel.</span></span> <span data-ttu-id="1b230-115">Предполагая, что значения цвета были усечены до правильного числа битов:</span><span class="sxs-lookup"><span data-stu-id="1b230-115">Assuming the color values have been truncated to the correct number of bits:</span></span>


```C++
WORD pixel565 = (red_value << 11) | (green_value << 5) | blue_value;
```



<span data-ttu-id="1b230-116">**RGB 555**</span><span class="sxs-lookup"><span data-stu-id="1b230-116">**RGB 555**</span></span>

<span data-ttu-id="1b230-117">Работа с RGB 555, по сути, аналогична RGB 565, за исключением того, что битовые маски и операции сдвига в битах различаются.</span><span class="sxs-lookup"><span data-stu-id="1b230-117">Working with RGB 555 is essentially the same as RGB 565, except the bit masks and bit shift operations are different.</span></span> <span data-ttu-id="1b230-118">Чтобы получить цветовые компоненты с пикселя RGB 555, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1b230-118">To get the color components from an RGB 555 pixel, do the following:</span></span>


```C++
WORD red_mask = 0x7C00;
WORD green_mask = 0x3E0;
WORD blue_mask = 0x1F;

BYTE red_value = (pixel & red_mask) >> 10;
BYTE green_value = (pixel & green_mask) >> 5;
BYTE blue_value = (pixel & blue_mask);

// Expand to 8-bit values:
BYTE red   = red_value << 3;
BYTE green = green_value << 3;
BYTE blue  = blue_value << 3;
```



<span data-ttu-id="1b230-119">Чтобы упаковать значения красного, зеленого и синего цветов в RGB 555 пикселей, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="1b230-119">To pack the red, green, and blue color values into an RGB 555 pixel, do the following:</span></span>


```C++
WORD pixel565 = (red << 10) | (green << 5) | blue;
```



## <a name="related-topics"></a><span data-ttu-id="1b230-120">См. также</span><span class="sxs-lookup"><span data-stu-id="1b230-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b230-121">Несжатые подтипы видео RGB</span><span class="sxs-lookup"><span data-stu-id="1b230-121">Uncompressed RGB Video Subtypes</span></span>](uncompressed-rgb-video-subtypes.md)
</dt> </dl>

 

 



