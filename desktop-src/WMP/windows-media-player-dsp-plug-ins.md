---
title: Подключаемые модули DSP проигрывателя Windows Media
description: Подключаемые модули DSP проигрывателя Windows Media
ms.assetid: 1c7202c4-ca66-491d-9a5f-26032cad1dcc
keywords:
- Проигрыватель Windows Media, подключаемые модули
- Проигрыватель Windows Media, подключаемые модули DSP
- Подключаемые модули проигрывателя Windows Media, обработка цифровых сигналов (DSP)
- подключаемые модули, обработка цифровых сигналов (DSP)
- подключаемые модули обработки цифровых сигналов, о
- Подключаемые модули DSP, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 755088bce89530350997d2f543e30872f630e882
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486885"
---
# <a name="windows-media-player-dsp-plug-ins"></a><span data-ttu-id="5277c-109">Подключаемые модули DSP проигрывателя Windows Media</span><span class="sxs-lookup"><span data-stu-id="5277c-109">Windows Media Player DSP Plug-ins</span></span>

<span data-ttu-id="5277c-110">Проигрыватель Microsoft Windows Media предоставляет архитектуру, позволяющую пользователю устанавливать и активировать подключаемые программы, которые добавляют функции обработки цифровой сигнализации (DSP).</span><span class="sxs-lookup"><span data-stu-id="5277c-110">Microsoft Windows Media Player provides an architecture that enables the user to install and activate plug-in programs that add digital signal processing (DSP) functionality.</span></span> <span data-ttu-id="5277c-111">Подключаемый модуль DSP — это объект мультимедиа Microsoft DirectX (DMO) или преобразование Media Foundation (MFT), которое подключается к проигрывателю с помощью COM-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="5277c-111">A DSP plug-in is a Microsoft DirectX Media Object (DMO) or a Media Foundation Transform (MFT) that connects to the Player by using COM interfaces.</span></span> <span data-ttu-id="5277c-112">Типичным подключаемым модулем DSP может быть аудио-эквалайзер или элемент управления "оттенок видео".</span><span class="sxs-lookup"><span data-stu-id="5277c-112">A typical DSP plug-in might be an audio equalizer or a video tint control.</span></span> <span data-ttu-id="5277c-113">В этом разделе пакета SDK содержатся сведения о программировании, необходимые для создания собственного подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="5277c-113">This section of the SDK provides the programming information you need to create your own DSP plug-in.</span></span>

<span data-ttu-id="5277c-114">Документация по подключаемому модулю DSP делится на следующие три раздела.</span><span class="sxs-lookup"><span data-stu-id="5277c-114">The DSP plug-in documentation is divided into the following three sections.</span></span>



| <span data-ttu-id="5277c-115">Section</span><span class="sxs-lookup"><span data-stu-id="5277c-115">Section</span></span>                                                                      | <span data-ttu-id="5277c-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5277c-116">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5277c-117">О подключаемых модулях DSP</span><span class="sxs-lookup"><span data-stu-id="5277c-117">About DSP Plug-ins</span></span>](about-dsp-plug-ins.md)                                 | <span data-ttu-id="5277c-118">Содержит общие сведения об архитектуре, используемой для подключаемых модулей DSP. Ознакомьтесь с этим разделом, чтобы узнать об общих принципах, связанных с этой технологией.</span><span class="sxs-lookup"><span data-stu-id="5277c-118">Provides an overview of the architecture used for DSP plug-ins. Read this section to learn the general concepts involved with this technology.</span></span>  |
| [<span data-ttu-id="5277c-119">Программное руководством по программированию для подключаемых модулей DSP</span><span class="sxs-lookup"><span data-stu-id="5277c-119">DSP Plug-ins Programming Guide</span></span>](dsp-plug-ins-programming-guide.md)         | <span data-ttu-id="5277c-120">Объясняет, что необходимо сделать для создания подключаемого модуля DSP.</span><span class="sxs-lookup"><span data-stu-id="5277c-120">Explains what you need to do to create a DSP plug-in.</span></span> <span data-ttu-id="5277c-121">Этот раздел содержит пример кода и пошаговые процедуры.</span><span class="sxs-lookup"><span data-stu-id="5277c-121">This section contains example code and step-by-step procedures.</span></span>                           |
| [<span data-ttu-id="5277c-122">Справочник по программированию подключаемых модулей DSP</span><span class="sxs-lookup"><span data-stu-id="5277c-122">DSP Plug-ins Programming Reference</span></span>](dsp-plug-ins-programming-reference.md) | <span data-ttu-id="5277c-123">Содержит подробный справочник по COM-интерфейсам, методам и перечислимым типам, поддерживаемым пакетом SDK проигрывателя Windows Media для подключаемых модулей DSP.</span><span class="sxs-lookup"><span data-stu-id="5277c-123">Provides a detailed reference for the COM interfaces, methods, and enumerated types supported by the Windows Media Player SDK for DSP plug-ins.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5277c-124">См. также</span><span class="sxs-lookup"><span data-stu-id="5277c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5277c-125">**Подключаемые модули проигрывателя Windows Media**</span><span class="sxs-lookup"><span data-stu-id="5277c-125">**Windows Media Player Plug-ins**</span></span>](windows-media-player-plug-ins.md)
</dt> </dl>

 

 




