---
description: Содержит значение неустановленного аппаратного кодека.
ms.assetid: 1df40a42-4c02-473f-a87f-2ae2d42e4f4e
title: Атрибут MFT_CODEC_MERIT_Attribute (Мфтрансформ. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74745244824bc766d0f7c1e691cb5f176d1da6a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105656556"
---
# <a name="mft_codec_merit_attribute-attribute"></a>\_ \_ Атрибут атрибута «неуспешный кодек MFT» \_

Содержит значение неустановленного аппаратного кодека.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Этот атрибут задается в объекте активации для Media Foundation преобразования (MFT), представляющего аппаратный кодек. Значением атрибута является значение «неуспешный» кодека.

Этот атрибут управляет порядком, в котором функция [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) перечисляет кодеки, если установлен флаг **\_ \_ \_ сортандфилтер флага перечисления MFT** . МФТС со значением в списке выше, чем у других МФТС.

Этот атрибут не содержит надежного значения. Чтобы проверить фактическое значение соответствия кодека, вызовите функцию [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) .

Если значение \_ \_ атрибута атрибута «несоответствие кодека MFT \_ » не совпадает со значением, полученным с помощью [**мфжетмфтмерит**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit), метод [**имфактивате:: Активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) завершается сбоем и возвращает **MF \_ E \_ Недопустимый \_ кодек \_**.

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

 

 




