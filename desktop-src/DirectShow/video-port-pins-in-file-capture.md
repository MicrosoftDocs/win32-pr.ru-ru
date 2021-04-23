---
description: Контакты порта видео в записи файлов
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Контакты порта видео в записи файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673447"
---
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="720dd-103">Контакты порта видео в записи файлов</span><span class="sxs-lookup"><span data-stu-id="720dd-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="720dd-104">Если устройство записи имеет порт видео, то ПИН-код видеопорта должен быть подключен к модулю обработки видео, даже если требуется только запись в файл.</span><span class="sxs-lookup"><span data-stu-id="720dd-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="720dd-105">Если вы вызываете [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) со значением **\_ \_ запись категории ПИН-кода** , а устройство имеет ПИН-код видеопорта, то построитель диаграмм автоматически подключает ПИН-код видеопорта к фильтру [микшера наложения](overlay-mixer-filter.md) и подключает микшер наложения к модулю визуализации видео.</span><span class="sxs-lookup"><span data-stu-id="720dd-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="720dd-106">Построитель графа записи скрывает окно видео, вызывая [**ивидеовиндов::p UT \_ автоотображения**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) со значением **оафалсе**.</span><span class="sxs-lookup"><span data-stu-id="720dd-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="720dd-107">Если позже приложение вызывает **RenderStream** с **\_ \_ предварительной версией категории ПИН-кода**, построитель диаграмм выполнит вызов **поместит \_ Автоотображение** со значением **оатруе**, чтобы отобразить окно видео.</span><span class="sxs-lookup"><span data-stu-id="720dd-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="720dd-108">После вызова **RenderStream** с **\_ \_ захватом категории ПИН-кода** можно проверить, добавлен ли модуль подготовки видео, выполнив запрос к диспетчеру графа фильтра для интерфейса [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="720dd-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="720dd-109">См. также</span><span class="sxs-lookup"><span data-stu-id="720dd-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="720dd-110">Запись видео в файл</span><span class="sxs-lookup"><span data-stu-id="720dd-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



