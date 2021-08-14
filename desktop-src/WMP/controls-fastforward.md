---
title: Controls. Фастфорвард, метод
description: Метод Фастфорвард запускает быстрое воспроизведение элемента мультимедиа в прямом направлении. | Controls. Фастфорвард, метод
ms.assetid: 69cee803-f76b-4a8c-a2c2-1870665afaf9
keywords:
- проигрыватель Windows Media метода фастфорвард
- проигрыватель Windows Media метода фастфорвард, класс controls
- класс элементов управления проигрыватель Windows Media, метод фастфорвард
topic_type:
- apiref
api_name:
- Controls.fastForward
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8b35c2a31c26259a12638d09c968b90ea42f93c692bf4c24af9dc987a6df3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341820"
---
# <a name="controlsfastforward-method"></a>Controls. Фастфорвард, метод

Метод **фастфорвард** запускает быстрое воспроизведение элемента мультимедиа в прямом направлении.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.fastForward()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Метод **фастфорвард** воспроизводит клип назад в пять раз подряд с обычной скоростью. при вызове **фастфорвард** изменяется *Параметры*. Свойство **Rate** до 5,0. если **ставка** впоследствии изменилась или вызывается **play** или **остановка** , проигрыватель Windows Media прекращает быструю пересылку.

Метод **фастфорвард** не работает для широковещательных трансляций и определенных типов носителей. Чтобы определить, можно ли быстро перемотать клип, **вызовите метод «фастфорвард**».

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который использует **фастфорвард** для запуска быстрого воспроизведения элемента мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "FF"  NAME = "FF"  VALUE = ">>"  

    /* Execute JScript when the BUTTON is clicked. 
       Check first to make sure fast-forward mode is available
       for this particular media item */
    onClick = "if (Player.controls.isAvailable('FastForward'))
        Player.controls.fastForward();
">

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Элементы управления. доступно**](controls-isavailable.md)
</dt> <dt>

[**Controls. Play**](controls-play.md)
</dt> <dt>

[**Controls. останавливаться**](controls-stop.md)
</dt> <dt>

[**Параметры. rate**](settings-rate.md)
</dt> </dl>

 

 





