---
description: В Direct3D все двухмерные (двумерные) изображения представлены линейным диапазоном памяти, называемым поверхностью.
ms.assetid: 33430f01-cd26-45f4-9ce8-ca2c17c7ae6b
title: Форматы поверхностей (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78aad64940510a080ba05d0513e7f66d33912a41
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104140194"
---
# <a name="surface-formats-direct3d-9"></a><span data-ttu-id="1048c-103">Форматы поверхностей (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="1048c-103">Surface Formats (Direct3D 9)</span></span>

<span data-ttu-id="1048c-104">В Direct3D все двухмерные (двумерные) изображения представлены линейным диапазоном памяти, называемым поверхностью.</span><span class="sxs-lookup"><span data-stu-id="1048c-104">In Direct3D, all two-dimensional (2D) images are represented by a linear range of memory called a surface.</span></span> <span data-ttu-id="1048c-105">Поверхность может рассматриваться как двумерный массив, где каждый элемент содержит значение цвета, представляющее небольшой участок изображения, называемый пиксель.</span><span class="sxs-lookup"><span data-stu-id="1048c-105">A surface can be thought of as a 2D array where each element holds a color value representing a small section of the image, called a pixel.</span></span> <span data-ttu-id="1048c-106">Уровень детализации изображения определяется как число пикселей, необходимых для представления изображения, и число бит, необходимых для цветового спектра изображения.</span><span class="sxs-lookup"><span data-stu-id="1048c-106">An image's detail level is defined by both the number of pixels needed to represent the image, and the number of bits needed for the image's color spectrum.</span></span> <span data-ttu-id="1048c-107">Например, изображение размером 800 пикселей в ширину на 600 пикселей высокого уровня с 32 битами цвета для каждого пикселя (написанное как 800x600x32) будет более детализировано, чем изображение размером в 640 пикселов в ширину, то есть в 480 пикселей высотой и 16 битами цвета для каждого пикселя (написано как 640x480x16).</span><span class="sxs-lookup"><span data-stu-id="1048c-107">For example, an image that is 800 pixels wide by 600 pixels high with 32 bits of color for each pixel (written as 800x600x32) will be more detailed than an image that is 640 pixels wide by 480 pixels tall with 16 bits of color for each pixel (written as 640x480x16).</span></span> <span data-ttu-id="1048c-108">Аналогично, более подробное изображение потребует более крупной поверхности для хранения данных.</span><span class="sxs-lookup"><span data-stu-id="1048c-108">Likewise, the more detailed image will require a larger surface to store the data.</span></span> <span data-ttu-id="1048c-109">Для изображения 800x600x32 размеры массива поверхности будут равно 800x600, а каждый элемент будет содержать 32-разрядное значение, представляющее его цвет.</span><span class="sxs-lookup"><span data-stu-id="1048c-109">For an 800x600x32 image, the surface's array dimensions will be 800x600, and each element will hold a 32-bit value to represent its color.</span></span>

<span data-ttu-id="1048c-110">Все поверхности имеют размер и сохраняют определенное количество битов, представляющих цвет.</span><span class="sxs-lookup"><span data-stu-id="1048c-110">All surfaces have a size and store a specific number of bits that represent color.</span></span> <span data-ttu-id="1048c-111">Биты, представляющие цвет, разделяются на отдельные элементы цвета: красный, зеленый и синий.</span><span class="sxs-lookup"><span data-stu-id="1048c-111">The bits that represent color are separated into individual color elements: red, green, and blue.</span></span> <span data-ttu-id="1048c-112">В Direct3D все элементы цвета определяются перечисляемым типом [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="1048c-112">In Direct3D all color elements are defined by the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="1048c-113">Формат цвета Direct3D разбивается на число байтов, зарезервированных для каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="1048c-113">A Direct3D color format is broken down into the number of byes reserved for each color.</span></span> <span data-ttu-id="1048c-114">Например, 16-разрядный формат цвета в Direct3D определяется как D3DFMT \_ R5G6B5, где 5 бит зарезервированы для Red (R), 6 бит для зеленого (G) и 5 бит для синего (B).</span><span class="sxs-lookup"><span data-stu-id="1048c-114">For example, a 16-bit color format in Direct3D is defined as D3DFMT\_R5G6B5, where 5 bits are reserved for red (R), 6 bits for green (G), and 5 bits for blue (B).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1048c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="1048c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1048c-116">Поверхности Direct3D</span><span class="sxs-lookup"><span data-stu-id="1048c-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> </dl>

 

 



