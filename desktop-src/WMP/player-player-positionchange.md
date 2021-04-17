---
title: Событие Player. Поситиончанже
description: Событие Поситиончанже возникает при изменении текущей позиции элемента мультимедиа.
ms.assetid: 0561c58c-da5d-438e-adf8-2472405c6b9e
keywords:
- Проигрыватель Windows Media Event Поситиончанже
- Проигрыватель Windows Media Event Поситиончанже, класс Player
- Класс проигрывателя Windows Media Player, событие Поситиончанже
topic_type:
- apiref
api_name:
- Player.PositionChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ab7f64d6f5c4a081b8a81a14e3fcb353e1478e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704411"
---
# <a name="playerpositionchange-event"></a>Событие Player. Поситиончанже

Событие **поситиончанже** возникает при изменении текущей позиции элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
Player.PositionChange(
  oldPosition,
  newPosition
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*олдпоситион* 
</dt> <dd>

Число (**Double**), указывающее старую точку.

</dd> <dt>

*невпоситион* 
</dt> <dd>

**Число** (**Double**), задающее новую точку.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Это событие не вызывается во время воспроизведения. Это происходит только тогда, когда что-то активно изменяет текущее положение воспроизводимого мультимедийного элемента, например перемещение маркера поиска или кода, указывающего значение для *элементов управления*. **CurrentPosition**.

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





