---
title: Метод Controls. Next
description: Следующий метод задает текущий элемент для следующего элемента списка воспроизведения.
ms.assetid: 67436c76-8fb9-4350-86f3-67f5e9e6dca1
keywords:
- следующий метод проигрыватель Windows Media
- следующий метод проигрыватель Windows Media, класс controls
- класс элементов управления проигрыватель Windows Media, метод next
topic_type:
- apiref
api_name:
- Controls.next
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a40c063163b0dadaa3db2d0d6281ace64312f68ee999763e6b27d4bd98f84d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997474"
---
# <a name="controlsnext-method"></a>Метод Controls. Next

**Следующий** метод задает текущий элемент для следующего элемента списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.next()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Если список воспроизведения находится в последней записи при вызове **Next** , первая запись списка воспроизведения станет текущей.

Для списков воспроизведения на стороне сервера этот метод пропускает следующий элемент в списке воспроизведения на стороне сервера, а не в списке воспроизведения клиента.

При воспроизведении DVD этот метод пропускает следующую логическую главу в последовательности воспроизведения, которая может не быть следующей главой в списке воспроизведения. При каждом воспроизведении DVD-диска этот метод пропускается до следующего.

## <a name="examples"></a>Примеры

В следующем примере создается HTML-элемент BUTTON, который использует **Next** для перехода к следующему элементу в текущем списке воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
<INPUT TYPE = "BUTTON"  ID = "NEXT"  NAME = "NEXT"  VALUE = ">>|"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Next'))

            /* Move to the next item in the playlist. */
            Player.controls.next();
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

[**Controls. Previous**](controls-previous.md)
</dt> <dt>

[**Controls. останавливаться**](controls-stop.md)
</dt> </dl>

 

 





