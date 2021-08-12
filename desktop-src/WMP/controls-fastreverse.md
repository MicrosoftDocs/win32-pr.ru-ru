---
title: Controls. Фастреверсе, метод
description: Метод Фастреверсе запускает быстрое сканирование элемента мультимедиа в обратном направлении.
ms.assetid: 4fc61739-9006-4d62-b2c1-2b8e8830f2d9
keywords:
- проигрыватель Windows Media метода фастреверсе
- проигрыватель Windows Media метода фастреверсе, класс controls
- класс элементов управления проигрыватель Windows Media, метод фастреверсе
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
ms.openlocfilehash: 3d4643525f66102cbd7b017a4a48f1068489062ec0849f197f1f55df45fc6f1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580280"
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

## <a name="remarks"></a>Remarks

Метод **фастреверсе** просматривает клип в обратную, в пять раз превышающую нормальную скорость, отображая только ключевые кадры, если это видеофайл. при вызове **фастреверсе** изменяется *Параметры*. Свойство **Rate** до 5,0. если **частота** в дальнейшем изменяется или вызывается **play** или **останавливаться** , проигрыватель Windows Media прекращается на обратный.

Если элемент является частью списка воспроизведения, **фастреверсе** останавливается в начале текущей записи. например, если для параметра track 3 задано значение **фастреверсе**, то при достижении начала track 3 проигрыватель Windows Media не будет переходить к дорожке 2. При вызове **фастреверсе** Счетчик воспроизведения не увеличивается.

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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
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

 

 





