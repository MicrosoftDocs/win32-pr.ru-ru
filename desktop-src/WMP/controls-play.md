---
title: Метод Controls. Play
description: Метод Play заставляет текущий элемент мультимедиа начать воспроизведение или возобновить воспроизведение приостановленного элемента.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- воспроизвести метод проигрыватель Windows Media
- метод Play проигрыватель Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, методом Play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698897"
---
# <a name="controlsplay-method"></a>Метод Controls. Play

Метод **Play** заставляет текущий элемент мультимедиа начать воспроизведение или возобновить воспроизведение приостановленного элемента.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.play()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если этот метод вызывается при быстрой пересылке или перемотки, значение *параметров*. **ставка** устанавливается равным 1,0.

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который использует **Play** для воспроизведения текущего элемента мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
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
</dt> </dl>

 

 





