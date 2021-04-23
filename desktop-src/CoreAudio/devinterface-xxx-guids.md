---
description: '\_Идентификаторы GUID девинтерфаце XXX используются для представления идентификаторов GUID для интерфейсов устройств.'
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: Идентификаторы GUID DEVINTERFACE_XXX (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 796f113d26ebc351a4d576ed76485d24d89fdb04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648864"
---
# <a name="devinterface_xxx-guids"></a><span data-ttu-id="593e7-103">\_Идентификаторы GUID девинтерфаце XXX</span><span class="sxs-lookup"><span data-stu-id="593e7-103">DEVINTERFACE\_XXX GUIDs</span></span>

<span data-ttu-id="593e7-104">\_Идентификаторы GUID девинтерфаце XXX используются для представления идентификаторов GUID для интерфейсов устройств.</span><span class="sxs-lookup"><span data-stu-id="593e7-104">The DEVINTERFACE\_XXX GUIDs are used to represent the GUIDs for device interfaces.</span></span>

<dl> <dt>

<span data-ttu-id="593e7-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**ДЕВИНТЕРФАЦЕ \_ \_ запись звука**</span><span class="sxs-lookup"><span data-stu-id="593e7-105"><span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**DEVINTERFACE\_AUDIO\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="593e7-106">Указывает строку запроса, используемую для перечисления всех устройств записи звука в системе.</span><span class="sxs-lookup"><span data-stu-id="593e7-106">Specifies the query string used to enumerate all audio capture devices on the system.</span></span> <span data-ttu-id="593e7-107">Это значение возвращается функцией [**медиадевице:: жетаудиокаптуреселектор**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span><span class="sxs-lookup"><span data-stu-id="593e7-107">This value is returned by [**MediaDevice::GetAudioCaptureSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).</span></span>

<span data-ttu-id="593e7-108">Передача этого значения в [**активатеаудиоинтерфацеасинк**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) активирует запрошенный интерфейс на устройстве аудиозаписи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="593e7-108">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio capture device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="593e7-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_рендеринг звука \_ девинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="593e7-109"><span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**DEVINTERFACE\_AUDIO\_RENDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="593e7-110">Указывает строку запроса, используемую для перечисления всех устройств рендеринга звука в системе.</span><span class="sxs-lookup"><span data-stu-id="593e7-110">Specifies the query string used to enumerate all audio render devices on the system.</span></span> <span data-ttu-id="593e7-111">Это значение возвращается функцией [**медиадевице:: жетаудиорендерселектор**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span><span class="sxs-lookup"><span data-stu-id="593e7-111">This value is returned by [**MediaDevice::GetAudioRenderSelector**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).</span></span>

<span data-ttu-id="593e7-112">Передача этого значения в [**активатеаудиоинтерфацеасинк**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) активирует запрошенный интерфейс на устройстве рендеринга звука по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="593e7-112">Passing this value to [**ActivateAudioInterfaceAsync**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) activates the requested interface on the default audio render device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="593e7-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_Вход девинтерфаце MIDI \_**</span><span class="sxs-lookup"><span data-stu-id="593e7-113"><span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**DEVINTERFACE\_MIDI\_INPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="593e7-114">Указывает строку запроса, используемую для перечисления всех объектов [**мидиинпорт**](/uwp/api/Windows.Devices.Midi.MidiInPort) в системе.</span><span class="sxs-lookup"><span data-stu-id="593e7-114">Specifies the query string used to enumerate all [**MidiInPort**](/uwp/api/Windows.Devices.Midi.MidiInPort) objects on the system.</span></span> <span data-ttu-id="593e7-115">Это значение возвращается функцией [**мидиинпорт:: жетдевицеселектор**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="593e7-115">This value is returned by [**MidiInPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="593e7-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_ \_ выходные данные MIDI девинтерфаце**</span><span class="sxs-lookup"><span data-stu-id="593e7-116"><span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**DEVINTERFACE\_MIDI\_OUTPUT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="593e7-117">Указывает строку запроса, используемую для перечисления всех объектов [**мидиаутпорт**](/uwp/api/Windows.Devices.Midi.MidiOutPort) в системе.</span><span class="sxs-lookup"><span data-stu-id="593e7-117">Specifies the query string used to enumerate all [**MidiOutPort**](/uwp/api/Windows.Devices.Midi.MidiOutPort) objects on the system.</span></span> <span data-ttu-id="593e7-118">Это значение возвращается функцией [**мидиаутпорт:: жетдевицеселектор**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span><span class="sxs-lookup"><span data-stu-id="593e7-118">This value is returned by [**MidiOutPort::GetDeviceSelector**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="593e7-119">Требования</span><span class="sxs-lookup"><span data-stu-id="593e7-119">Requirements</span></span>



| <span data-ttu-id="593e7-120">Требование</span><span class="sxs-lookup"><span data-stu-id="593e7-120">Requirement</span></span> | <span data-ttu-id="593e7-121">Значение</span><span class="sxs-lookup"><span data-stu-id="593e7-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="593e7-122">Header</span><span class="sxs-lookup"><span data-stu-id="593e7-122">Header</span></span><br/> | <dl> <span data-ttu-id="593e7-123"><dt>Ммдевицеапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="593e7-123"><dt>Mmdeviceapi.h</dt></span></span> </dl> |



 

