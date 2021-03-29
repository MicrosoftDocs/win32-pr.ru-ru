---
description: Содержит указатель на атрибуты потока подключенного потока на аппаратном Media Foundation преобразовании (MFT).
ms.assetid: 7e14a02e-4cbf-45aa-a6f5-2c53b2437127
title: Атрибут MFT_CONNECTED_STREAM_ATTRIBUTE (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b182cbed78f5f9851b621de72bf691bf698b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898730"
---
# <a name="mft_connected_stream_attribute-attribute"></a>\_ \_ Атрибут атрибута потока, подключенного к MFT \_

Содержит указатель на атрибуты потока подключенного потока на аппаратном Media Foundation преобразовании (MFT).

## <a name="data-type"></a>Тип данных

**Имфаттрибутес \** _ хранится как _*IUnknown \**_

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: ununknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Комментарии

Приложения обычно не используют этот атрибут.

Этот атрибут используется для МФТС, которые действуют как прокси-серверы для аппаратного устройства. Дополнительные сведения см. в разделе [Hardware МФТС](hardware-mfts.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



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

 

 




