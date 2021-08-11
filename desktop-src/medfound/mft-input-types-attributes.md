---
description: Содержит зарегистрированные входные типы для Media Foundation преобразования (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: Атрибут MFT_INPUT_TYPES_Attributes (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a750094361cdaa877bff82e20a74c1beae4e1a1f76ea0a9ad5be83f308c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118240239"
---
# <a name="mft_input_types_attributes-attribute"></a>\_ \_ Атрибут атрибутов входных типов MFT \_

Содержит зарегистрированные входные типы для Media Foundation преобразования (MFT).

## <a name="data-type"></a>Тип данных

**MFT \_ \_ \_ Сведения \[ о \] типе регистрации** хранятся в виде **байта \[ \]**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес::-BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Remarks

Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Этот атрибут содержит массив структур [**\_ \_ \_ сведений о типе регистра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , описывающих один или несколько форматов входных данных, поддерживаемых MFT. Эти значения берутся из реестра и предназначены в качестве подсказки для приложения. Таблица MFT может поддерживать дополнительные форматы. Чтобы задать фактический формат входных данных, необходимо создать таблицу MFT и вызвать [**имфтрансформ:: сетинпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).

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

 

 




