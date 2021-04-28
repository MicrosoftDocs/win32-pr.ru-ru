---
description: MFPKEY_RESIZE_INTERLACE свойство — указывает, является ли входной поток чередованием.
ms.assetid: 01ee0766-06ed-4255-9057-2fe033a772cd
title: Свойство MFPKEY_RESIZE_INTERLACE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45d0efe93901a08322a05dbed2515f76b04a214b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092882"
---
# <a name="mfpkey_resize_interlace-property"></a>МФПКЭЙ \_ \_ Свойства развертки изменения размера

Указывает, является ли входной поток чередованием.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="applies-to"></a>Применение

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
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                             |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Вмкодекдсп. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
