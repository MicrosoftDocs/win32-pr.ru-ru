---
title: Controls. Фастреверсе, метод
description: Метод Фастреверсе запускает быстрое сканирование элемента мультимедиа в обратном направлении.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- Фастреверсе метод Windows Media Player
- метод Фастреверсе Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Фастреверсе
topic_type:
- apiref
api_name:
- Controls.fastReverse
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73e5a63c4299bf08c25e36e2d61924f3fb171792
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694902"
---
# <a name="controlsfastreverse-method"></a>Controls. Фастреверсе, метод

Метод **фастреверсе** запускает быстрое сканирование элемента мультимедиа в обратном направлении.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.fastReverse()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Метод **фастреверсе** просматривает клип в обратную, в пять раз превышающую нормальную скорость, отображая только ключевые кадры, если это видеофайл. При вызове **фастреверсе** изменяется *Настройка параметров*. Свойство **Rate** до 5,0. Если **ставка** впоследствии изменилась или вызывается **Воспроизведение** или **прекращение** , проигрыватель Windows Media прекратит обратный.

Если элемент является частью списка воспроизведения, **фастреверсе** останавливается в начале текущей записи. Например, если параметр Track 3 находится в **фастреверсе**, то при достижении начала Track 3 проигрыватель Windows Media не будет переходить к разделу Track 2. При вызове **фастреверсе** Счетчик воспроизведения не увеличивается.

Если вы вызываете **фастфорвард** , когда действует **фастреверсе** , **фастреверсе** будет остановлена, а **фастфорвард** начнется.

Этот метод не работает для широковещательных трансляций и определенных типов носителей. Чтобы определить, можно ли использовать функцию быстрого просмотра клипа, вызовите **метод «фастреверсе**».

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который использует **фастреверсе** для запуска быстрого воспроизведения элемента мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "REW"  NAME = "REW"  VALUE = "<<"  

    /* Run JScript when the BUTTON is clicked. 
       Check first to make sure fast-reverse mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastReverse'))
        Player.controls.fastReverse();
">
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Controls. Фастфорвард**](controls-fastforward.md)
</dt> <dt>

[**Элементы управления. доступно**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. останавливаться**](controls-stop.md)
</dt> <dt>

[**Параметры. rate**](settings-rate.md)
</dt> </dl>

 

 





