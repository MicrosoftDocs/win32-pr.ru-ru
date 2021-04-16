---
description: Указывает, использует ли Имфтрансформ аппаратный DRM.
title: MFT_USING_HARDWARE_DRM (Mftransform.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e6dbacedbf5fd9298e4da5154bd82fcc9f39bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497763"
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

## <a name="remarks"></a>Комментарии

Если расшифровка MFT задает для этого атрибута значение 1, то используется аппаратный DRM. Если расшифровка MFT задает для этого атрибута значение 0, то оборудование DRM не используется. Если в расшифровке MFT не указан этот атрибут или указано другое значение, то он не (или не может) указать, использует ли он аппаратный DRM.


Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Обновление Windows 10 от апреля 2020   <br/>                                       |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>Мфтрансформ. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt>  <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 




