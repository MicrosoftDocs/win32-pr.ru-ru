---
description: Базовые перечисления аудио
ms.assetid: 7d25be71-ffbe-4e8c-9a45-cdeb35d10292
title: Базовые перечисления аудио
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35c786e1e18f25374a942a4140b67f0992ca7281
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496692"
---
# <a name="core-audio-enumerations"></a><span data-ttu-id="f34aa-103">Базовые перечисления аудио</span><span class="sxs-lookup"><span data-stu-id="f34aa-103">Core Audio Enumerations</span></span>

<span data-ttu-id="f34aa-104">В этом разделе описываются перечисления, используемые основными API-интерфейсами аудиоподсистемы в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="f34aa-104">This section describes the enumerations that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="f34aa-105">Перечисление</span><span class="sxs-lookup"><span data-stu-id="f34aa-105">Enumeration</span></span>                                                                   | <span data-ttu-id="f34aa-106">Описание</span><span class="sxs-lookup"><span data-stu-id="f34aa-106">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f34aa-107">**\_АУДКЛНТ \_ буфферфлагс**</span><span class="sxs-lookup"><span data-stu-id="f34aa-107">**\_AUDCLNT\_BUFFERFLAGS**</span></span>](/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags)                        | <span data-ttu-id="f34aa-108">Флаги состояния для буфера конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="f34aa-108">Status flags for an audio endpoint buffer.</span></span>                                                         |
| [<span data-ttu-id="f34aa-109">**АУДКЛНТ \_ шаремоде**</span><span class="sxs-lookup"><span data-stu-id="f34aa-109">**AUDCLNT\_SHAREMODE**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audclnt_sharemode)                               | <span data-ttu-id="f34aa-110">Режим общего доступа для потока.</span><span class="sxs-lookup"><span data-stu-id="f34aa-110">The sharing mode for a stream.</span></span>                                                                     |
| [<span data-ttu-id="f34aa-111">**АУДКЛНТ \_ стреамоптионс**</span><span class="sxs-lookup"><span data-stu-id="f34aa-111">**AUDCLNT\_STREAMOPTIONS**</span></span>](/windows/desktop/api/audioclient/ne-audioclient-audclnt_streamoptions)                       | <span data-ttu-id="f34aa-112">Определяет значения, описывающие характеристики аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="f34aa-112">Defines values that describe the characteristics of an audio stream.</span></span>                               |
| [<span data-ttu-id="f34aa-113">**Категория ЗВУКового \_ потока \_**</span><span class="sxs-lookup"><span data-stu-id="f34aa-113">**AUDIO\_STREAM\_CATEGORY**</span></span>](/windows/desktop/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category)                      | <span data-ttu-id="f34aa-114">Задает категорию аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="f34aa-114">Specifies the category of an audio stream.</span></span>                                                         |
| [<span data-ttu-id="f34aa-115">**аудиосессионстате**</span><span class="sxs-lookup"><span data-stu-id="f34aa-115">**AudioSessionState**</span></span>](/windows/desktop/api/Audiosessiontypes/ne-audiosessiontypes-audiosessionstate)                                | <span data-ttu-id="f34aa-116">Состояние сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="f34aa-116">The state of an audio session.</span></span>                                                                     |
| [<span data-ttu-id="f34aa-117">**коннектортипе**</span><span class="sxs-lookup"><span data-stu-id="f34aa-117">**ConnectorType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-connectortype)                                        | <span data-ttu-id="f34aa-118">Тип соединителя в топологии устройства.</span><span class="sxs-lookup"><span data-stu-id="f34aa-118">The type of connector in a device topology.</span></span>                                                        |
| [<span data-ttu-id="f34aa-119">**DataFlow**</span><span class="sxs-lookup"><span data-stu-id="f34aa-119">**DataFlow**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-dataflow)                                                  | <span data-ttu-id="f34aa-120">Направление потока данных аудиопотока.</span><span class="sxs-lookup"><span data-stu-id="f34aa-120">The data-flow direction of an audio stream.</span></span>                                                        |
| [<span data-ttu-id="f34aa-121">**едатафлов**</span><span class="sxs-lookup"><span data-stu-id="f34aa-121">**EDataFlow**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-edataflow)                                                | <span data-ttu-id="f34aa-122">Направление передачи звуковых данных между устройством конечной точки аудио и клиентским приложением.</span><span class="sxs-lookup"><span data-stu-id="f34aa-122">The direction in which audio data flows between an audio endpoint device and a client application.</span></span> |
| [<span data-ttu-id="f34aa-123">**ендпоинтформфактор**</span><span class="sxs-lookup"><span data-stu-id="f34aa-123">**EndpointFormFactor**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)                              | <span data-ttu-id="f34aa-124">Общие физические атрибуты устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="f34aa-124">The general physical attributes of an audio endpoint device.</span></span>                                       |
| [<span data-ttu-id="f34aa-125">**ероле**</span><span class="sxs-lookup"><span data-stu-id="f34aa-125">**ERole**</span></span>](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole)                                                        | <span data-ttu-id="f34aa-126">Системная роль устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="f34aa-126">The system role of an audio endpoint device.</span></span>                                                       |
| [<span data-ttu-id="f34aa-127">**\_CONNECTIONTYPE приемника ксжакк \_**</span><span class="sxs-lookup"><span data-stu-id="f34aa-127">**KSJACK\_SINK\_CONNECTIONTYPE**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-ksjack_sink_connectiontype)<br/> | <span data-ttu-id="f34aa-128">Тип соединения.</span><span class="sxs-lookup"><span data-stu-id="f34aa-128">The type of connection.</span></span><br/>                                                                 |
| [<span data-ttu-id="f34aa-129">**парттипе**</span><span class="sxs-lookup"><span data-stu-id="f34aa-129">**PartType**</span></span>](/windows/win32/api/devicetopology/ne-devicetopology-parttype)                                                  | <span data-ttu-id="f34aa-130">Тип части части (соединитель или подразделение) в топологии устройства.</span><span class="sxs-lookup"><span data-stu-id="f34aa-130">The part type of a part (connector or subunit) in a device topology.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="f34aa-131">См. также</span><span class="sxs-lookup"><span data-stu-id="f34aa-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f34aa-132">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="f34aa-132">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




