---
description: Содержит флаги для объекта активации Media Foundation преобразования (MFT).
ms.assetid: de377132-19b0-4c8c-882e-193c31420739
title: Атрибут MF_TRANSFORM_FLAGS_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d54d8775cb58980e0b5b4a8557ae4a3e8082b045eb3e87330841f75dfd057774
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739232"
---
# <a name="mf_transform_flags_attribute-attribute"></a>\_ \_ Атрибут атрибута флага MF Transform \_

Содержит флаги для объекта активации Media Foundation преобразования (MFT).

## <a name="data-type"></a>Тип данных

**UINT32**

Значение представляет собой побитовое **или** для флагов перечисления [**\_ MFT \_ Enum \_ Flag**](/windows/win32/api/mfapi/ne-mfapi-_mft_enum_flag) .

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) . Атрибут содержит флаги, описывающие основную таблицу файлов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 
