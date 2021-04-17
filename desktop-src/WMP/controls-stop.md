---
title: Метод Controls. останавливаться
description: Метод Stop останавливает воспроизведение элемента мультимедиа. | Метод Controls. останавливаться
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- метод завершения проигрывателя Windows Media Player
- метод завершения Windows Media Player, класс Controls
- Управляет проигрывателем Windows Media Player, методом завершения
topic_type:
- apiref
api_name:
- Controls.stop
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e1ffc581fffbce0a341559e82c6bd196f712149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694941"
---
# <a name="controlsstop-method"></a>Метод Controls. останавливаться

Метод **Stop** останавливает воспроизведение элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.stop()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод заставляет проигрыватель Windows Media освобождать любые системные ресурсы, которые он использует, например звуковое устройство. Однако текущий элемент мультимедиа не освобожден.

Когда игрок остановлен, запись начнется на начало. Вызов **Play** начнет воспроизведение клипа с самого начала. Чтобы остановить операцию воспроизведения без изменения текущей позицией, используйте метод **Pause** .

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который **использует метод «приостанавливает»** для отмены воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "STOP"  NAME = "STOP"  VALUE = "Stop"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Stop'))

            /* Stop the Player. */
            Player.controls.stop();
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

[**Controls. Next**](controls-next.md)
</dt> <dt>

[**Controls. Pause**](controls-pause.md)
</dt> <dt>

[**Controls. Previous**](controls-previous.md)
</dt> </dl>

 

 





