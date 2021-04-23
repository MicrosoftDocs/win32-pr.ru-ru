---
description: Ускорение видео DirectX 2,0
ms.assetid: acb73b20-89fa-4a48-be4a-846715a239b0
title: Ускорение видео DirectX 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3ae813d3c81ebcf753dcaa273cc9f9149eaab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262792"
---
# <a name="directx-video-acceleration-20"></a><span data-ttu-id="61242-103">Ускорение видео DirectX 2,0</span><span class="sxs-lookup"><span data-stu-id="61242-103">DirectX Video Acceleration 2.0</span></span>

<span data-ttu-id="61242-104">Ускорение видео DirectX (ДКСВА) — это API и соответствующий DDI для использования аппаратного ускорения для ускорения обработки видеокодеков.</span><span class="sxs-lookup"><span data-stu-id="61242-104">DirectX Video Acceleration (DXVA) is an API and a corresponding DDI for using hardware-acceleration to speed up video codec processing.</span></span> <span data-ttu-id="61242-105">Программные кодеки и видеопроцессоры могут использовать ДКСВА для разгрузки определенных вычислительных операций в GPU.</span><span class="sxs-lookup"><span data-stu-id="61242-105">Software codecs and software video processors can use DXVA to offload certain CPU-intensive operations to the GPU.</span></span> <span data-ttu-id="61242-106">Например, программный декодер может разгрузить обратное дискретное преобразование косинуса (идкт) в GPU.</span><span class="sxs-lookup"><span data-stu-id="61242-106">For example, a software decoder can offload the inverse discrete cosine transform (iDCT) to the GPU.</span></span>

<span data-ttu-id="61242-107">Этот раздел содержит следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="61242-107">This section contains the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="61242-108">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="61242-108">In this section</span></span>



| <span data-ttu-id="61242-109">Раздел</span><span class="sxs-lookup"><span data-stu-id="61242-109">Topic</span></span>                                                                                             | <span data-ttu-id="61242-110">Описание</span><span class="sxs-lookup"><span data-stu-id="61242-110">Description</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61242-111">О ДКСВА 2,0</span><span class="sxs-lookup"><span data-stu-id="61242-111">About DXVA 2.0</span></span>](about-dxva-2-0.md)<br/>                                                   | <span data-ttu-id="61242-112">Общие сведения о ДКСВА 2 и его связи с ДКСВА 1.</span><span class="sxs-lookup"><span data-stu-id="61242-112">Overview of DXVA 2 and its relation to DXVA 1.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="61242-113">диспетчер устройств Direct3D</span><span class="sxs-lookup"><span data-stu-id="61242-113">Direct3D Device Manager</span></span>](direct3d-device-manager.md)<br/>                                 | <span data-ttu-id="61242-114">Диспетчер устройств Microsoft Direct3D позволяет нескольким объектам совместно использовать одно и то же устройство Microsoft Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="61242-114">The Microsoft Direct3D device manager enables two or more objects to share the same Microsoft Direct3D 9 device.</span></span><br/>                                                                                      |
| [<span data-ttu-id="61242-115">Поддержка ДКСВА 2,0 в DirectShow</span><span class="sxs-lookup"><span data-stu-id="61242-115">Supporting DXVA 2.0 in DirectShow</span></span>](supporting-dxva-2-0-in-directshow.md)<br/>             | <span data-ttu-id="61242-116">В этом разделе описано, как поддерживать ускорение видео DirectX (ДКСВА) 2,0 в фильтре декодера DirectShow.</span><span class="sxs-lookup"><span data-stu-id="61242-116">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a DirectShow decoder filter.</span></span><br/>                                                                                             |
| [<span data-ttu-id="61242-117">Поддержка ДКСВА 2,0 в Media Foundation</span><span class="sxs-lookup"><span data-stu-id="61242-117">Supporting DXVA 2.0 in Media Foundation</span></span>](supporting-dxva-2-0-in-media-foundation.md)<br/> | <span data-ttu-id="61242-118">В этом разделе описывается поддержка ускорения видео DirectX (ДКСВА) 2,0 в преобразовании Media Foundation (MFT) с помощью Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="61242-118">This topic describes how to support DirectX Video Acceleration (DXVA) 2.0 in a Media Foundation transform (MFT) using Direct3D 9</span></span><br/>                                                                      |
| [<span data-ttu-id="61242-119">Обработка видео ДКСВА</span><span class="sxs-lookup"><span data-stu-id="61242-119">DXVA Video Processing</span></span>](dxva-video-processing.md)<br/>                                     | <span data-ttu-id="61242-120">ДКСВА обработка видео включает функции графического оборудования, предназначенные для обработки несжатых видеоизображений.</span><span class="sxs-lookup"><span data-stu-id="61242-120">DXVA video processing encapsulates the functions of the graphics hardware that are devoted to processing uncompressed video images.</span></span> <span data-ttu-id="61242-121">Службы обработки видео включают в себя дечередование и смешение видео.</span><span class="sxs-lookup"><span data-stu-id="61242-121">Video processing services include deinterlacing and video mixing.</span></span><br/> |
| [<span data-ttu-id="61242-122">ДКСВА-HD</span><span class="sxs-lookup"><span data-stu-id="61242-122">DXVA-HD</span></span>](dxva-hd.md)<br/>                                                                 | <span data-ttu-id="61242-123">High Definition (ДКСВА-HD) ускорение видео Microsoft DirectX — это API для обработки видео с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="61242-123">Microsoft DirectX Video Acceleration High Definition (DXVA-HD) is an API for hardware-accelerated video processing.</span></span> <br/>                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="61242-124">См. также</span><span class="sxs-lookup"><span data-stu-id="61242-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61242-125">Media Foundationое программное руководством</span><span class="sxs-lookup"><span data-stu-id="61242-125">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> <dt>

[<span data-ttu-id="61242-126">Спецификация ДКСВА 1</span><span class="sxs-lookup"><span data-stu-id="61242-126">DXVA 1 Specification</span></span>](/windows-hardware/drivers/display/directx-video-acceleration)
</dt> </dl>

 

 
