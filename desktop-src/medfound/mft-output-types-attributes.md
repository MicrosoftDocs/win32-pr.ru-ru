---
description: Содержит зарегистрированные типы выходных данных для Media Foundation преобразования (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Атрибут MFT_OUTPUT_TYPES_Attributes (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701804"
---
# <a name="mft_output_types_attributes-attribute"></a>\_ \_ Атрибут атрибутов типов выходных данных MFT \_

Содержит зарегистрированные типы выходных данных для Media Foundation преобразования (MFT).

## <a name="data-type"></a>Тип данных

**MFT \_ \_ \_ Сведения \[ о \] типе регистрации** хранятся в виде **байта \[ \]**

## <a name="remarks"></a>Комментарии

Этот атрибут задается для указателей [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращаемых функцией [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .

Этот атрибут содержит массив структур [**\_ \_ \_ сведений о типе регистра MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) , описывающих один или несколько выходных форматов, поддерживаемых MFT. Эти значения берутся из реестра и предназначены в качестве подсказки для приложения. Таблица MFT может поддерживать дополнительные форматы. Чтобы задать реальный формат вывода, необходимо создать таблицу MFT и вызвать [**имфтрансформ:: сетаутпуттипе**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).

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

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




