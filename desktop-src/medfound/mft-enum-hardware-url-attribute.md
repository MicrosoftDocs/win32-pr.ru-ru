---
description: Содержит символьную ссылку для преобразования Media Foundation на основе оборудования (MFT).
ms.assetid: 7e153051-a167-4ff7-8178-b290d8a1345e
title: Атрибут MFT_ENUM_HARDWARE_URL_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 539aa1ecbf8bf322e7397a50bb16175dbcca806f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263896"
---
# <a name="mft_enum_hardware_url_attribute-attribute"></a>\_ \_ \_ Атрибут атрибута аппаратного URL-адреса перечисления MFT \_

Содержит символьную ссылку для преобразования Media Foundation на основе оборудования (MFT).

## <a name="data-type"></a>Тип данных

**WCHAR \** _

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [_ *имфаттрибутес:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Комментарии

Этот атрибут поддерживается МФТС на основе оборудования. Значение атрибута является символьной ссылкой для драйвера устройства. Этот атрибут также задается в [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) указателях, выделенных функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , если эти указатели представляют аппаратное МФТС.

Символьная ссылка должна рассматриваться как непрозрачная строка. Чтобы получить отображаемое имя для устройства, запросите [атрибут \_ понятного \_ имени MFT](mft-friendly-name-attribute.md) .

Для программного МФТС не должен быть задан этот атрибут.

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

[Оборудование МФТС](hardware-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




