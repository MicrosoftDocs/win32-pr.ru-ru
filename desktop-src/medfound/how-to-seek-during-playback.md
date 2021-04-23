---
description: В этом разделе описывается поиск во время воспроизведения с помощью Мфплай.
ms.assetid: 8ccca882-5543-4913-8eb9-8adaed2c57aa
title: Поиск во время воспроизведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16d7ad964335db100c84f0a396b7f13de7a270d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683026"
---
# <a name="how-to-seek-during-playback"></a><span data-ttu-id="fa59b-103">Поиск во время воспроизведения</span><span class="sxs-lookup"><span data-stu-id="fa59b-103">How to Seek During Playback</span></span>

<span data-ttu-id="fa59b-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fa59b-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fa59b-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="fa59b-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="fa59b-106">\]</span><span class="sxs-lookup"><span data-stu-id="fa59b-106">\]</span></span>

<span data-ttu-id="fa59b-107">В этом разделе описывается поиск во время воспроизведения с помощью Мфплай.</span><span class="sxs-lookup"><span data-stu-id="fa59b-107">This topic describes how to seek during playback using MFPlay.</span></span>

<span data-ttu-id="fa59b-108">**Поиск во время воспроизведения**</span><span class="sxs-lookup"><span data-stu-id="fa59b-108">**To Seek During Playback**</span></span>

1.  <span data-ttu-id="fa59b-109">Инициализируйте **пропвариант** для хранения времени поиска в единицах 100-наносекундных в виде **большого \_ целого** типа (**VT \_ i8**).</span><span class="sxs-lookup"><span data-stu-id="fa59b-109">Initialize a **PROPVARIANT** to hold the seek time in 100-nanosecond units, as a **LARGE\_INTEGER** (**VT\_I8**) type.</span></span>
2.  <span data-ttu-id="fa59b-110">Вызовите [**имфпмедиаплайер:: SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span><span class="sxs-lookup"><span data-stu-id="fa59b-110">Call [**IMFPMediaPlayer::SetPosition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition).</span></span> <span data-ttu-id="fa59b-111">Укажите **МФП \_ поситионтипе \_ 100 НС** для первого параметра и передайте **пропвариант** для второго параметра.</span><span class="sxs-lookup"><span data-stu-id="fa59b-111">Specify **MFP\_POSITIONTYPE\_100NS** for the first parameter, and pass in the **PROPVARIANT** for the second parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa59b-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fa59b-112">Requirements</span></span>

<span data-ttu-id="fa59b-113">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fa59b-113">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa59b-114">См. также</span><span class="sxs-lookup"><span data-stu-id="fa59b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa59b-115">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="fa59b-115">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



