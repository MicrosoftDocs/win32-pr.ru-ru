---
title: Обложка альбома
description: Обложка альбома
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Обложки для мобильных устройств проигрывателя Windows Media, Обложка альбома
- обложки, Обложка альбома
- Справочник по обложкам, обложкам альбомов
- графические файлы для обложек, обложки альбомов
- Обложка альбома в обложек
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691175"
---
# <a name="album-art"></a><span data-ttu-id="f4a26-108">Обложка альбома</span><span class="sxs-lookup"><span data-stu-id="f4a26-108">Album Art</span></span>

<span data-ttu-id="f4a26-109">При создании обложки для проигрывателя Windows Media 10 Mobile или более поздней версии может потребоваться отображение обложки альбома, относящейся к текущему воспроизводимому элементу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f4a26-109">When you create a skin for Windows Media Player 10 Mobile or later, you may want to display album art that relates to the currently playing media item.</span></span> <span data-ttu-id="f4a26-110">При проектировании обложки необходимо зарезервировать место в фоновом изображении, чтобы оно содержало обложку альбома.</span><span class="sxs-lookup"><span data-stu-id="f4a26-110">When you design your skin, you will want to reserve space in the Background image to contain the album art.</span></span>

<span data-ttu-id="f4a26-111">Раздел обложки альбома файла определения обложки должен начинаться со следующей строки:</span><span class="sxs-lookup"><span data-stu-id="f4a26-111">The Album Art section of the skin definition file must begin with the following line:</span></span>


```C++
[ Album Art ]

```



<span data-ttu-id="f4a26-112">Затем необходимо добавить сведения, указывающие расположение и размер обложки альбома в оболочке.</span><span class="sxs-lookup"><span data-stu-id="f4a26-112">You then must add information that specifies the location and size of the album art in your skin.</span></span> <span data-ttu-id="f4a26-113">Необходимо ввести четыре положительных целых числа, разделенные запятыми, которые определяют левую, верхнюю, ширину и высоту обложки альбома (в пикселях) относительно фонового изображения.</span><span class="sxs-lookup"><span data-stu-id="f4a26-113">You must enter four positive integers, separated by commas that define the left, top, width, and height of the album art, in pixels, relative to the background image.</span></span> <span data-ttu-id="f4a26-114">В следующем примере показано, как задать измерения:</span><span class="sxs-lookup"><span data-stu-id="f4a26-114">The following example shows how to specify dimensions:</span></span>


```C++
//  <Location>
//  ----------
   5,37,230,155

```



<span data-ttu-id="f4a26-115">Если вы планируете включить в обложку раздел видео, то для экономии места можно использовать тот же размер и расположение для обложки альбома.</span><span class="sxs-lookup"><span data-stu-id="f4a26-115">If you plan on including a video section in your skin, you can use the same size and location for your album art to conserve space.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4a26-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f4a26-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4a26-117">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="f4a26-117">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




