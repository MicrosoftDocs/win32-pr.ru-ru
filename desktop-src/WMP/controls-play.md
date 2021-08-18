---
title: Метод Controls. Play
description: Метод Play заставляет текущий элемент мультимедиа начать воспроизведение или возобновить воспроизведение приостановленного элемента.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- метод play проигрыватель Windows Media
- метод play проигрыватель Windows Media, класс controls
- класс элементов управления проигрыватель Windows Media, метод play
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
ms.openlocfilehash: 86ce3c1572515b320a62b1b3c76aac72e44101e21f3b0f89d7c3356046ea95f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997454"
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

## <a name="remarks"></a>Remarks

если этот метод вызывается при быстрой пересылке или перемотки, значение *Параметры*. **ставка** устанавливается равным 1,0.

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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> </dl>

 

 





