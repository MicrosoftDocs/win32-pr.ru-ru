---
description: Указывает, ограничивает ли модуль записи приемника скорость входящих данных.
ms.assetid: eb79bda7-ece0-4977-a0f9-d40bd5d220ab
title: Атрибут MF_SINK_WRITER_DISABLE_THROTTLING (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e01c34b51726135516fb6547679db3ba3d48ebfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712858"
---
# <a name="mf_sink_writer_disable_throttling-attribute"></a>Запись \_ приемника MF \_ \_ отключает \_ атрибут регулирования

Указывает, ограничивает ли модуль записи приемника скорость входящих данных.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

По умолчанию метод [**имфсинквритер:: вритесампле**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) модуля записи в приемник ограничивает скорость передачи данных, блокируя вызывающий поток. Это предотвращает слишком быстрое предоставление примеров для приложения. Чтобы отключить это поведение, установите \_ \_ для атрибута регулирования в модуле записи MF Sink \_ \_ **значение true** при создании модуля записи приемника.

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты модуля записи приемника](sink-writer-attributes.md)
</dt> </dl>

 

 




