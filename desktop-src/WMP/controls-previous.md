---
title: Метод Controls. Previous
description: Предыдущий метод устанавливает текущий элемент на предыдущий элемент в списке воспроизведения.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- Предыдущий метод проигрывателя Windows Media
- Предыдущий метод проигрыватель Windows Media, класс Controls
- Класс элементов управления проигрыватель Windows Media Player, предыдущий метод
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698761"
---
# <a name="controlsprevious-method"></a>Метод Controls. Previous

**Предыдущий** метод устанавливает текущий элемент на предыдущий элемент в списке воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.previous()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Если список воспроизведения находится в первой записи при вызове **предыдущего** , последняя запись списка воспроизведения станет текущей.

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который использует **Previous** для перехода к предыдущему элементу в текущем списке воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
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

[**Controls. останавливаться**](controls-stop.md)
</dt> </dl>

 

 





