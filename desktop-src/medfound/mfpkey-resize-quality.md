---
description: Указывает, следует ли использовать алгоритм, создающий видео более высокого качества, или более быстрый алгоритм.
ms.assetid: a6760e7e-7c99-4412-bde5-05958fad89a1
title: Свойство MFPKEY_RESIZE_QUALITY (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8aeb59935c8fc3462b713967ed2b14a0adfcf731fa1a71fec434b0e07d4309
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973413"
---
# <a name="mfpkey_resize_quality-property"></a>МФПКЭЙ \_ изменить \_ свойство качества

Указывает, следует ли использовать алгоритм, создающий видео более высокого качества, или более быстрый алгоритм.

## <a name="constant-for-ipropertybag"></a>Константа для Ипропертибаг

Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Тип данных

Логическое значение VT \_

## <a name="applies-to"></a>Применяется к

-   [DSP изменения видеоконтроллеров](videoresizer.md)

## <a name="remarks"></a>Remarks

Используйте одно из следующих значений:



| Значение     | Описание          |
|-----------|----------------------|
| VT \_ false | Более быстрый алгоритм     |
| VT \_ true  | Видео высокого качества |



 

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

 

 
