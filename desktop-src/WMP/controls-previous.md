---
title: Метод Controls. Previous
description: Предыдущий метод устанавливает текущий элемент на предыдущий элемент в списке воспроизведения.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- предыдущий метод проигрыватель Windows Media
- предыдущий метод проигрыватель Windows Media, класс controls
- класс элементов управления проигрыватель Windows Media, предыдущий метод
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
ms.openlocfilehash: f67dbc80fb731f32eefb36f2a0f66c852da3da69dbc6b7ae56c03ebafb06e07e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119333"
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

## <a name="remarks"></a>Remarks

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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Controls. Next**](controls-next.md)
</dt> <dt>

[**Controls. останавливаться**](controls-stop.md)
</dt> </dl>

 

 





