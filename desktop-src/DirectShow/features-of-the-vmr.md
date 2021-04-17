---
description: Свойства VMR
ms.assetid: a809045b-b60d-4092-bc4d-0e70e17d2913
title: Свойства VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c4a5a34be9fb3b3bb08df18091b88fbe7d7432
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105673105"
---
# <a name="features-of-the-vmr"></a><span data-ttu-id="d1444-103">Свойства VMR</span><span class="sxs-lookup"><span data-stu-id="d1444-103">Features of the VMR</span></span>

<span data-ttu-id="d1444-104">Модуль подготовки видео 7 (VMR-7) поддерживает следующие новые функции:</span><span class="sxs-lookup"><span data-stu-id="d1444-104">The Video Mixing Renderer 7 (VMR-7) supports the following new features:</span></span>

-   <span data-ttu-id="d1444-105">Практическое смешение нескольких видеопотоков с использованием альфа-смешения устройств Direct3D.</span><span class="sxs-lookup"><span data-stu-id="d1444-105">Real mixing of multiple video streams, using the alpha-blending capabilities of Direct3D hardware devices.</span></span>
-   <span data-ttu-id="d1444-106">Возможность подключения собственного компонента компоновки для реализации эффектов и переходов между несколькими видеопотоками, входящими в VMR.</span><span class="sxs-lookup"><span data-stu-id="d1444-106">The ability to plug in your own compositing component to implement effects and transitions between multiple video streams entering the VMR.</span></span>
-   <span data-ttu-id="d1444-107">Истинная отрисовка без окна.</span><span class="sxs-lookup"><span data-stu-id="d1444-107">True windowless rendering.</span></span> <span data-ttu-id="d1444-108">Больше не нужно, чтобы окно воспроизведения видео было дочерним по отношению к окну приложения, чтобы оно содержало воспроизведение видео.</span><span class="sxs-lookup"><span data-stu-id="d1444-108">It is no longer necessary to make the video playback window a child of the application's window in order to contain video playback.</span></span> <span data-ttu-id="d1444-109">Новый режим рендеринга VMR позволяет приложениям легко размещать воспроизведение видео в любом окне без необходимости пересылать сообщения окна обработчику для обработки, зависящей от модуля подготовки отчетов.</span><span class="sxs-lookup"><span data-stu-id="d1444-109">The VMR's new windowless rendering mode allows applications to easily host video playback within any window without having to forward window messages to the renderer for renderer-specific processing.</span></span>
-   <span data-ttu-id="d1444-110">Новый режим воспроизведения без подготовки к просмотру, в котором приложения могут предоставлять собственный компонент распределителя для получения доступа к декодированному видеоизображению до его отображения на экране.</span><span class="sxs-lookup"><span data-stu-id="d1444-110">A new renderless playback mode where applications can supply their own allocator component to get access to the decoded video image prior to it being displayed on the screen.</span></span>
-   <span data-ttu-id="d1444-111">Улучшенная поддержка компьютеров, оснащенных несколькими мониторами.</span><span class="sxs-lookup"><span data-stu-id="d1444-111">Improved support for PCs equipped with multiple monitors.</span></span>
-   <span data-ttu-id="d1444-112">Поддержка новой архитектуры Microsoft DirectX для ускорения видео.</span><span class="sxs-lookup"><span data-stu-id="d1444-112">Support for Microsoft's new DirectX Video Acceleration architecture.</span></span>
-   <span data-ttu-id="d1444-113">Поддержка одновременного воспроизведения видео высокого качества в нескольких окнах.</span><span class="sxs-lookup"><span data-stu-id="d1444-113">Support for high-quality video playback concurrently on multiple windows.</span></span>
-   <span data-ttu-id="d1444-114">Поддержка монопольного режима DirectDraw</span><span class="sxs-lookup"><span data-stu-id="d1444-114">Support for DirectDraw Exclusive Mode</span></span>
-   <span data-ttu-id="d1444-115">100% обратная совместимость с существующими приложениями.</span><span class="sxs-lookup"><span data-stu-id="d1444-115">100% backward-compatibility with existing applications.</span></span>
-   <span data-ttu-id="d1444-116">Поддержка пошагового выполнения кадров и надежный способ записи текущего отображаемого изображения.</span><span class="sxs-lookup"><span data-stu-id="d1444-116">Support for frame stepping and a reliable way to capture the current image being displayed.</span></span>
-   <span data-ttu-id="d1444-117">Возможность приложений с легкостью альфа-смешения собственных статических данных изображения (например, логотипов каналов или компонентов пользовательского интерфейса) с помощью видео с плавным переходом без мерцания.</span><span class="sxs-lookup"><span data-stu-id="d1444-117">The ability for applications to easily alpha-blend their own static image data (such as channel logos or UI components) with the video in a smooth flicker-free way.</span></span>

<span data-ttu-id="d1444-118">VMR-9 поддерживает все перечисленные выше функции, а также:</span><span class="sxs-lookup"><span data-stu-id="d1444-118">The VMR-9 supports all the features listed above, plus:</span></span>

-   <span data-ttu-id="d1444-119">Возможность обрабатывать данные видео непосредственно с помощью интерфейсов API Direct3D, таких как шейдеры пикселей.</span><span class="sxs-lookup"><span data-stu-id="d1444-119">The ability to process video data directly with Direct3D APIs such as pixel shaders.</span></span>
-   <span data-ttu-id="d1444-120">Улучшенная поддержка чередования содержимого видео.</span><span class="sxs-lookup"><span data-stu-id="d1444-120">Improved support for interlaced video content.</span></span>
-   <span data-ttu-id="d1444-121">Поддержка любой платформы, поддерживаемой DirectX.</span><span class="sxs-lookup"><span data-stu-id="d1444-121">Support on any platform supported by DirectX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1444-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d1444-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1444-123">О рендеринге видео</span><span class="sxs-lookup"><span data-stu-id="d1444-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



