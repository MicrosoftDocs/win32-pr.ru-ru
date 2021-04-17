---
description: Возвращает характеристики источника мультимедиа от модуля чтения исходного кода.
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: Атрибут MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de4d1ed026f7b74f290446af74a6cf9947612617
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351712"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>\_ \_ \_ Атрибут характеристик медиасаурце для СЧИТЫВАНИя источника MF \_

Возвращает характеристики источника мультимедиа от [модуля чтения исходного кода](source-reader.md).

## <a name="data-type"></a>Тип данных

**UINT32**

Значение представляет собой побитовое **или** для флагов перечисления [**мфмедиасаурце \_ характеристик**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics) .

## <a name="remarks"></a>Комментарии

Чтобы получить этот атрибут, вызовите метод [**имфсаурцереадер:: жетпресентатионаттрибуте**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) в модуле чтения исходного кода. Задайте для параметра *двстреаминдекс* значение **MF \_ \_ Reader source \_ медиасаурце** , а параметр *guidAttribute* — значение MF \_ source \_ Reader \_ медиасаурце \_ характеристики.

Тип **пропвариант** для этого атрибута — **VT \_ UI4**.

## <a name="examples"></a>Примеры


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



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
</dt> </dl>

 

 




