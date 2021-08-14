---
description: Позволяет модулю чтения источника или записи приемника использовать Media Foundation преобразования на основе оборудования (МФТС).
ms.assetid: 03f2fa76-b828-40b1-929d-60e7d5ab49bb
title: Атрибут MF_READWRITE_ENABLE_HARDWARE_TRANSFORMS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f851ba188f8a2cc42140b799e23156cdc8e5c06bb474deb16debf508c173a908
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059537"
---
# <a name="mf_readwrite_enable_hardware_transforms-attribute"></a>\_Атрибут MF ReadWrite \_ включить \_ аппаратные \_ преобразования

Позволяет модулю чтения источника или записи приемника использовать Media Foundation преобразования на основе оборудования (МФТС).

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

По умолчанию модуль чтения источника и модуль записи приемника не используют аппаратные декодеры или кодировщики. Чтобы включить использование оборудования МФТС, установите для этого атрибута значение **true** при создании модуля чтения исходного кода или модуля записи приемника.

Используйте этот атрибут со следующими функциями:

-   [**мфкреатесаурцереадерфромбитестреам**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**мфкреатесаурцереадерфроммедиасаурце**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**мфкреатесаурцереадерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)
-   [**мфкреатесинквритерфроммедиасинк**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**мфкреатесинквритерфромурл**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Существует одно исключение, связанное с поведением по умолчанию. Средство чтения исходного кода и модуль записи приемника автоматически используют МФТС, которые зарегистрированы локально в процессе вызывающего. Чтобы зарегистрировать таблицу MFT локально, вызовите [**мфтрегистерлокал**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) или [**мфтрегистерлокалбиклсид**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid). МФТС оборудования, зарегистрированные локально, используются, даже если не установлен атрибут **\_ Enable ReadWrite ( \_ включить \_ аппаратное \_ Преобразование** ).

Этот атрибут не влияет на декодирование видео с аппаратным ускорением, которое использует ускорение видео DirectX (ДКСВА). Чтобы включить декодирование ДКСВА в модуле чтения исходного кода, установите [атрибут \_ \_ \_ \_ диспетчера D3D источника MF](mf-source-reader-d3d-manager.md) .

Если этот атрибут имеет **значение true**, не устанавливайте [атрибут \_ \_ \_ преобразователей MF ReadWrite Disable](mf-readwrite-disable-converters.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты модуля записи приемника](sink-writer-attributes.md)
</dt> <dt>

[Атрибуты модуля чтения исходного кода](source-reader-attributes.md)
</dt> </dl>

 

 




