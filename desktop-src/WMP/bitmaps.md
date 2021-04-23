---
title: Точечные рисунки (пакет SDK для проигрывателя Windows Media)
description: Растровые изображения
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Обложки Windows Media Player для мобильных устройств, точечные рисунки
- обложки, точечные рисунки
- Справочник по обложкам, точечным рисункам
- точечные рисунки в обложках, о
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488655"
---
# <a name="bitmaps-windows-media-player-sdk"></a><span data-ttu-id="47cf2-107">Точечные рисунки (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="47cf2-107">Bitmaps (Windows Media Player SDK)</span></span>

<span data-ttu-id="47cf2-108">Необходимо использовать одно или несколько изображений в обложке, и каждое изображение должно быть определено в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="47cf2-108">You must use one or more images in your skin, and each image must be defined in the skin definition file.</span></span> <span data-ttu-id="47cf2-109">Если вы не определили образ в этом разделе, Обложка не сможет его использовать.</span><span class="sxs-lookup"><span data-stu-id="47cf2-109">If you do not define an image in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="47cf2-110">Термин "точечный рисунок" используется в ссылке в универсальном смысле и относится к точечным изображениям с расширением. bmp, изображениям GIF с расширением. gif, изображениям JPEG с расширением. jpg и изображениям PNG с расширением PNG.</span><span class="sxs-lookup"><span data-stu-id="47cf2-110">The term "bitmap" is used throughout the reference in a generic sense, and refers to bitmap images with a .bmp extension, GIF images with a .gif extension, JPEG images with a .jpg extension, and PNG images with a .png extension.</span></span>

<span data-ttu-id="47cf2-111">Раздел точечные рисунки файла определения обложки начинается со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="47cf2-111">The Bitmaps section of the skin definition file begins with this line:</span></span>


```C++
[ Bitmaps ]

```



<span data-ttu-id="47cf2-112">Затем необходимо добавить одну или несколько строк, содержащих сведения о каждом из изображений в обложке.</span><span class="sxs-lookup"><span data-stu-id="47cf2-112">You then must add one or more lines that contain information about each of the images in your skin.</span></span>

<span data-ttu-id="47cf2-113">Типичная строка может выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="47cf2-113">A typical line might be:</span></span>


```C++
    Background  Background.bmp  0,0

```



<span data-ttu-id="47cf2-114">Для раздела точечных рисунков в файле определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="47cf2-114">You can use the following template for the Bitmaps section of your skin definition file:</span></span>


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



<span data-ttu-id="47cf2-115">Для получения сведений о точечных рисунках для каждой строки в разделе "точечный рисунок" необходимо использовать следующий порядок.</span><span class="sxs-lookup"><span data-stu-id="47cf2-115">You must use the following order for bitmap information for each line in the Bitmap section.</span></span> <span data-ttu-id="47cf2-116">Каждая часть строки является обязательной.</span><span class="sxs-lookup"><span data-stu-id="47cf2-116">Each part of the line is required.</span></span>

1.  [<span data-ttu-id="47cf2-117">Тип точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="47cf2-117">Bitmap Type</span></span>](bitmap-type.md)
2.  [<span data-ttu-id="47cf2-118">Имя файла</span><span class="sxs-lookup"><span data-stu-id="47cf2-118">File Name</span></span>](file-name.md)
3.  [<span data-ttu-id="47cf2-119">Положения</span><span class="sxs-lookup"><span data-stu-id="47cf2-119">Coordinates</span></span>](coordinates.md)

<span data-ttu-id="47cf2-120">Пример кода точечного рисунка см. в [разделе пример точечного рисунка](sample-bitmap-section.md).</span><span class="sxs-lookup"><span data-stu-id="47cf2-120">For an example of bitmap code, see [Sample Bitmap Section](sample-bitmap-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="47cf2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="47cf2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47cf2-122">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="47cf2-122">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




