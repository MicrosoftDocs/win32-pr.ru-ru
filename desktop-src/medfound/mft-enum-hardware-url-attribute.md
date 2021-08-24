---
description: Содержит символьную ссылку для преобразования Media Foundation на основе оборудования (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Атрибут MFT_ENUM_HARDWARE_URL_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7119ea4bde7900087f706cb6fbc77c845721debab54dfa05b48f5c0094b1e29e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119722591"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_ \_ \_ Атрибут атрибута аппаратного URL-адреса перечисления MFT \_

Содержит символьную ссылку для преобразования Media Foundation на основе оборудования (MFT).

## <a name="data-type"></a>Тип данных

**WCHAR\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarks

Этот атрибут поддерживается МФТС на основе оборудования. Значение атрибута является символьной ссылкой для драйвера устройства. Этот атрибут также задается в [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателях, выделенных функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , если эти указатели представляют аппаратное МФТС.

Символьная ссылка должна рассматриваться как непрозрачная строка. Чтобы получить отображаемое имя для устройства, запросите [атрибут \_ понятного \_ имени MFT](mft-friendly-name-attribute.md) .

Для программного МФТС не должен быть задан этот атрибут.

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

 

 




