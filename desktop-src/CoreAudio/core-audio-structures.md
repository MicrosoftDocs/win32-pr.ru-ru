---
description: Основные аудио структуры
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Основные аудио структуры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8ea83d0de4c07c1a3d36bab169d5cb581e82cf60e84e308d04dff49af0dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407218"
---
# <a name="core-audio-structures"></a>Основные аудио структуры

в этом разделе описываются структуры, используемые основными api-интерфейсами аудиоподсистемы в Windows Vista и более поздних версиях.



| Структура                                                                     | Описание                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ данные уведомления о звуковом томе \_**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Описывает изменение уровня громкости или выключения звука устройства конечной точки.                                                                                 |
| [**\_ \_ параметры активации DirectX \_ Audio**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Задает параметры инициализации для потока DirectSound.                                                                                                   |
| [**\_Описание ксжакк**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Извлекается с помощью [**иксжаккдескриптион:: жетжаккдескриптион**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); Описывает аудиоразъемы.                                 |
| [**КСЖАКК \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Извлекается с помощью [**IKsJackDescription2:: GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); Описывает аудиоразъемы. <br/>                 |
| [**\_сведения о приемнике ксжакк \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Извлекается с помощью [**иксжакксинкинформатион:: жетжакксинкинформатион**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); Описывает приемник звуковой розетки.<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Содержит идентификатор порта видео.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по программированию](programming-reference.md)
</dt> </dl>

 

 




