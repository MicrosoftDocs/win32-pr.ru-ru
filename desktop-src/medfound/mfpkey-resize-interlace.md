---
description: Указывает, является ли входной поток чередованием.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Свойство MFPKEY_RESIZE_INTERLACE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a27504bd6da92bc48fee04afc999568a514fdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662827"
---
# <a name="mfpkey_resize_interlace-property"></a>МФПКЭЙ \_ \_ Свойства развертки изменения размера

Указывает, является ли входной поток чередованием.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="applies-to"></a>Применение

-   [DSP изменения видеоконтроллеров](videoresizer.md)

## <a name="remarks"></a>Комментарии

Используйте одно из следующих значений:



| Значение     | Описание |
|-----------|-------------|
| VT \_ false | прогрессивный |
| VT \_ true  | Interlaced  |



 

Если это свойство не задано, DSP использует входной тип носителя для определения, является ли видео чередованием. Это свойство можно задать, чтобы переопределить параметр типа мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
