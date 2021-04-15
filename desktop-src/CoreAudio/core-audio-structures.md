---
description: Основные аудио структуры
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Основные аудио структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655631"
---
# <a name="core-audio-structures"></a><span data-ttu-id="d1a4c-103">Основные аудио структуры</span><span class="sxs-lookup"><span data-stu-id="d1a4c-103">Core Audio Structures</span></span>

<span data-ttu-id="d1a4c-104">В этом разделе описываются структуры, используемые основными API-интерфейсами аудиоподсистемы в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-104">This section describes the structures that are used by the Core Audio APIs in Windows Vista and later.</span></span>



| <span data-ttu-id="d1a4c-105">Структура</span><span class="sxs-lookup"><span data-stu-id="d1a4c-105">Structure</span></span>                                                                     | <span data-ttu-id="d1a4c-106">Описание</span><span class="sxs-lookup"><span data-stu-id="d1a4c-106">Description</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1a4c-107">**\_ \_ данные уведомления о звуковом томе \_**</span><span class="sxs-lookup"><span data-stu-id="d1a4c-107">**AUDIO\_VOLUME\_NOTIFICATION\_DATA**</span></span>](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | <span data-ttu-id="d1a4c-108">Описывает изменение уровня громкости или выключения звука устройства конечной точки.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-108">Describes a change in the volume level or muting state of an audio endpoint device.</span></span>                                                                                 |
| [<span data-ttu-id="d1a4c-109">**\_ \_ параметры активации DirectX \_ Audio**</span><span class="sxs-lookup"><span data-stu-id="d1a4c-109">**DIRECTX\_AUDIO\_ACTIVATION\_PARAMS**</span></span>](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | <span data-ttu-id="d1a4c-110">Задает параметры инициализации для потока DirectSound.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-110">Specifies the initialization parameters for a DirectSound stream.</span></span>                                                                                                   |
| [<span data-ttu-id="d1a4c-111">**\_Описание ксжакк**</span><span class="sxs-lookup"><span data-stu-id="d1a4c-111">**KSJACK\_DESCRIPTION**</span></span>](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | <span data-ttu-id="d1a4c-112">Извлекается с помощью [**иксжаккдескриптион:: жетжаккдескриптион**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); Описывает аудиоразъемы.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-112">Retrieved through [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describes an audio jack.</span></span>                                 |
| [<span data-ttu-id="d1a4c-113">**КСЖАКК \_ DESCRIPTION2**</span><span class="sxs-lookup"><span data-stu-id="d1a4c-113">**KSJACK\_DESCRIPTION2**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | <span data-ttu-id="d1a4c-114">Извлекается с помощью [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); Описывает аудиоразъемы.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-114">Retrieved through [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describes an audio jack.</span></span> <br/>                 |
| [<span data-ttu-id="d1a4c-115">**\_сведения о приемнике ксжакк \_**</span><span class="sxs-lookup"><span data-stu-id="d1a4c-115">**KSJACK\_SINK\_INFORMATION**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | <span data-ttu-id="d1a4c-116">Извлекается с помощью [**иксжакксинкинформатион:: жетжакксинкинформатион**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); Описывает приемник звуковой розетки.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-116">Retrieved through [**IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describes an audio jack sink.</span></span><br/> |
| [<span data-ttu-id="d1a4c-117">**LUID**</span><span class="sxs-lookup"><span data-stu-id="d1a4c-117">**LUID**</span></span>](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | <span data-ttu-id="d1a4c-118">Содержит идентификатор порта видео.</span><span class="sxs-lookup"><span data-stu-id="d1a4c-118">Stores the video port identifier.</span></span><br/>                                                                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="d1a4c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="d1a4c-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1a4c-120">Справочник по программированию</span><span class="sxs-lookup"><span data-stu-id="d1a4c-120">Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 




