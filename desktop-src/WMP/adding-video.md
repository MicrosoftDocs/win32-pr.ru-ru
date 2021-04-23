---
title: Добавление видео
description: Добавление видео
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- Создание обложек, видео
- Обложки проигрывателя Windows Media, видео
- обложки, видео
- видео в обложках, добавление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc952f2fa80536bc6b2bb9ef3b43c6730616af3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691218"
---
# <a name="adding-video"></a><span data-ttu-id="4a117-107">Добавление видео</span><span class="sxs-lookup"><span data-stu-id="4a117-107">Adding Video</span></span>

<span data-ttu-id="4a117-108">Вы можете добавить видео в файл, просто используя элемент **Video** и определив место, где должно размещаться видеоокно.</span><span class="sxs-lookup"><span data-stu-id="4a117-108">You can add a video to your file by simply using the **VIDEO** element and defining where you want the video window to be placed.</span></span>

<span data-ttu-id="4a117-109">Используйте тот же код, что и в разделе Выбор файлов. все, что нужно сделать, — это добавить элемент **Video** с атрибутами верхнего, левого, ширины и высоты.</span><span class="sxs-lookup"><span data-stu-id="4a117-109">Use the same code as you did in the Choosing Files section; all you need to do is add the **VIDEO** element with the top, left, width, and height attributes.</span></span>


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



<span data-ttu-id="4a117-110">Затем при воспроизведении видео оно отобразится в окне.</span><span class="sxs-lookup"><span data-stu-id="4a117-110">Then when you play a video, it will be displayed in the window.</span></span> <span data-ttu-id="4a117-111">Иллюстрация для примера видео была изменена, чтобы сделать обложку немного крупнее.</span><span class="sxs-lookup"><span data-stu-id="4a117-111">The art for the video sample was modified to make a slightly larger skin.</span></span> <span data-ttu-id="4a117-112">Поскольку слои использовались в Photoshop, кнопки были легко перемещены, а новый набор был очень быстро создан.</span><span class="sxs-lookup"><span data-stu-id="4a117-112">Because layers were used in Photoshop, the buttons were easily moved around and a new set was created very quickly.</span></span> <span data-ttu-id="4a117-113">Было изменено только фоновое изображение.</span><span class="sxs-lookup"><span data-stu-id="4a117-113">Only the background image was changed.</span></span> <span data-ttu-id="4a117-114">Заливка использовалась в пустом слое, и был добавлен эффект рельефа и выпуклости.</span><span class="sxs-lookup"><span data-stu-id="4a117-114">A fill was used in a blank layer and a bevel and emboss effect was added.</span></span>

<span data-ttu-id="4a117-115">Аналогичные рабочие обложки можно увидеть в разделе с примерами пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="4a117-115">You can see a similar working video skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a117-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4a117-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a117-117">**Руководством по созданию обложки**</span><span class="sxs-lookup"><span data-stu-id="4a117-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




