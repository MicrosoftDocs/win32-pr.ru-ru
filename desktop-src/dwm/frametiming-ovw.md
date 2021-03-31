---
title: Доступ к данным кадра DWM и управление ими
description: В этом разделе обсуждаются интерфейсы API диспетчер окон рабочего стола (DWM), которые используются для планирования и представления мультимедиа.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- API-интерфейсы представления диспетчер окон рабочего стола (DWM), планирования и мультимедиа
- Интерфейсы API презентации DWM (диспетчер окон рабочего стола), планирования и мультимедиа
- API-интерфейсы представления планирования и мультимедиа
- Диспетчер окон рабочего стола (DWM), доступ к данным кадра
- DWM (диспетчер окон рабочего стола), доступ к данным кадра
- доступ к данным кадра
- Диспетчер окон рабочего стола (DWM), управление данными кадра
- DWM (диспетчер окон рабочего стола), управление данными кадров
- Управление данными кадров
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330280"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="5208b-112">Доступ к данным кадра DWM и управление ими</span><span class="sxs-lookup"><span data-stu-id="5208b-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="5208b-113">В этом разделе обсуждаются интерфейсы API диспетчер окон рабочего стола (DWM), которые используются для планирования и представления мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="5208b-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="5208b-114">API времени кадров DWM</span><span class="sxs-lookup"><span data-stu-id="5208b-114">DWM Frame Timing API</span></span>

<span data-ttu-id="5208b-115">API-интерфейсы представления расписания и мультимедиа позволяют более детально контролировать, когда образ настольного компьютера является составным и представленным.</span><span class="sxs-lookup"><span data-stu-id="5208b-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="5208b-116">Обычно это требуется для приложений воспроизведения мультимедиа и видео, для которых диспетчер DWM выполняется асинхронно с собственным расписанием представления, что может привести к выборке артефактов, если не было жестко контролироваться.</span><span class="sxs-lookup"><span data-stu-id="5208b-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="5208b-117">Функции планирования и презентации мультимедиа включают следующее.</span><span class="sxs-lookup"><span data-stu-id="5208b-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="5208b-118">Сведения об их использовании находятся на этих страницах.</span><span class="sxs-lookup"><span data-stu-id="5208b-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="5208b-119">[**Двменаблеммксс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span><span class="sxs-lookup"><span data-stu-id="5208b-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="5208b-120">Уведомляет DWM о том, что планируется включить планирование службы обработки и планирования (MMCSS) класса мультимедиа, пока вызывающий процесс находится в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="5208b-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="5208b-121">[**Двмжеткомпоситионтимингинфо**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span><span class="sxs-lookup"><span data-stu-id="5208b-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="5208b-122">Извлекает сведения о текущем времени композиции.</span><span class="sxs-lookup"><span data-stu-id="5208b-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="5208b-123">[**Двммодифипревиаусдксфрамедуратион**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="5208b-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="5208b-124">Изменяет число обновлений, в течение которых будет отображаться предыдущий кадр.</span><span class="sxs-lookup"><span data-stu-id="5208b-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="5208b-125">[**Двмсетдксфрамедуратион**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="5208b-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="5208b-126">Задает количество обновлений, в которых отображается отображаемый кадр.</span><span class="sxs-lookup"><span data-stu-id="5208b-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="5208b-127">[**Двмсетпресентпараметерс**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span><span class="sxs-lookup"><span data-stu-id="5208b-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="5208b-128">Задает существующие параметры для компоновки кадра.</span><span class="sxs-lookup"><span data-stu-id="5208b-128">Sets the present parameters for frame composition.</span></span>

 

 




