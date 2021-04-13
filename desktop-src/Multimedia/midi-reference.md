---
title: Справочник по MIDI
description: Справочник по MIDI
ms.assetid: 6229a4a7-be42-4e2a-af9d-695c4759a4ef
keywords:
- Мультимедиа Windows, цифровой интерфейс музыкальных инструментов (MIDI)
- мультимедиа, цифровой интерфейс музыкальных инструментов (MIDI)
- мультимедийный звук, цифровой интерфейс музыкальных инструментов (MIDI)
- аудио, цифровой интерфейс музыкальных инструментов (MIDI)
- Windows мультимедиа, Справочник MIDI
- мультимедиа, Справочник MIDI
- мультимедиа аудио, Справочник MIDI
- аудио, Справочник MIDI
- Цифровой интерфейс MIDI, справочные материалы
- MIDI (цифровой интерфейс музыкального инструмента), Справочник
- Справочник по MIDI, сведения
- Справочник по MIDI, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c21542867faf1e09d68dc4fc81a50d25f56b5c5e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104412908"
---
# <a name="midi-reference"></a>Справочник по MIDI

В этом разделе описываются функции, макросы, сообщения и структуры, связанные с цифровым интерфейсом MIDI. Эти элементы группируются следующим образом.

## <a name="allocating-and-managing-buffers"></a>Выделение буферов и управление ими

-   [**мидихдр**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr)
-   [**мидиинаддбуффер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinaddbuffer)
-   [**мидиинпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinprepareheader)
-   [**мидиинунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midiinunprepareheader)
-   [**мидиаутпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutprepareheader)
-   [**мидиаутунпрепарехеадер**](/windows/win32/api/mmeapi/nf-mmeapi-midioutunprepareheader)

## <a name="callback-functions"></a>Функции обратного вызова

-   [**мидиинпрок**](/previous-versions//dd798460(v=vs.85))
-   [**мидиаутпрок**](/previous-versions//dd798478(v=vs.85))

## <a name="device-capabilities"></a>Возможности устройства

-   [**мидиинкапс**](/windows/win32/api/mmeapi/ns-mmeapi-midiincaps)
-   [**мидиинжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetdevcaps)
-   [**мидиинжетид**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetid)
-   [**мидиинжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-midiingetnumdevs)
-   [**мидиауткапс**](/windows/win32/api/mmeapi/ns-mmeapi-midioutcaps)
-   [**мидиаутжетдевкапс**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetdevcaps)
-   [**мидиаутжетид**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetid)
-   [**мидиаутжетнумдевс**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetnumdevs)
-   [**мидистрмбуффвер**](/windows/win32/api/mmeapi/ns-mmeapi-midistrmbuffver)

## <a name="error-processing"></a>Обработка ошибок

-   [**мидиинжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-midiingeterrortext)
-   [**мидиаутжетеррортекст**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgeterrortext)
-   [**\_Ошибка MIM**](mim-error.md)
-   [**\_ЛОНЖЕРРОР MIM**](mim-longerror.md)
-   [**MM \_ , \_ Ошибка MIM**](mm-mim-error.md)
-   [**MM \_ MIM \_ лонжеррор**](mm-mim-longerror.md)

## <a name="managing-midi-streams"></a>Управление потоками MIDI

-   [**мидистреамклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamclose)
-   [**мидистреамопен**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamopen)
-   [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**мидистреампаусе**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**мидистреампоситион**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition)
-   [**мидистреампроперти**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamproperty)
-   [**мидистреамрестарт**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**мидистреамстоп**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)

## <a name="opening-and-closing-devices"></a>Открытие и закрытие устройств

-   [**мидиинклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midiinclose)
-   [**мидиинопен**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen)
-   [**мидиаутклосе**](/windows/win32/api/mmeapi/nf-mmeapi-midioutclose)
-   [**мидиаутопен**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen)
-   [**\_закрытие MIM**](mim-close.md)
-   [**\_Запуск MIM**](mim-open.md)
-   [**MM \_ MIM, \_ закрытие**](mm-mim-close.md)
-   [**MM \_ MIM \_ Open**](mm-mim-open.md)
-   [**\_закрытие mm MOM \_**](mm-mom-close.md)
-   [**\_ \_ открытая MOM mm**](mm-mom-open.md)
-   [**\_закрытие MOM**](mom-close.md)
-   [**диспетчер MOM \_ открыт**](mom-open.md)

## <a name="output-devices"></a>Устройства вывода

-   [кэйаррай](keyarray.md)
-   [**мидиауткачедрумпатчес**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachedrumpatches)
-   [**мидиауткачепатчес**](/windows/win32/api/mmeapi/nf-mmeapi-midioutcachepatches)
-   [**мидиаутжетволуме**](/windows/win32/api/mmeapi/nf-mmeapi-midioutgetvolume)
-   [**мидиаутсетволуме**](/windows/win32/api/mmeapi/nf-mmeapi-midioutsetvolume)
-   [патчаррай](patcharray.md)

## <a name="playing-a-message-or-messages"></a>Воспроизведение сообщения или сообщений

-   [**МЕВТ \_ евентпарм**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventparm)
-   [**МЕВТ \_ EVENTTYPE**](/windows/win32/api/mmeapi/nf-mmeapi-mevt_eventtype)
-   [**мидиевент**](/windows/win32/api/mmeapi/ns-mmeapi-midievent)
-   [**мидиаутлонгмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutlongmsg)
-   [**мидиаутресет**](/windows/win32/api/mmeapi/nf-mmeapi-midioutreset)
-   [**мидиаутшортмсг**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg)
-   [**мидистреамаут**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamout)
-   [**мидистреампаусе**](/windows/win32/api/mmeapi/nf-mmeapi-midistreampause)
-   [**мидистреамрестарт**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamrestart)
-   [**мидистреамстоп**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamstop)
-   [**MM, \_ MOM \_**](mm-mom-done.md)
-   [**MM \_ MOM \_ поситионкб**](mm-mom-positioncb.md)
-   [**MOM \_**](mom-done.md)
-   [**MOM \_ поситионкб**](mom-positioncb.md)

## <a name="recording"></a>Запись

-   [**мидиконнект**](/windows/win32/api/mmeapi/nf-mmeapi-midiconnect)
-   [**мидидисконнект**](/windows/win32/api/mmeapi/nf-mmeapi-mididisconnect)
-   [**мидиинресет**](/windows/win32/api/mmeapi/nf-mmeapi-midiinreset)
-   [**мидиинстарт**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstart)
-   [**мидиинстоп**](/windows/win32/api/mmeapi/nf-mmeapi-midiinstop)
-   [**мидипроптемпо**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptempo)
-   [**мидипроптимедив**](/windows/win32/api/mmeapi/ns-mmeapi-midiproptimediv)
-   [**\_данные MIM**](mim-data.md)
-   [**\_ЛОНГДАТА MIM**](mim-longdata.md)
-   [**\_MOREDATA MIM**](mim-moredata.md)
-   [**MM \_ MIM \_ Data**](mm-mim-data.md)
-   [**MM \_ MIM \_ MOREDATA**](mm-mim-moredata.md)
-   [**MM \_ MIM \_ лонгдата**](mm-mim-longdata.md)

## <a name="sending-messages-to-devices"></a>Отправка сообщений на устройства

-   [**мидиинмессаже**](/windows/win32/api/mmeapi/nf-mmeapi-midiinmessage)
-   [**мидиаутмессаже**](/windows/win32/api/mmeapi/nf-mmeapi-midioutmessage)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Цифровой интерфейс музыкальных инструментов (MIDI)](musical-instrument-digital-interface--midi.md)
</dt> </dl>

 

 