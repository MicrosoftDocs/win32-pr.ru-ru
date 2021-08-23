---
description: Содержит отображаемое имя для аппаратного преобразования Media Foundation (MFT).
ms.assetid: 8f2634e8-6bdd-463a-893a-6dc616c8333d
title: Атрибут MFT_FRIENDLY_NAME_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b867db021c43679fef026022bf95bda1186a679eb544465393562b0a51d5d7af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554924"
---
# <a name="mft_friendly_name_attribute-attribute"></a>\_ \_ Атрибут атрибута понятного имени MFT \_

Содержит отображаемое имя для аппаратного преобразования Media Foundation (MFT).

## <a name="data-type"></a>Тип данных

**WCHAR\***

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Remarks

Этот атрибут поддерживается МФТС на основе оборудования. Он также задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , выделенных функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) , если эти указатели представляют аппаратную МФТС.

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

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




