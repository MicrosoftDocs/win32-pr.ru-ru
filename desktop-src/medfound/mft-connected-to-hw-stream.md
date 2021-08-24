---
description: Указывает, подключено ли аппаратное преобразование Media Foundation к другому MFT на основе оборудования.
ms.assetid: 9166c43f-d2ae-4dc7-84e9-02146b67efe2
title: Атрибут MFT_CONNECTED_TO_HW_STREAM (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31ff2a2dea2fcb67cff776ba02c43193b571a382df57a5d0562f3f2cd1fb7248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602874"
---
# <a name="mft_connected_to_hw_stream-attribute"></a>MFT \_ подключено \_ к \_ \_ атрибуту потока HW

Указывает, подключено ли аппаратное преобразование Media Foundation к другому MFT на основе оборудования.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Приложения обычно не используют этот атрибут.

Этот атрибут используется с МФТС на основе оборудования. При подключении двух МФТС оборудования в топологии загрузчик топологии присваивает этому атрибуту **значение true** для следующих объектов:

-   Выходной поток вышестоящей MFT
-   Входной поток нисходящих файлов MFT

Чтобы получить хранилище атрибутов для выходного потока, загрузчик топологии вызывает [**имфтрансформ:: жетаутпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreamattributes) в вышестоящей MFT. Чтобы получить хранилище атрибутов для входного потока, загрузчик топологии вызывает [**имфтрансформ:: жетинпутстреаматтрибутес**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes) в ПОДЧИНЕННОЙ таблице MFT.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Оборудование МФТС](hardware-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




