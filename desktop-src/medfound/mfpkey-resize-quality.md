---
description: Указывает, следует ли использовать алгоритм, создающий видео более высокого качества, или более быстрый алгоритм.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Свойство MFPKEY_RESIZE_QUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e79ae1cac78b4d836261905afdacaf14fc227fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711778"
---
# <a name="mfpkey_resize_quality-property"></a>МФПКЭЙ \_ изменить \_ свойство качества

Указывает, следует ли использовать алгоритм, создающий видео более высокого качества, или более быстрый алгоритм.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="applies-to"></a>Применение

-   [DSP изменения видеоконтроллеров](videoresizer.md)

## <a name="remarks"></a>Комментарии

Используйте одно из следующих значений:



| Значение     | Описание          |
|-----------|----------------------|
| VT \_ false | Более быстрый алгоритм     |
| VT \_ true  | Видео высокого качества |



 

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

 

 
