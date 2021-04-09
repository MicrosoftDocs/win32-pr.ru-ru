---
title: Справочник по Waveform Audio
description: В этом разделе перечислены функции, структуры и сообщения, связанные с волновой звукозаписью, которые задокументированы в справочнике по мультимедиа. Эти элементы группируются следующим образом.
ms.assetid: 723953f7-b38e-4f24-8d54-9849e013011d
keywords:
- Мультимедиа Windows, Справочник по волнам аудио
- мультимедиа, Справочник по волнам аудио
- мультимедиа аудио, Справочник по волнам
- аудио, Справочник по волнам
- Мультимедиа Windows, звуковая волна
- мультимедиа, волна аудио
- мультимедийные аудио, волна
- аудио, волна
- звуковая волна, справочная информация
- Справочник по волнам звукозаписи, сведения
- Справочник по вавефоре Audio, о программе
- Справочник по волнам аудио, дополнительные устройства
- Справочник по вавефоре аудио, дополнительным устройствам
- Звуковая ссылка аудио, воспроизведение
- Справочник по вавефоре аудио, воспроизведению
- Звуковая ссылка аудио, ошибки
- Справочник по вавефоре аудио, ошибкам
- Справочник по волнам аудио, открытие
- Справочник по вавефоре Audio, открытие
- Справочник по волнам аудио, закрытие
- Справочник по вавефоре Audio, закрытие
- Звуковая ссылка звуковой волны, шаг
- Справочник по вавефоре Audio, тон
- Справочник по волнам аудио, том
- Справочник по вавефоре Audio, Volume
- Справочник по волнам аудио, сообщения
- Справочник по вавефоре Audio, messages
- Справочник по волнам аудио, Текущая заданная позицией
- Справочник по вавефоре аудио, текущему положению
- Справочник по волнам аудио, запись
- Справочник по вавефоре аудио, записи
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c74b37984b2d3fab5dad1ea0df4f1f62dfa1855e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104069914"
---
# <a name="waveform-audio-reference"></a>Справочник по Waveform Audio

В этом разделе перечислены функции, структуры и сообщения, связанные с волновой звукозаписью, которые задокументированы в [справочнике по мультимедиа](multimedia-reference.md). Эти элементы группируются следующим образом.

## <a name="auxiliary-devices"></a>Вспомогательные устройства

-   [**аукскапс**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps)
-   [**ауксжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps)
-   [**ауксжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs)
-   [**ауксжетволуме**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetvolume)
-   [**ауксаутмессаже**](/windows/win32/api/mmeapi/nf-mmeapi-auxoutmessage)
-   [**аукссетволуме**](/windows/win32/api/mmeapi/nf-mmeapi-auxsetvolume)

## <a name="easy-playback"></a>Удобное воспроизведение

-   [**PlaySound**](/previous-versions//dd743680(v=vs.85))
-   [**сндплайсаунд**](/previous-versions//dd798676(v=vs.85))

## <a name="errors"></a>ошибки

-   [**вавеинжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)
-   [**вавеаутжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext)

## <a name="opening-and-closing"></a>Открытие и закрытие

-   [**пкмвавеформат**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat)
-   [**MM \_ , \_ закрытие WIM**](mm-wim-close.md)
-   [**ММ — \_ открытый WIM-файл \_**](mm-wim-open.md)
-   [**вом мм, \_ \_ закрытие**](mm-wom-close.md)
-   [**\_вом мм \_ Open**](mm-wom-open.md)
-   [**вавеформат**](/windows/win32/api/mmreg/ns-mmreg-waveformat)
-   [**вавеформатекс**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex)
-   [**вавеинклосе**](/windows/win32/api/mmeapi/nf-mmeapi-waveinclose)
-   [**вавеинпрок**](/previous-versions//dd743849(v=vs.85))
-   [**вавеинопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveinopen)
-   [**вавеаутклосе**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutclose)
-   [**вавеаутпрок**](/previous-versions//dd743869(v=vs.85))
-   [**вавеаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutopen)
-   [**\_закрытие WIM**](wim-close.md)
-   [**\_открытый WIM**](wim-open.md)
-   [**ВОМ \_ Закрыть**](wom-close.md)
-   [**ВОМ \_ Открыть**](wom-open.md)

## <a name="pitch"></a>Высота тона

-   [**вавеаутжетпитч**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetpitch)
-   [**вавеаутсетпитч**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetpitch)

## <a name="playback-rate"></a>Скорость воспроизведения

-   [**вавеаутжетплайбаккрате**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetplaybackrate)
-   [**вавеаутсетплайбаккрате**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetplaybackrate)

## <a name="playback-progress"></a>Ход воспроизведения

-   [**MM \_ вом \_ done**](mm-wom-done.md)
-   [**вавеаутбреаклуп**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutbreakloop)
-   [**вавеаутпаусе**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutpause)
-   [**вавеаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset)
-   [**вавеаутрестарт**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutrestart)
-   [**ВОМ \_ Готово**](wom-done.md)

## <a name="playing"></a>Воспроизведение

-   [**MM \_ вом \_ done**](mm-wom-done.md)
-   [**вавехдр**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)
-   [**вавеаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutprepareheader)
-   [**вавеаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader)
-   [**вавеаутврите**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutwrite)
-   [**ВОМ \_ Готово**](wom-done.md)

## <a name="querying-a-device"></a>Запрос устройства

-   [**вавеинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-waveincaps)
-   [**вавеинжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetdevcaps)
-   [**вавеинжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)
-   [**вавеауткапс**](/windows/win32/api/mmeapi/ns-mmeapi-waveoutcaps)
-   [**вавеаутжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetdevcaps)
-   [**вавеаутжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs)

## <a name="recording"></a>Запись

-   [**MM \_ . \_ данные WIM**](mm-wim-data.md)
-   [**вавеинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinaddbuffer)
-   [**вавеинпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinprepareheader)
-   [**вавеинресет**](/windows/win32/api/mmeapi/nf-mmeapi-waveinreset)
-   [**вавеинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstart)
-   [**вавеинстоп**](/windows/win32/api/mmeapi/nf-mmeapi-waveinstop)
-   [**вавеинунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-waveinunprepareheader)
-   [**\_данные WIM**](wim-data.md)

## <a name="retrieving-device-identifiers"></a>Получение идентификаторов устройств

-   [**вавеинжетид**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetid)
-   [**вавеаутжетид**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetid)

## <a name="retrieving-the-current-position"></a>Получение текущей должности

-   [**вавеинжетпоситион**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetposition)
-   [**вавеаутжетпоситион**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetposition)

## <a name="sending-custom-messages"></a>Отправка пользовательских сообщений

-   [**вавеинмессаже**](/windows/win32/api/mmeapi/nf-mmeapi-waveinmessage)
-   [**вавеаутмессаже**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutmessage)

## <a name="volume"></a>Том

-   [**вавеаутжетволуме**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetvolume)
-   [**вавеаутсетволуме**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutsetvolume)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Звуковая волна](waveform-audio.md)
</dt> </dl>

 

 