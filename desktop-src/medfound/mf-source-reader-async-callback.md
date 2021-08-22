---
description: Содержит указатель на интерфейс обратного вызова приложений для модуля чтения исходного кода.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: Атрибут MF_SOURCE_READER_ASYNC_CALLBACK (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4dedfcdcb426eb62a0ae14bec3fd75232c9a871d0bad10194860305c687fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605163"
---
# <a name="mf_source_reader_async_callback-attribute"></a>\_ \_ \_ Атрибут асинхронного \_ обратного вызова для чтения источника MF

Содержит указатель на интерфейс обратного вызова приложения для [модуля чтения исходного кода](source-reader.md).

## <a name="data-type"></a>Тип данных

**Имфсаурцереадеркаллбакк \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Remarks

Значение этого атрибута является указателем на интерфейс [**имфсаурцереадеркаллбакк**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) приложения.

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

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

 

 




