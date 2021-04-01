---
description: Содержит указатель на интерфейс обратного вызова приложений для модуля записи приемника.
ms.assetid: 22df1fa0-469d-4501-aaf0-a0379b7ed096
title: Атрибут MF_SINK_WRITER_ASYNC_CALLBACK (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f11bed051df9107ca3a2247b6c3d0cf2058224c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817784"
---
# <a name="mf_sink_writer_async_callback-attribute"></a>\_ \_ \_ Атрибут асинхронного \_ обратного вызова для записи MF SINK

Содержит указатель на интерфейс обратного вызова приложения для модуля записи приемника.

## <a name="data-type"></a>Тип данных

**[](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) Имфсинквритеркаллбакк \** _ хранится как _*IUnknown \**_

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Значение этого атрибута является указателем на интерфейс [**имфсинквритеркаллбакк**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwritercallback) приложения.

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

 

 




