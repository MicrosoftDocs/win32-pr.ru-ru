---
description: Указывает, использует ли Имфтрансформ аппаратный DRM.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b46760fd5759abdd601269f5905f0649145649713839de5fe6424bc36219c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118473554"
---
# <a name="mft_using_hardware_drm-attribute"></a>MFT \_ с использованием \_ аппаратного \_ атрибута DRM

Указывает, использует ли Имфтрансформ аппаратный DRM.

## <a name="data-type"></a>Тип данных

**UINT32** (рассматривается как **bool**)

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/win32/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Применяется к

[**имтрансфром**](/windows/win32/api/mftransform/nn-mftransform-imftransform)

## <a name="remarks"></a>Remarks

Если расшифровка MFT задает для этого атрибута значение 1, то используется аппаратный DRM. Если расшифровка MFT задает для этого атрибута значение 0, то оборудование DRM не используется. Если в расшифровке MFT не указан этот атрибут или указано другое значение, то он не (или не может) указать, использует ли он аппаратный DRM.


Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 Обновление за Апрель 2020   <br/>                                       |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




