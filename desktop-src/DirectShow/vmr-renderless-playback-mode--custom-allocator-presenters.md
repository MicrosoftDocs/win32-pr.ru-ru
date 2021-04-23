---
description: Режим воспроизведения VMR (пользовательский распределитель — выступающие)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Режим воспроизведения VMR (пользовательский распределитель — выступающие)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815248"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a><span data-ttu-id="0ad54-103">Режим воспроизведения VMR (пользовательский распределитель — выступающие)</span><span class="sxs-lookup"><span data-stu-id="0ad54-103">VMR Renderless Playback Mode (Custom Allocator-Presenters)</span></span>

<span data-ttu-id="0ad54-104">В режиме воспроизведения фильтр VMR не выполняет отрисовку.</span><span class="sxs-lookup"><span data-stu-id="0ad54-104">In renderless playback mode, the VMR does not perform the rendering.</span></span> <span data-ttu-id="0ad54-105">Вместо этого он использует пользовательский распределитель-представление, предоставляемое приложением.</span><span class="sxs-lookup"><span data-stu-id="0ad54-105">Instead, it uses a custom allocator-presenter supplied by the application.</span></span> <span data-ttu-id="0ad54-106">Этот режим удобен для игр и других типов приложений, которые имеют сложные видеоэффекты.</span><span class="sxs-lookup"><span data-stu-id="0ad54-106">This mode is useful for games and other types of applications that have sophisticated video effects.</span></span> <span data-ttu-id="0ad54-107">Режим воспроизведения, не поддерживающий рендеринг, позволяет приложениям создавать и контролировать собственную поверхность DirectDraw (VMR-7) или поверхность Direct3D (VMR-9), а также получать доступ к видео-битам во время презентации.</span><span class="sxs-lookup"><span data-stu-id="0ad54-107">Renderless playback mode enables the applications to create and control its own DirectDraw surface (VMR-7) or Direct3D surface (VMR-9), and to access the video bits at presentation time.</span></span>

<span data-ttu-id="0ad54-108">В режиме без отображения VMR-9 не загружает компонент микшера автоматически.</span><span class="sxs-lookup"><span data-stu-id="0ad54-108">In renderless mode, the VMR-9 does not automatically load its mixer component.</span></span>

<span data-ttu-id="0ad54-109">В режиме воспроизведения без отрисовок приложение выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="0ad54-109">In renderless playback mode, the application does the following tasks:</span></span>

-   <span data-ttu-id="0ad54-110">Управляет окном воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0ad54-110">Manages the playback window.</span></span>
-   <span data-ttu-id="0ad54-111">Выделяет объект DirectDraw или Direct3D и конечный буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="0ad54-111">Allocates the DirectDraw or Direct3D object and the final frame buffer.</span></span>
-   <span data-ttu-id="0ad54-112">Уведомляет оставшуюся часть системы воспроизведения используемого объекта.</span><span class="sxs-lookup"><span data-stu-id="0ad54-112">Notifies the rest of the playback system of the object being used.</span></span>
-   <span data-ttu-id="0ad54-113">Представляет буфер фрейма в нужное время.</span><span class="sxs-lookup"><span data-stu-id="0ad54-113">Presents the frame buffer at the correct time.</span></span>
-   <span data-ttu-id="0ad54-114">Обрабатывает все изменения режима разрешения, изменения монитора и потери поверхности.</span><span class="sxs-lookup"><span data-stu-id="0ad54-114">Handles all resolution-mode changes, monitor changes, and surface losses.</span></span> <span data-ttu-id="0ad54-115">Он должен рекомендовать оставшуюся часть системы воспроизведения этих событий.</span><span class="sxs-lookup"><span data-stu-id="0ad54-115">It must advise the rest of the playback system of these events.</span></span>

<span data-ttu-id="0ad54-116">VMR выполняет следующие действия:</span><span class="sxs-lookup"><span data-stu-id="0ad54-116">The VMR does the following:</span></span>

-   <span data-ttu-id="0ad54-117">Обрабатывает все временные рамки, связанные с представлением видеокадра.</span><span class="sxs-lookup"><span data-stu-id="0ad54-117">Handles all timing related to presenting the video frame.</span></span>
-   <span data-ttu-id="0ad54-118">Предоставляет сведения контроля качества приложению и остальной части системы воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="0ad54-118">Provides quality-control information to the application and the rest of the playback system.</span></span>
-   <span data-ttu-id="0ad54-119">Представляет собой последовательный интерфейс для восходящих компонентов системы воспроизведения, которые не знают о том, что приложение предоставляет выделение буфера фрейма и выполнение отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0ad54-119">Presents a consistent interface to the upstream components of the playback system, which are not aware that the application is providing the frame buffer allocation and performing the rendering.</span></span>
-   <span data-ttu-id="0ad54-120">Предоставляет все смешение видеопотоков, которые могут потребоваться перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="0ad54-120">Provides any mixing of video streams that may be required prior to rendering.</span></span>

<span data-ttu-id="0ad54-121">Так как разчередование выполняется микшером, распределитель-выступающий всегда получает нечередующиеся кадры.</span><span class="sxs-lookup"><span data-stu-id="0ad54-121">Because deinterlacing is performed by the mixer, the allocator-presenter always received deinterlaced frames.</span></span> <span data-ttu-id="0ad54-122">Дополнительные сведения см. в разделе [Настройка параметров дечередования](setting-deinterlace-preferences.md).</span><span class="sxs-lookup"><span data-stu-id="0ad54-122">For more information, see [Setting Deinterlace Preferences](setting-deinterlace-preferences.md).</span></span>

<span data-ttu-id="0ad54-123">Дополнительные сведения о предоставлении пользовательского распределителя-Presenter см. в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="0ad54-123">For more information about providing a custom allocator-presenter, see the following topics:</span></span>

-   [<span data-ttu-id="0ad54-124">Предоставление пользовательского Allocator-Presenter для VMR-7</span><span class="sxs-lookup"><span data-stu-id="0ad54-124">Supplying a Custom Allocator-Presenter for VMR-7</span></span>](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [<span data-ttu-id="0ad54-125">Предоставление пользовательского Allocator-Presenter для VMR-9</span><span class="sxs-lookup"><span data-stu-id="0ad54-125">Supplying a Custom Allocator-Presenter for VMR-9</span></span>](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [<span data-ttu-id="0ad54-126">Синхронизация VMR с частотой обновления монитора</span><span class="sxs-lookup"><span data-stu-id="0ad54-126">Synchronizing the VMR to the Monitor's Refresh Rate</span></span>](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



