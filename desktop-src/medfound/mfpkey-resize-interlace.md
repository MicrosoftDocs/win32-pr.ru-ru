---
description: MFPKEY_RESIZE_INTERLACE свойство — указывает, является ли входной поток чередованием.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Свойство MFPKEY_RESIZE_INTERLACE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c614865d0c8a49238b9c8d6f7714787bb22aaadaa317a8a3a0405a7f51c87be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873038"
---
# <a name="mfpkey_resize_interlace-property"></a>МФПКЭЙ \_ \_ Свойства развертки изменения размера

Указывает, является ли входной поток чередованием.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="applies-to"></a>Применяется к

-   [DSP изменения видеоконтроллеров](videoresizer.md)

## <a name="remarks"></a>Remarks

Используйте одно из следующих значений:



| Значение     | Описание |
|-----------|-------------|
| VT \_ false | прогрессивный |
| VT \_ true  | Interlaced  |



 

Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием. Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| Заголовок<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
