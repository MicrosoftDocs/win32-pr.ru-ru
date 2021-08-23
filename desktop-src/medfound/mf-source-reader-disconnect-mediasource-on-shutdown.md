---
description: Указывает, завершает ли модуль чтения источника носитель.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Атрибут MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323340a0b95fd6f52d4ac7e8db2e9ff53bf70edb30442369f1ffd8f2f2c55fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663894"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>\_ \_ Агент чтения источника MF \_ Отключить \_ медиасаурце \_ при \_ завершении работы

Указывает, завершает ли [модуль чтения источника](source-reader.md) носитель.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Этот атрибут применяется только в том случае, если приложение создает модуль чтения исходного кода из существующего объекта источника мультимедиа либо путем вызова [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) , либо путем вызова [**Имфреадвритеклассфактори:: креатеинстанцефромобжект**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

По умолчанию, когда приложение освобождает модуль чтения исходного кода, модуль чтения источника завершает работу источника мультимедиа, вызывая [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике мультимедиа. На этом этапе приложение больше не может использовать источник мультимедиа.

Однако, если \_ \_ атрибуту "чтение источника MF \_ Отключить \_ медиасаурце \_ On Shutdown" \_ присвоено **значение true**, модуль чтения исходного кода не завершает работу источника мультимедиа. Это означает, что приложение по-прежнему может использовать источник мультимедиа после освобождения приложением модуля чтения исходного кода. Это также означает, что приложение отвечает за вызов [**имфмедиасаурце:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) в источнике мультимедиа.

Если приложение создает модуль чтения исходного кода из URL-адреса или потока байтов, модуль чтения исходного кода всегда завершает работу источника мультимедиа. \_ \_ \_ \_ \_ \_ В этом случае в этом случае пропускается атрибут MF Source DataReader Disconnect медиасаурце on Shutdown.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Модуль чтения исходного кода](source-reader.md)
</dt> <dt>

[Атрибуты модуля чтения исходного кода](source-reader-attributes.md)
</dt> </dl>

 

 




