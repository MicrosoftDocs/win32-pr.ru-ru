---
title: Обзор образца эхо
description: Обзор образца эхо
ms.assetid: df9ad8f4-8c17-44b8-b5ee-c86de44788cf
keywords:
- Подключаемые модули проигрывателя Windows Media, обзор эхо-образца
- подключаемые модули, Обзор примера эхо
- подключаемые модули обработки цифровых сигналов, обзор образца эха
- Подключаемые модули DSP, Обзор примера эхо
- Пример подключаемого модуля Echo DSP, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1081b6d54ce34581bb6231d5617dd300e392ad71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691297"
---
# <a name="echo-sample-overview"></a><span data-ttu-id="c2ef8-108">Обзор образца эхо</span><span class="sxs-lookup"><span data-stu-id="c2ef8-108">Echo Sample Overview</span></span>

<span data-ttu-id="c2ef8-109">В этом руководством создается подключаемый модуль DSP для проигрывателя Windows Media, который создает эхо в звуковой записи PCM во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-109">This guide builds a Windows Media Player DSP plug-in that creates an echo effect in PCM audio during playback.</span></span> <span data-ttu-id="c2ef8-110">Ниже приведены цели для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-110">The goals for the plug-in are as follows:</span></span>

-   <span data-ttu-id="c2ef8-111">Подключаемый модуль обрабатывает 8-разрядный или 16-разрядный звук PCM.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-111">The plug-in processes 8-bit or 16-bit PCM audio only.</span></span>
-   <span data-ttu-id="c2ef8-112">Он поддерживает время задержки от 10 миллисекунд (МС) до 2000 мс (2 секунды).</span><span class="sxs-lookup"><span data-stu-id="c2ef8-112">It supports a delay time between 10 milliseconds (ms) and 2000 ms (2 seconds).</span></span> <span data-ttu-id="c2ef8-113">Это представляет практический диапазон для большинства приложений.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-113">This represents a practical range for most applications.</span></span>
-   <span data-ttu-id="c2ef8-114">Он поддерживает смешивание исходного сигнала с помощью сигнала задержки.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-114">It supports mixing of the original signal with the delay signal.</span></span>
-   <span data-ttu-id="c2ef8-115">Он предоставляет реализацию страницы свойств, которая позволяет пользователю указать значение времени задержки и значение для процентного сигнала задержки относительно общего уровня звукового сигнала.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-115">It provides a property page implementation that allows the user to provide a value for the delay time and a value for the percentage of delay signal relative to the overall audio signal level.</span></span>
-   <span data-ttu-id="c2ef8-116">Код создается путем изменения примера подключаемого модуля "аудио-подключение" мастера подключаемых модулей для проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-116">The code is created by modifying the Windows Media Player Plug-in Wizard audio DSP plug-in sample.</span></span>

<span data-ttu-id="c2ef8-117">Образец echo не включен в пакет SDK проигрывателя Windows Media. Это пример, который вы создаете.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-117">The Echo sample is not included with the Windows Media Player SDK; it is a sample that you create.</span></span> <span data-ttu-id="c2ef8-118">Чтобы создать образец Echo, необходимо начать работу с проектом по умолчанию из мастера подключаемых модулей проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-118">To create the Echo sample, you must start with the default project from the Windows Media Player Plug-in Wizard.</span></span> <span data-ttu-id="c2ef8-119">Можно присвоить проекту имя, которое вам нравится. в документации предполагается, что проект называется Echo.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-119">You can name the project whatever you like; this documentation assumes the project is named Echo.</span></span> <span data-ttu-id="c2ef8-120">Дополнительные сведения об использовании мастера см. [в разделе Создание подключаемого модуля DSP](building-a-dsp-plug-in.md).</span><span class="sxs-lookup"><span data-stu-id="c2ef8-120">For details about using the wizard, see [Building a DSP Plug-in](building-a-dsp-plug-in.md).</span></span>

<span data-ttu-id="c2ef8-121">В следующем разделе приведены общие сведения о создании эффекта эха в примере.</span><span class="sxs-lookup"><span data-stu-id="c2ef8-121">The following section provides an overview of how the sample creates an echo effect:</span></span>

-   [<span data-ttu-id="c2ef8-122">Как работает образец Echo</span><span class="sxs-lookup"><span data-stu-id="c2ef8-122">How the Echo Sample Works</span></span>](how-the-echo-sample-works.md)

## <a name="related-topics"></a><span data-ttu-id="c2ef8-123">См. также</span><span class="sxs-lookup"><span data-stu-id="c2ef8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2ef8-124">**Пример эха**</span><span class="sxs-lookup"><span data-stu-id="c2ef8-124">**The Echo Sample**</span></span>](the-echo-sample.md)
</dt> </dl>

 

 




