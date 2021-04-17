---
title: Формат согласования
description: Формат согласования
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Подключаемые модули проигрывателя Windows Media, формат согласования
- подключаемые модули, формат согласования
- подключаемые модули обработки цифровых сигналов, согласование формата
- Подключаемые модули DSP, форматирование согласования
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105691330"
---
# <a name="format-negotiation"></a><span data-ttu-id="2cdab-107">Формат согласования</span><span class="sxs-lookup"><span data-stu-id="2cdab-107">Format Negotiation</span></span>

<span data-ttu-id="2cdab-108">Для проигрывателя Windows Media и подключаемого модуля DSP для совместного использования данных обе программы должны согласовать формат обрабатываемых данных.</span><span class="sxs-lookup"><span data-stu-id="2cdab-108">For Windows Media Player and a DSP plug-in to share data, both programs must agree on the format of the data they are processing.</span></span> <span data-ttu-id="2cdab-109">Подключаемый модуль DSP реализует методы, которые вызываются проигрывателем для определения форматов, поддерживаемых подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="2cdab-109">The DSP plug-in implements methods that the Player calls to determine which formats the plug-in supports.</span></span> <span data-ttu-id="2cdab-110">Подключаемый модуль также реализует методы, которые вызываются проигрывателем для задания текущего формата.</span><span class="sxs-lookup"><span data-stu-id="2cdab-110">The plug-in also implements methods that the Player calls to set the current format.</span></span>

<span data-ttu-id="2cdab-111">Если подключаемый модуль выступает в роли объекта мультимедиа Дирексткс (DMO), проигрыватель Windows Media обнаруживает и устанавливает форматы мультимедиа путем вызова методов интерфейса **имедиаобжект** .</span><span class="sxs-lookup"><span data-stu-id="2cdab-111">If the plug-in is acting as a DirextX Media Object (DMO), Windows Media Player discovers and sets media formats by calling methods of the **IMediaObject** interface.</span></span> <span data-ttu-id="2cdab-112">Например, проигрыватель вызывает **имедиаобжект:: жетинпуттипе** подключаемого модуля, чтобы получить список всех входных форматов, поддерживаемых подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="2cdab-112">For example, the Player calls the plug-in's **IMediaObject::GetInputType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="2cdab-113">Подключаемые модули DMO используют структуру **\_ \_ типа мультимедиа DMO** для организации сведений, указывающих формат мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="2cdab-113">DMO plug-ins use the **DMO\_MEDIA\_TYPE** structure to organize the information that specifies a media format.</span></span> <span data-ttu-id="2cdab-114">Дополнительные сведения о том, как подключаемые модули DMO и формат согласования с проигрывателем, см. в разделе [About имедиаобжект](about-imediaobject.md).</span><span class="sxs-lookup"><span data-stu-id="2cdab-114">For more information about how DMO plug-ins and the Player negotiate format, see [About IMediaObject](about-imediaobject.md).</span></span>

<span data-ttu-id="2cdab-115">Если подключаемый модуль выступает в качестве Media Foundation преобразования (MFT), проигрыватель Windows Media обнаруживает и устанавливает форматы мультимедиа путем вызова методов интерфейса **имфтрансформ** .</span><span class="sxs-lookup"><span data-stu-id="2cdab-115">If the plug-in is acting as a Media Foundation Transform (MFT), Windows Media Player discovers and sets media formats by calling methods of the **IMFTransform** interface.</span></span> <span data-ttu-id="2cdab-116">Например, проигрыватель вызывает **имфтрансформ:: жетинпутаваилаблетипе** подключаемого модуля, чтобы получить список всех входных форматов, поддерживаемых подключаемым модулем.</span><span class="sxs-lookup"><span data-stu-id="2cdab-116">For example, the Player calls the plug-in's **IMFTransform::GetInputAvailableType** repeatedly to get a list of all input formats supported by the plug-in.</span></span> <span data-ttu-id="2cdab-117">Подключаемые модули MFT и проигрыватель используют интерфейс **имфмедиатипе** для Организации и обмена сведениями о формате.</span><span class="sxs-lookup"><span data-stu-id="2cdab-117">MFT plug-ins and the Player use the **IMFMediaType** interface to organize and exchange format information.</span></span>

<span data-ttu-id="2cdab-118">Проигрыватель Windows Media будет использовать подключаемый модуль DSP для аудио, только если подключаемый модуль поддерживает ту же глубину, что и воспроизводимый цифровой звук.</span><span class="sxs-lookup"><span data-stu-id="2cdab-118">Windows Media Player will use an audio DSP plug-in only if the plug-in supports the same bit depth as the digital audio being played.</span></span> <span data-ttu-id="2cdab-119">Например, если цифровой звук имеет 20-битное значение, подключаемый модуль должен быть написан для обработки 20-разрядного звука.</span><span class="sxs-lookup"><span data-stu-id="2cdab-119">For instance, if the digital audio is 20-bit, the plug-in must be written to process 20-bit audio.</span></span> <span data-ttu-id="2cdab-120">Подключаемые модули DSP для аудио компакт-дисков должны поддерживать 20-разрядную обработку.</span><span class="sxs-lookup"><span data-stu-id="2cdab-120">For CD audio, DSP plug-ins must support 20-bit processing.</span></span>

<span data-ttu-id="2cdab-121">Во время согласования формата многоканального содержимого на компьютере, настроенном для использования со стерео динамиками, проигрыватель Windows Media сначала пытается подключиться к подключаемому модулю DSP аудиоподсистемы, используя существующий формат входных и выходных данных, вызвав **имедиаобжект:: сетинпуттипе** и **Имедиаобжект:: сетаутпуттипе**.</span><span class="sxs-lookup"><span data-stu-id="2cdab-121">During format negotiation of multi-channel content on a computer configured for use with stereo speakers, Windows Media Player first attempts to connect to an audio DSP plug-in using the existing input and output format by calling **IMediaObject::SetInputType** and **IMediaObject::SetOutputType**.</span></span> <span data-ttu-id="2cdab-122">После первоначального согласования проигрыватель перечисляет форматы, поддерживаемые подключаемым модулем, и пытается согласовать оптимальное сочетание форматов для проигрывателя и подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="2cdab-122">Once this initial negotiation occurs, the Player then enumerates the formats the plug-in supports and attempts to negotiate the best format combination for the Player and the plug-in.</span></span> <span data-ttu-id="2cdab-123">Если подключаемый модуль принимает стерео аудио (определяется структурой **вавеформатекс** ) в качестве входного формата во время первоначального согласования, а затем принимает только многоканальный звук (определенный структурой **Вавеформатекстенсибле** ), проигрыватель предоставит многоканальный звук в качестве входного формата для подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="2cdab-123">If the plug-in accepts stereo audio (defined by a **WAVEFORMATEX** structure) as the input format during the initial negotiation, and then subsequently accepts only multi-channel audio (defined by a **WAVEFORMATEXTENSIBLE** structure), the Player will provide multi-channel audio as the input format to the plug-in.</span></span> <span data-ttu-id="2cdab-124">Такое поведение во время согласования формата доступно для использования в операционной системе Microsoft Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2cdab-124">This behavior during format negotiation is available for use in the Microsoft Windows XP operating system.</span></span> <span data-ttu-id="2cdab-125">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="2cdab-125">It may be altered or unavailable in subsequent versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cdab-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2cdab-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cdab-127">**Обзор подключаемого модуля DSP**</span><span class="sxs-lookup"><span data-stu-id="2cdab-127">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




