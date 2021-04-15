---
description: Задает исходный URL-адрес для потока байтов.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Атрибут MF_BYTESTREAM_ORIGIN_NAME (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682878"
---
# <a name="mf_bytestream_origin_name-attribute"></a>\_ \_ Атрибут имени источника MF BYTESTREAM \_

Задает исходный URL-адрес для потока байтов.

## <a name="data-type"></a>Тип данных

Строка расширенных символов

## <a name="remarks"></a>Комментарии

Файловые потоки байтов могут поддерживать этот атрибут. Значение атрибута задается при создании потока байтов. Чтобы получить значение атрибута, запросите объект потока байтов для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                                                    |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты потока байтов](byte-stream-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**Имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




