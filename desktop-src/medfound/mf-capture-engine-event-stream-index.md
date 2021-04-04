---
description: Определяет, какой поток создал событие записи.
ms.assetid: A15B334A-716A-467E-AEA5-C13710FFE109
title: Атрибут MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8172a79bae2a2eeb529beb0c0ce57273830c1787
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898365"
---
# <a name="mf_capture_engine_event_stream_index-attribute"></a>\_ \_ \_ \_ Атрибут индекса потока событий для обработчика записи MF \_

Определяет, какой поток создал событие записи.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

## <a name="remarks"></a>Комментарии

Этот атрибут отображается для некоторых событий в подсистеме захвата. Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) GetObject для объекта события. Объект события передается в приложение через метод [**имфкаптурингинеоневенткаллбакк:: oneven**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                   |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                         |
| Header<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфкаптурингинеоневенткаллбакк:: oneven**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent)
</dt> </dl>

 

 




