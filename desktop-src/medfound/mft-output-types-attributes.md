---
description: Содержит зарегистрированные типы выходных данных для Media Foundation преобразования (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Атрибут MFT_OUTPUT_TYPES_Attributes (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d244bc5184652d0ba1d89ebf4e1beaddb472bb1d6fa09c05d1edf99030fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462784"
---
# <a name="mft_output_types_attributes-attribute"></a>\_ \_ Атрибут атрибутов типов выходных данных MFT \_

Содержит зарегистрированные типы выходных данных для Media Foundation преобразования (MFT).

## <a name="data-type"></a>Тип данных

**MFT \_ \_ \_ Сведения \[ о \] типе регистрации** хранятся в виде **байта \[ \]**

## <a name="remarks"></a>Remarks

Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Этот атрибут содержит массив структур [**\_ \_ \_ сведений о типе регистра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , описывающих один или несколько выходных форматов, поддерживаемых MFT. Эти значения берутся из реестра и предназначены в качестве подсказки для приложения. Таблица MFT может поддерживать дополнительные форматы. Чтобы задать реальный формат вывода, необходимо создать таблицу MFT и вызвать [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

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

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




