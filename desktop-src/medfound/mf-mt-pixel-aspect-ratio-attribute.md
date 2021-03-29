---
description: Пропорции пикселя для типа видеоклипа.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Атрибут MF_MT_PIXEL_ASPECT_RATIO (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542159"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a>\_ \_ \_ Атрибут соотношения сторон MF MT пикселей \_

Пропорции пикселя для типа видеоклипа.

## <a name="data-type"></a>Тип данных

**UINT64**

## <a name="remarks"></a>Комментарии

Верхние 32 бит содержат числитель с пропорциями в пикселях, а младшие 32 бита содержат знаменатель. Числитель является горизонтальным компонентом пропорций; знаменатель является вертикальным компонентом.

Чтобы задать этот атрибут, используйте функцию [**мфсетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) . Чтобы получить этот атрибут, используйте функцию [**мфжетаттрибутератио**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .

Соотношение пиксельных пропорций описывает форму пикселов в отображаемом видеоизображении. Установите этот атрибут, если изображение содержит неквадратные пикселы. Для правильной работы на устройстве вывода с квадратными пикселами изображение должно масштабироваться путем обратного пропорций изображения.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты типа мультимедиа](media-type-attributes.md)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Пропорции рисунка](picture-aspect-ratio.md)
</dt> </dl>

 

 




