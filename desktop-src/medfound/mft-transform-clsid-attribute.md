---
description: Содержит идентификатор класса (CLSID) Media Foundation преобразования (MFT).
ms.assetid: 99ee6f50-1de7-41ea-be5b-135730138d5d
title: Атрибут MFT_TRANSFORM_CLSID_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0122b783d8b321aa2a5c7788a589e19625b6a2bde8e37b0b659b0a1192f8c7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240202"
---
# <a name="mft_transform_clsid_attribute-attribute"></a>\_ \_ Атрибут атрибута CLSID преобразования MFT \_

Содержит идентификатор класса (CLSID) Media Foundation преобразования (MFT).

## <a name="data-type"></a>Тип данных

**GUID**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)InAttribute.

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Remarks

Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Этот атрибут используется внутренне объектом активации при создании таблицы MFT. Приложения не должны использовать этот CLSID напрямую для создания MFT, так как объекту активации может потребоваться инициализация MFT. Таким образом, чтобы создать экземпляр MFT, вызовите [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) в объекте активации.

Обратите внимание, что функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) работает иначе, чем функция [**мфтенум**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) в этом отношении. Функция **мфтенум** возвращает идентификаторы CLSID, которые приложение передает в функцию **CoCreateInstance** . Функция **мфтенумекс** возвращает объекты активации, а не CLSID.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также статью

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




