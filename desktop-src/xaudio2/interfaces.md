---
title: Интерфейсы XAudio2
description: В этом разделе содержатся сведения об интерфейсах, предоставляемых Microsoft XAudio2 API.
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272823"
---
# <a name="xaudio2-interfaces"></a>Интерфейсы XAudio2

В этом разделе содержатся сведения об интерфейсах, предоставляемых Microsoft XAudio2 API.

## <a name="in-this-section"></a>В этом разделе



| Раздел                                                               | Описание                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 — это интерфейс для объекта [XAudio2](xaudio2-apis-portal.md) , который управляет всеми состояниями обработчика аудио, потоком обработки звука, графом голоса и т. д. <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) представляет базовый интерфейс, от которого наследуются [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice), [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) и [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) . Перечисленные ниже методы являются общими для всех подклассов Voice.<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | Используйте исходный голос для отправки звуковых данных в конвейер обработки XAudio2.<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Субмикс Voice используется в основном для повышения производительности и обработки эффектов. <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | Для представления выходного устройства используется основной голосовой канал.<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | Интерфейс IXAudio2EngineCallback содержит методы, уведомляющие клиента при возникновении определенных событий в подсистеме [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | Интерфейс [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) содержит методы, уведомляющие клиента, когда определенные события происходят в заданном [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice). <br/>                                                                                                                       |
| [**иксапо**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | Интерфейс для объекта обработки звука, который используется в цепочке эффектов XAudio2.<br/>                                                                                                                                                                                                                                        |
| [**иксапопараметерс**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | Необязательный интерфейс, позволяющий КСАПО использовать параметры, относящиеся к определенному результату.<br/>                                                                                                                                                                                                                                                  |
| [**иксапохртфпараметерс**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | Интерфейс, используемый для задания параметров, управляющих применением к звуку функций перенаправления, связанных с HEAD (ХРТФ).<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по программированию](programming-reference.md)
</dt> <dt>

[Справочник по программированию](./programming-reference.md)
</dt> </dl>

 

 
