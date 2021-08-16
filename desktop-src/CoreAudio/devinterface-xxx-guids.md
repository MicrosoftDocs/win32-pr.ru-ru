---
description: '\_Идентификаторы GUID девинтерфаце XXX используются для представления идентификаторов GUID для интерфейсов устройств.'
ms.assetid: 2503463B-D7C6-4C82-8421-424D79FD1C2A
title: Идентификаторы GUID DEVINTERFACE_XXX (Ммдевицеапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cef6a105ed8e34519a2ca0a06d9d4f43a7aa91495fae9f54eedfa44d79b043c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406797"
---
# <a name="devinterface_xxx-guids"></a>\_Идентификаторы GUID девинтерфаце XXX

\_Идентификаторы GUID девинтерфаце XXX используются для представления идентификаторов GUID для интерфейсов устройств.

<dl> <dt>

<span id="DEVINTERFACE_AUDIO_CAPTURE"></span><span id="devinterface_audio_capture"></span>**ДЕВИНТЕРФАЦЕ \_ \_ запись звука**
</dt> <dd> <dl> <dt>



Указывает строку запроса, используемую для перечисления всех устройств записи звука в системе. Это значение возвращается функцией [**медиадевице:: жетаудиокаптуреселектор**](/uwp/api/windows.media.devices.mediadevice.getaudiocaptureselector).

Передача этого значения в [**активатеаудиоинтерфацеасинк**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) активирует запрошенный интерфейс на устройстве аудиозаписи по умолчанию.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_AUDIO_RENDER"></span><span id="devinterface_audio_render"></span>**\_рендеринг звука \_ девинтерфаце**
</dt> <dd> <dl> <dt>



Указывает строку запроса, используемую для перечисления всех устройств рендеринга звука в системе. Это значение возвращается функцией [**медиадевице:: жетаудиорендерселектор**](/uwp/api/windows.media.devices.mediadevice.getaudiorenderselector).

Передача этого значения в [**активатеаудиоинтерфацеасинк**](/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync) активирует запрошенный интерфейс на устройстве рендеринга звука по умолчанию.


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_INPUT"></span><span id="devinterface_midi_input"></span>**\_Вход девинтерфаце MIDI \_**
</dt> <dd> <dl> <dt>



Указывает строку запроса, используемую для перечисления всех объектов [**мидиинпорт**](/uwp/api/Windows.Devices.Midi.MidiInPort) в системе. Это значение возвращается функцией [**мидиинпорт:: жетдевицеселектор**](/uwp/api/windows.devices.midi.midiinport.getdeviceselector).


</dt> </dl> </dd> <dt>

<span id="DEVINTERFACE_MIDI_OUTPUT"></span><span id="devinterface_midi_output"></span>**\_ \_ выходные данные MIDI девинтерфаце**
</dt> <dd> <dl> <dt>



Указывает строку запроса, используемую для перечисления всех объектов [**мидиаутпорт**](/uwp/api/Windows.Devices.Midi.MidiOutPort) в системе. Это значение возвращается функцией [**мидиаутпорт:: жетдевицеселектор**](/uwp/api/windows.devices.midi.midioutport.getdeviceselector).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Ммдевицеапи. h</dt> </dl> |



 

