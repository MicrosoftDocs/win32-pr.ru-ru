---
description: Содержит указатель на атрибуты потока подключенного потока на аппаратном Media Foundation преобразовании (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Атрибут MFT_CONNECTED_STREAM_ATTRIBUTE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2289b8f1e8d5d751f7aa69564b8bbd26d865b43efedb474529147385b1851bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722570"
---
# <a name="mft_connected_stream_attribute-attribute"></a>\_ \_ Атрибут атрибута потока, подключенного к MFT \_

Содержит указатель на атрибуты потока подключенного потока на аппаратном Media Foundation преобразовании (MFT).

## <a name="data-type"></a>Тип данных

**Имфаттрибутес \* *_ хранится как _* IUnknown\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: ununknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Remarks

Приложения обычно не используют этот атрибут.

Этот атрибут используется для МФТС, которые действуют как прокси-серверы для аппаратного устройства. Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Заголовок<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[MFT \_ подключено \_ к \_ аппаратному \_ потоку](mft-connected-to-hw-stream.md)
</dt> <dt>

[Оборудование МФТС](hardware-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




