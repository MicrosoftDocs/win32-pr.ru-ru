---
description: Пакет SDK для DirectShow и пакет SDK Windows Media Format
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: Пакет SDK для DirectShow и пакет SDK Windows Media Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351662"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a><span data-ttu-id="e9730-103">Пакет SDK для DirectShow и пакет SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="e9730-103">The DirectShow SDK and the Windows Media Format SDK</span></span>

<span data-ttu-id="e9730-104">DirectShow и пакет SDK для Windows Media Format предлагают дополнительные решения для создания приложений, которые создают и воспроизводят потоки формата Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e9730-104">DirectShow and the Windows Media Format SDK offer complementary solutions for writing applications that create and play back Windows Media Format streams.</span></span> <span data-ttu-id="e9730-105">Дополнительные сведения см. в разделе "[аудио и видео](../audio-and-video.md)" библиотеки MSDN.</span><span class="sxs-lookup"><span data-stu-id="e9730-105">For more information, see the "[Audio and Video](../audio-and-video.md)" section of the MSDN Library.</span></span>

<span data-ttu-id="e9730-106">Фильтр модуля записи ASF принимает любое количество входных потоков и создает файл ASF.</span><span class="sxs-lookup"><span data-stu-id="e9730-106">The ASF Writer filter accepts any number of input streams and creates an ASF file.</span></span> <span data-ttu-id="e9730-107">Фильтр использует Windows Media Format SDK для преобразования несжатых аудио-или видеофайлов в содержимое Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e9730-107">The filter uses the Windows Media Format SDK to convert uncompressed audio or video files to Windows Media-based content.</span></span> <span data-ttu-id="e9730-108">После этого сжатое содержимое сохраняется в формате контейнера ASF.</span><span class="sxs-lookup"><span data-stu-id="e9730-108">The compressed content is then stored in the ASF container format.</span></span> <span data-ttu-id="e9730-109">Если содержимое имеет только аудио, файл получает расширение WMA и называется аудиофайлом Windows Media Audio.</span><span class="sxs-lookup"><span data-stu-id="e9730-109">If the content is audio only, then the file is given a .wma extension and is referred to as a Windows Media Audio file.</span></span> <span data-ttu-id="e9730-110">Если содержимое относится только к видео или видео и аудио, файл получает расширение WMV и называется файлом видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e9730-110">If the content is video only or video and audio, then the file is given a .wmv extension and is referred to as a Windows Media Video file.</span></span> <span data-ttu-id="e9730-111">Оба типа файлов могут также включать метаданные.</span><span class="sxs-lookup"><span data-stu-id="e9730-111">Either type of file may also include metadata.</span></span>

<span data-ttu-id="e9730-112">Модуль записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов мультимедиа с чередованием (AVI) или MPEG для потоковой передачи в сети.</span><span class="sxs-lookup"><span data-stu-id="e9730-112">You can use the WM ASF Writer in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG multimedia files for network streaming.</span></span> <span data-ttu-id="e9730-113">Этот фильтр предоставляет единственный способ создания файлов Microsoft® Windows Media™ Audio (WMA) и Windows Media Video (WMV) в® DirectShow.</span><span class="sxs-lookup"><span data-stu-id="e9730-113">This filter provides the only way to create Microsoft® Windows Media™ Audio (WMA) and Windows Media Video (WMV) files in DirectShow®.</span></span> <span data-ttu-id="e9730-114">Фильтр также может создавать файлы, защищенные цифровыми Rights Management (DRM), и также может создавать содержимое MPEG-4 с помощью кодировщика Microsoft MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="e9730-114">The filter can also create files that are secured by Digital Rights Management (DRM), and can also create MPEG-4 content using the Microsoft MPEG-4 Encoder.</span></span> <span data-ttu-id="e9730-115">Это содержимое хранится в формате контейнера ASF.</span><span class="sxs-lookup"><span data-stu-id="e9730-115">This content is stored in the ASF container format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9730-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e9730-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9730-117">Создание файлов ASF в DirectShow</span><span class="sxs-lookup"><span data-stu-id="e9730-117">Creating ASF Files in DirectShow</span></span>](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
