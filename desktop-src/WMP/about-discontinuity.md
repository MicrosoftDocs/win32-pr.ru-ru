---
title: О прекращении поддержки
description: О прекращении поддержки
ms.assetid: 29210758-a1e6-47f2-9428-38f79623fbca
keywords:
- Подключаемые модули проигрывателя Windows Media, DSP аудиоподсистемы
- подключаемые модули, DSP аудиоподсистемы
- подключаемые модули обработки цифровых сигналов, прекращение звука
- Подключаемые модули DSP, прекращение звука
- подключаемые модули DSP аудио, прекращение поддержки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0448220d4616122b3c99670357bbbd78de11c392
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410666"
---
# <a name="about-discontinuity"></a><span data-ttu-id="ace1e-108">О прекращении поддержки</span><span class="sxs-lookup"><span data-stu-id="ace1e-108">About Discontinuity</span></span>

<span data-ttu-id="ace1e-109">В любой момент времени проигрыватель Windows Media может сообщить о разрыве во входном потоке, вызвав метод **имедиаобжект::D методом непрерывности** .</span><span class="sxs-lookup"><span data-stu-id="ace1e-109">At any time, Windows Media Player can signal a break in the input stream by calling the **IMediaObject::Discontinuity** method.</span></span> <span data-ttu-id="ace1e-110">Это происходит в начале и в конце потока, а также до каждой операции поиска или при прерывании потокового содержимого по какой-либо причине.</span><span class="sxs-lookup"><span data-stu-id="ace1e-110">This occurs routinely at the start and end of a stream, and also prior to each seek operation or when streaming content is interrupted for any reason.</span></span> <span data-ttu-id="ace1e-111">Пример подключаемого модуля DSP, создаваемый мастером подключаемых модулей проигрывателя Windows Media, не требует проблем со прекращениями по следующим причинам:</span><span class="sxs-lookup"><span data-stu-id="ace1e-111">The sample DSP plug-in that the Windows Media Player Plug-in wizard generates does not need to deal with discontinuities for the following reasons:</span></span>

-   <span data-ttu-id="ace1e-112">Примеры PCM являются атомарными, то есть их можно обрабатывать без учета других примеров в потоке.</span><span class="sxs-lookup"><span data-stu-id="ace1e-112">PCM samples are atomic, meaning they can be processed without regard to the other samples in the stream.</span></span> <span data-ttu-id="ace1e-113">Некоторые видеоформаты содержат данные, зависящие от ключевых кадров и сжатых образцов.</span><span class="sxs-lookup"><span data-stu-id="ace1e-113">Some video formats contain data that depends on key frames and compressed samples.</span></span>
-   <span data-ttu-id="ace1e-114">Пример кода написан так, чтобы клиент всегда обрабатывал все выходные данные до того, как подключаемый модуль будет принимать больше входных данных.</span><span class="sxs-lookup"><span data-stu-id="ace1e-114">The sample code is written to always force the client to process all output before the plug-in will accept more input.</span></span>

<span data-ttu-id="ace1e-115">Реализация Имедиаобжект по умолчанию **::D непрерывность** просто возвращает значение S \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ace1e-115">The default implementation of **IMediaObject::Discontinuity** simply returns S\_OK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ace1e-116">См. также</span><span class="sxs-lookup"><span data-stu-id="ace1e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ace1e-117">**Реализация подключаемого модуля DSP аудиоподсистемы**</span><span class="sxs-lookup"><span data-stu-id="ace1e-117">**Implementing an Audio DSP Plug-in**</span></span>](implementing-an-audio-dsp-plug-in.md)
</dt> </dl>

 

 




