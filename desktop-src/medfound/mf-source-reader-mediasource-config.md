---
description: Содержит свойства конфигурации для модуля чтения исходного кода.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: Атрибут MF_SOURCE_READER_MEDIASOURCE_CONFIG (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703475"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a>\_ \_ \_ Атрибут конфигурации медиасаурце для чтения источника MF \_

Содержит свойства конфигурации для [модуля чтения исходного кода](source-reader.md).

## <a name="data-type"></a>Тип данных

**Ипропертисторе \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Значение этого атрибута является указателем на интерфейс **ипропертисторе** хранилища свойств. Этот атрибут можно использовать для передачи свойств конфигурации источнику мультимедиа.

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Модуль чтения исходного кода передает указатель **ипропертисторе** в сопоставитель источника. Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).

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

[Модуль чтения исходного кода](source-reader.md)
</dt> <dt>

[Атрибуты модуля чтения исходного кода](source-reader-attributes.md)
</dt> </dl>

 

 




