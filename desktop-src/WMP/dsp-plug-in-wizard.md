---
title: Мастер подключаемых модулей DSP
description: Мастер подключаемых модулей DSP
ms.assetid: 3d1ae5ef-12c4-4db3-815a-2adc73353f20
keywords:
- Подключаемые модули проигрывателя Windows Media, мастер подключаемых модулей
- подключаемые модули, мастер подключаемых модулей
- подключаемые модули обработки цифровых сигналов, мастер подключаемых модулей
- Подключаемые модули DSP, мастер подключаемых модулей
- Мастер подключаемых модулей
- Visual Studio, мастер подключаемых модулей DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a7228056d821d2c2bca258f5c236fe1dce11d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532078"
---
# <a name="dsp-plug-in-wizard"></a><span data-ttu-id="d1233-109">Мастер подключаемых модулей DSP</span><span class="sxs-lookup"><span data-stu-id="d1233-109">DSP Plug-in Wizard</span></span>

<span data-ttu-id="d1233-110">Пакет SDK для проигрывателя Windows Media предоставляет мастер подключаемых модулей, который можно добавить в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="d1233-110">The Windows Media Player SDK provides a plug-in wizard that you can add to Visual Studio.</span></span> <span data-ttu-id="d1233-111">Мастер может создать пример кода для различных подключаемых модулей, включая следующие типы подключаемых модулей DSP:</span><span class="sxs-lookup"><span data-stu-id="d1233-111">The wizard can generate sample code for a variety of plug-ins, including the following types of DSP plug-ins:</span></span>

-   <span data-ttu-id="d1233-112">Подключаемый модуль DSP аудиоподсистемы</span><span class="sxs-lookup"><span data-stu-id="d1233-112">Audio DSP plug-in</span></span>
-   <span data-ttu-id="d1233-113">Подключаемый модуль DSP аудиоподсистемы (в двух режимах)</span><span class="sxs-lookup"><span data-stu-id="d1233-113">Audio DSP plug-in (dual mode)</span></span>
-   <span data-ttu-id="d1233-114">Подключаемый модуль DSP видео</span><span class="sxs-lookup"><span data-stu-id="d1233-114">Video DSP plug-in</span></span>
-   <span data-ttu-id="d1233-115">Подключаемый модуль DSP видео (в двух режимах)</span><span class="sxs-lookup"><span data-stu-id="d1233-115">Video DSP plug-in (dual mode)</span></span>

<span data-ttu-id="d1233-116">Каждый из двух базовых примеров подключаемых модулей, DSP аудио и видео DSP функционирует как объект мультимедиа DirectX (DMO).</span><span class="sxs-lookup"><span data-stu-id="d1233-116">Each of the two basic sample plug-ins, Audio DSP and Video DSP, functions as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="d1233-117">Это значит, что каждый пример подключаемого модуля реализует интерфейс **имедиаобжект** .</span><span class="sxs-lookup"><span data-stu-id="d1233-117">That is, each sample plug-in implements the **IMediaObject** interface.</span></span> <span data-ttu-id="d1233-118">Каждый из двух подключаемых модулей с двойным режимом может функционировать как DMO или как преобразование Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d1233-118">Each of the two dual-mode sample plug-ins can function either as a DMO or as a Media Foundation Transform (MFT).</span></span> <span data-ttu-id="d1233-119">Это значит, что каждый двойной подключаемый модуль с двойным режимом реализует интерфейс **имедиаобжект** и интерфейс **имфтрансформ** .</span><span class="sxs-lookup"><span data-stu-id="d1233-119">That is, each dual-mode sample plug-in implements both the **IMediaObject** interface and the **IMFTransform** interface.</span></span>

<span data-ttu-id="d1233-120">Вы можете компилировать, связывать, регистрировать и тестировать пример кода подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="d1233-120">You can compile, link, register, and test the sample plug-in code.</span></span> <span data-ttu-id="d1233-121">Затем можно изменить созданный пример кода, чтобы создать собственный подключаемый модуль DSP.</span><span class="sxs-lookup"><span data-stu-id="d1233-121">Then you can modify the generated sample code to create your own DSP plug-in.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1233-122">См. также</span><span class="sxs-lookup"><span data-stu-id="d1233-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1233-123">**Создание подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="d1233-123">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> <dt>

[<span data-ttu-id="d1233-124">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="d1233-124">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> <dt>

[<span data-ttu-id="d1233-125">**Обновления мастера подключаемых модулей DSP для проигрывателя Windows Media 11**</span><span class="sxs-lookup"><span data-stu-id="d1233-125">**Updates to the DSP Plug-in Wizard for Windows Media Player 11**</span></span>](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)
</dt> </dl>

 

 




