---
description: 'Содержит URL-адрес файла ИФО (сведения о DVD-диске), заданный HTTP-сервером в заголовке HTTP &\# 0034; Pragma: ifoFileURI.dlna.org&\# 0034;.'
ms.assetid: 007e0f4d-fb37-4dec-96a7-311df567eb04
title: Атрибут MF_BYTESTREAM_IFO_FILE_URI (Мфобжектс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab4349f3319a875f428921b0a99aefa61e49340c240a87260c1132abcc7c45f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723474"
---
# <a name="mf_bytestream_ifo_file_uri-attribute"></a>\_ \_ \_ Атрибут URI файла ИФО MF BYTESTREAM \_

Содержит URL-адрес файла ИФО (сведения о DVD-диске), заданный HTTP-сервером в заголовке HTTP, "pragma: ifoFileURI.dlna.org".

## <a name="data-type"></a>Тип данных

**LPWSTR**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Применяется к

[**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)

## <a name="remarks"></a>Remarks

Поток байтов HTTP выполняет поиск строки "ifoFileURI.dlna.org" в заголовке HTTP. Если строка найдена, она копируется в этот атрибут потока байтов.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                                           |
| Заголовок<br/>                   | <dl> <dt>Мфобжектс. h (включение Мфидл. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты потока байтов](byte-stream-attributes.md)
</dt> <dt>

[**имфбитестреам**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




