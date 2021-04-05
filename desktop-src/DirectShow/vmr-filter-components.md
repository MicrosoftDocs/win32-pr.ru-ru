---
description: Компоненты фильтра VMR
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: Компоненты фильтра VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b597f6ac1b52f81ddc26d18e3fe0c6d16bae9515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546039"
---
# <a name="vmr-filter-components"></a><span data-ttu-id="fb112-103">Компоненты фильтра VMR</span><span class="sxs-lookup"><span data-stu-id="fb112-103">VMR Filter Components</span></span>

<span data-ttu-id="fb112-104">VMR использует модульный проект, позволяющий приложениям настраивать его для многих различных сценариев отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fb112-104">The VMR employs a modular design that enables applications to configure it for many different rendering scenarios.</span></span> <span data-ttu-id="fb112-105">В зависимости от конфигурации VMR содержит от двух до пяти подкомпонентов (в дополнение к входным ПИН-данным).</span><span class="sxs-lookup"><span data-stu-id="fb112-105">Depending on its configuration, the VMR contains from two to five subcomponents (in addition to its input pins).</span></span>

![VMR в оконном режиме с несколькими потоками](images/vmr-multiple-streams.png)

<span data-ttu-id="fb112-107">**Микшер:** Микшер — это COM-объект, отвечающий за смешение нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="fb112-107">**Mixer:** The mixer is a COM object responsible for mixing multiple streams.</span></span> <span data-ttu-id="fb112-108">Дечередование также происходит внутри микшера.</span><span class="sxs-lookup"><span data-stu-id="fb112-108">Deinterlacing also occurs inside the mixer.</span></span> <span data-ttu-id="fb112-109">Микшер загружается с помощью VMR при обнаружении нескольких входных потоков или при чередовании входного видео.</span><span class="sxs-lookup"><span data-stu-id="fb112-109">The mixer is loaded by the VMR when multiple input streams are detected, or when the input video is interlaced.</span></span> <span data-ttu-id="fb112-110">Микшер собирает сведения о каждом входном потоке и сортирует потоки в правильном Z-порядке.</span><span class="sxs-lookup"><span data-stu-id="fb112-110">The mixer collects information about each input stream and sorts the streams into the correct Z-order.</span></span> <span data-ttu-id="fb112-111">Он отвечает за определение того, получает ли каждый входной ПИН-код выборку, а также указывает, что в нужное время для выполнения фактического смешения используется компоновщик изображений.</span><span class="sxs-lookup"><span data-stu-id="fb112-111">It is responsible for determining when each input pin receives a sample, and for instructing the image compositor at the proper time to perform the actual blending.</span></span> <span data-ttu-id="fb112-112">Микшер также вычисляет отметку времени, которая будет применена к каждому выходному изображению.</span><span class="sxs-lookup"><span data-stu-id="fb112-112">The mixer also calculates the time stamp to be applied to each output image.</span></span> <span data-ttu-id="fb112-113">Когда приложение предоставляет точечный рисунок, отображаемый поверх составного изображения, микшер отвечает за обеспечение отображения точечного рисунка поверх остальных элементов, даже если изменяется Z-порядок входных потоков.</span><span class="sxs-lookup"><span data-stu-id="fb112-113">When the application is supplying a bitmap to be displayed on top of the composited image, the mixer is responsible for ensuring that the bitmap is displayed on top even if the Z-order of the input streams is modified.</span></span>

<span data-ttu-id="fb112-114">**Компоновщик изображений:** Компоновщик изображений — это COM-объект, который выполняет фактическое смешивание входных потоков на одной поверхности DirectDraw или Direct3D, предоставляемой распределителем.</span><span class="sxs-lookup"><span data-stu-id="fb112-114">**Image Compositor:** The Image Compositor is a COM object that performs the actual blending of the input streams onto a single DirectDraw or Direct3D surface provided by the allocator-presenter.</span></span> <span data-ttu-id="fb112-115">VMR предоставляет компоновщик изображений по умолчанию, позволяющий приложениям выполнять двумерные трехмерные эффекты альфа-смешения.</span><span class="sxs-lookup"><span data-stu-id="fb112-115">The VMR provides a default image compositor that enables applications to perform 2-D alpha-blending effects.</span></span> <span data-ttu-id="fb112-116">Приложения могут предоставлять пользовательский набор изображений, чтобы включить другие плоские и трехмерные эффекты, такие как применение текстур к частям изображения, смешение альфа-канала на пиксель, сопоставление изображения с стационарными или перемещаемыми трехмерными объектами и т. д.</span><span class="sxs-lookup"><span data-stu-id="fb112-116">Applications can provide a custom image compositor to enable other 2-D and 3-D effects, such as applying textures to portions of the image, per-pixel alpha blending, mapping the image to stationary or moving 3-D objects, and so on.</span></span>

<span data-ttu-id="fb112-117">**Распределитель-выступающий:** Распределитель-выступающий — это COM-объект, который выделяет объект DirectDraw или Direct3D и обрабатывает связь с графической картой.</span><span class="sxs-lookup"><span data-stu-id="fb112-117">**Allocator-Presenter:** The allocator-presenter is a COM object that allocates the DirectDraw or Direct3D object and handles the communication with the graphics card.</span></span> <span data-ttu-id="fb112-118">Рисование можно выполнить как отразить или как Блит.</span><span class="sxs-lookup"><span data-stu-id="fb112-118">The drawing can be performed either as a flip or as a blit.</span></span> <span data-ttu-id="fb112-119">Вы можете подключить собственный распределитель-представление для создания и управления объектом DirectDraw или Direct3D, а также для получения доступа к видеороликам во время презентации.</span><span class="sxs-lookup"><span data-stu-id="fb112-119">You can plug in your own allocator-presenter in order to create and control the DirectDraw or Direct3D object, and/or to obtain access to the video bits at presentation time.</span></span>

<span data-ttu-id="fb112-120">**Диспетчер окон:** Диспетчер окон используется только в оконном режиме.</span><span class="sxs-lookup"><span data-stu-id="fb112-120">**Window Manager:** The Window Manager is used only in windowed mode.</span></span> <span data-ttu-id="fb112-121">Диспетчер окон поддерживает устаревшие интерфейсы [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) и [**ибасиквидео**](/windows/desktop/api/Control/nn-control-ibasicvideo) для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="fb112-121">The Window Manager supports the legacy [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) and [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) interfaces for backward-compatibility.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb112-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fb112-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb112-123">О рендеринге видео</span><span class="sxs-lookup"><span data-stu-id="fb112-123">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
</dt> </dl>

 

 



