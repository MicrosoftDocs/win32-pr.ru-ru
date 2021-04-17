---
title: Видео (пакет SDK для проигрывателя Windows Media)
description: Видео
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Обложки Windows Media Player для мобильных устройств, видео
- обложки, видео
- Справочник по обложкам, видео
- видео в обложках, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105701001"
---
# <a name="video-windows-media-player-sdk"></a><span data-ttu-id="fe830-107">Видео (пакет SDK для проигрывателя Windows Media)</span><span class="sxs-lookup"><span data-stu-id="fe830-107">Video (Windows Media Player SDK)</span></span>

<span data-ttu-id="fe830-108">Видеоизображение позволяет пользователю просматривать цифровые видеофайлы.</span><span class="sxs-lookup"><span data-stu-id="fe830-108">A video display allows the user to view digital video files.</span></span> <span data-ttu-id="fe830-109">Область отображения видео отображается только при воспроизведении или приостановке видео.</span><span class="sxs-lookup"><span data-stu-id="fe830-109">The video display area is only visible when video is playing or paused.</span></span> <span data-ttu-id="fe830-110">При проектировании обложки необходимо зарезервировать пространство в фоновом изображении, чтобы оно содержало экран видео.</span><span class="sxs-lookup"><span data-stu-id="fe830-110">When you design your skin, you will want to reserve space in the Background image to contain the video display.</span></span> <span data-ttu-id="fe830-111">В противном случае экран видео может переложить себя на любую видимую картинку, например на фоновый файл, кнопки и ползунки, что позволит пользователю использовать элементы управления на обложке.</span><span class="sxs-lookup"><span data-stu-id="fe830-111">If you don't, the video display may superimpose itself over any visible art, such as the Background file, buttons, and trackbars, which will keep the user from operating the controls on your skin.</span></span>

<span data-ttu-id="fe830-112">Раздел видео файла определения обложки должен начинаться с следующей строки:</span><span class="sxs-lookup"><span data-stu-id="fe830-112">The Video section of the skin definition file must begin with this line:</span></span>


```C++
[ Video ]

```



<span data-ttu-id="fe830-113">Затем необходимо добавить строку, указывающую расположение и размер отображаемой видеообласти в обложке.</span><span class="sxs-lookup"><span data-stu-id="fe830-113">You then must add a line that specifies the location and size of the video display area in your skin.</span></span>


```C++
0,38,240,172

```



<span data-ttu-id="fe830-114">Для раздела видео в файле определения обложки можно использовать следующий шаблон:</span><span class="sxs-lookup"><span data-stu-id="fe830-114">You can use the following template for the Video section of your skin definition file:</span></span>


```C++
//  <Location>
//  ----------

```



<span data-ttu-id="fe830-115">Дополнительные сведения приведены в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="fe830-115">The following sections provide further details.</span></span>

-   [<span data-ttu-id="fe830-116">Расположение видео</span><span class="sxs-lookup"><span data-stu-id="fe830-116">Video Location</span></span>](video-location.md)
-   [<span data-ttu-id="fe830-117">Источник изображения видео</span><span class="sxs-lookup"><span data-stu-id="fe830-117">Video Image Source</span></span>](video-image-source.md)
-   [<span data-ttu-id="fe830-118">Размер видео</span><span class="sxs-lookup"><span data-stu-id="fe830-118">Video Size</span></span>](video-size.md)
-   [<span data-ttu-id="fe830-119">Раздел с примерами видео</span><span class="sxs-lookup"><span data-stu-id="fe830-119">Sample Video Section</span></span>](sample-video-section.md)

## <a name="related-topics"></a><span data-ttu-id="fe830-120">См. также</span><span class="sxs-lookup"><span data-stu-id="fe830-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fe830-121">**Справочник по обложкам**</span><span class="sxs-lookup"><span data-stu-id="fe830-121">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




