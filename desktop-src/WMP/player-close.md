---
title: Метод Player. Close
description: Метод Close освобождает ресурсы проигрывателя Windows Media.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- закрыть метод проигрыватель Windows Media Player
- закрыть метод проигрыватель Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695186"
---
# <a name="playerclose-method"></a>Метод Player. Close

Метод **Close** освобождает ресурсы проигрывателя Windows Media.

## <a name="syntax"></a>Синтаксис


```JScript
Player.close()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод закрывает текущий файл мультимедиа, а не проигрыватель Windows Media.

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который при щелчке останавливает воспроизведение в проигрывателе Windows Media и освобождает используемые ресурсы. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





