---
description: Поддержка VMR для ускорения видео DirectX
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: Поддержка VMR для ускорения видео DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811507"
---
# <a name="vmr-support-for-directx-video-acceleration"></a><span data-ttu-id="12ec8-103">Поддержка VMR для ускорения видео DirectX</span><span class="sxs-lookup"><span data-stu-id="12ec8-103">VMR Support for DirectX Video Acceleration</span></span>

<span data-ttu-id="12ec8-104">Ускорение видео DirectX — это интерфейс прикладного программирования (API) и соответствующий интерфейс драйвера устройства (DDI) для аппаратного ускорения обработки декодирования цифрового видео с поддержкой альфа-смешения для таких целей, как поддержка подизображений DVD.</span><span class="sxs-lookup"><span data-stu-id="12ec8-104">DirectX Video Acceleration is an Application Programming Interface (API) and a corresponding Device Driver Interface (DDI) for hardware acceleration of digital video decoding processing, with support of alpha blending for such purposes as DVD subpicture support.</span></span> <span data-ttu-id="12ec8-105">DirectX ва описан в Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="12ec8-105">DirectX VA is documented in the Windows DDK.</span></span> <span data-ttu-id="12ec8-106">В этом пакете SDK описан интерфейс [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) , который обеспечивает доступ к функциональности DirectX в пользовательском режиме на аппаратном устройстве.</span><span class="sxs-lookup"><span data-stu-id="12ec8-106">The [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) interface, which provides user mode access to DirectX VA functionality on a hardware device, is documented in this SDK.</span></span>

<span data-ttu-id="12ec8-107">VMR поддерживает [**иамвидеоакцелератор**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), и его реализация идентична старому микшеру наложения, за исключением одного важного отличия.</span><span class="sxs-lookup"><span data-stu-id="12ec8-107">The VMR supports [**IAMVideoAccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), and its implementation is identical to the old Overlay Mixer except for one important difference.</span></span> <span data-ttu-id="12ec8-108">Микшер наложения гарантирует, что выходные данные будут отображены в область наложения, тогда как VMR может отправить выходные данные для дальнейшей обработки, например трехмерную операцию, или отправить выходные данные на поверхность, которая затем блиттед на основную поверхность.</span><span class="sxs-lookup"><span data-stu-id="12ec8-108">The Overlay Mixer guaranteed that the output is rendered into an overlay surface, while the VMR can send the output for further processing, for example a 3D operation, or it might send the output to an offscreen surface which is then blitted to the primary surface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12ec8-109">См. также</span><span class="sxs-lookup"><span data-stu-id="12ec8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12ec8-110">Об ускорении видео DirectX</span><span class="sxs-lookup"><span data-stu-id="12ec8-110">About DirectX Video Acceleration</span></span>](about-directx-video-acceleration.md)
</dt> </dl>

 

 



