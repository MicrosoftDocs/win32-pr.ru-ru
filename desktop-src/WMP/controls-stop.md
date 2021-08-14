---
title: Метод Controls. останавливаться
description: Метод Stop останавливает воспроизведение элемента мультимедиа. | Метод Controls. останавливаться
ms.assetid: ace95fde-9c94-4737-88f2-94321cbc687c
keywords:
- проигрыватель Windows Media метода завершения
- метод завершения проигрыватель Windows Media, класс controls
- класс элементов управления проигрыватель Windows Media, метод завершения
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
ms.openlocfilehash: b882f462903c2c5f75a3655cd26b927e7439043828dad41fcce7d0e64e4ce812
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580163"
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

## <a name="remarks"></a>Remarks

этот метод заставляет проигрыватель Windows Media освобождать какие-либо системные ресурсы, которые он использует, например звуковое устройство. Однако текущий элемент мультимедиа не освобожден.

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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
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

 

 





