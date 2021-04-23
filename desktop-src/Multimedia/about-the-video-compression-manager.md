---
title: О диспетчере сжатия видео
description: О диспетчере сжатия видео
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Мультимедиа Windows, диспетчер сжатия видео (ВКМ)
- мультимедиа, диспетчер сжатия видео (ВКМ)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487636"
---
# <a name="about-the-video-compression-manager"></a><span data-ttu-id="68ef7-105">О диспетчере сжатия видео</span><span class="sxs-lookup"><span data-stu-id="68ef7-105">About the Video Compression Manager</span></span>

<span data-ttu-id="68ef7-106">Как правило, устанавливаемые программы сжатия работают с изображениями видео, хранящимися в файлах AVI.</span><span class="sxs-lookup"><span data-stu-id="68ef7-106">Typically, installable compressors operate with video-image data stored in audio-video interleaved (AVI) files.</span></span> <span data-ttu-id="68ef7-107">В этом обзоре объясняются методики программирования, используемые для доступа к устанавливаемым программам сжатия с помощью ВКМ, и рассматриваются следующие темы:</span><span class="sxs-lookup"><span data-stu-id="68ef7-107">This overview explains the programming techniques used to access installable compressors through VCM and covers the following topics:</span></span>

-   <span data-ttu-id="68ef7-108">Архитектура ВКМ и видео для архитектуры Windows</span><span class="sxs-lookup"><span data-stu-id="68ef7-108">VCM and the Video for Windows architecture</span></span>
-   <span data-ttu-id="68ef7-109">Сжатие и распаковка данных изображения из приложения</span><span class="sxs-lookup"><span data-stu-id="68ef7-109">Compressing and decompressing image data from your application</span></span>
-   <span data-ttu-id="68ef7-110">Рисование данных из приложения с помощью модулей подготовки отчетов ВКМ</span><span class="sxs-lookup"><span data-stu-id="68ef7-110">Using VCM renderers to draw data from your application</span></span>
-   <span data-ttu-id="68ef7-111">Функции и структуры ВКМ</span><span class="sxs-lookup"><span data-stu-id="68ef7-111">VCM functions and structures</span></span>

<span data-ttu-id="68ef7-112">Перед прочтением этого обзора необходимо ознакомиться с графическими службами Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="68ef7-112">Before you read this overview, you should be familiar with the Microsoft Win32 graphic services.</span></span> <span data-ttu-id="68ef7-113">В частности, точечные рисунки и структуры, связанные с точечными рисунками, такие как [**битмапинфо**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) и [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), широко используются ВКМ.</span><span class="sxs-lookup"><span data-stu-id="68ef7-113">In particular, bitmaps and bitmap-related structures, such as [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) and [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), are used extensively by VCM.</span></span> <span data-ttu-id="68ef7-114">Дополнительные сведения о структурах **битмапинфо** и **битмапинфохеадер** см. в разделе [растровые изображения](/previous-versions//ms532349(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="68ef7-114">For additional information about the **BITMAPINFO** and **BITMAPINFOHEADER** structures, see [Bitmaps](/previous-versions//ms532349(v=vs.85)).</span></span>

> [!Note]  
> <span data-ttu-id="68ef7-115">Диспетчер аудиосжатия (ACM) обеспечивает поддержку на уровне системы для драйверов сжатия аудио и распаковки.</span><span class="sxs-lookup"><span data-stu-id="68ef7-115">The audio compression manager (ACM) provides system-level support for audio compression and decompression drivers.</span></span> <span data-ttu-id="68ef7-116">Описание служб сжатия звука см. в разделе [Диспетчер](audio-compression-manager.md)аудиосжатия.</span><span class="sxs-lookup"><span data-stu-id="68ef7-116">For a description of the audio compression services, see [Audio Compression Manager](audio-compression-manager.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="68ef7-117">См. также</span><span class="sxs-lookup"><span data-stu-id="68ef7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ef7-118">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="68ef7-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 