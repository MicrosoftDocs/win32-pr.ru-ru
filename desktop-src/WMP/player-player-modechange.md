---
title: Событие Player. Модечанже
description: Событие Модечанже возникает при изменении режима проигрывателя Windows Media. | Событие Player. Модечанже
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Проигрыватель Windows Media Event Модечанже
- Проигрыватель Windows Media Event Модечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Модечанже
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704177"
---
# <a name="playermodechange-event"></a>Событие Player. Модечанже

Событие **модечанже** возникает при изменении режима проигрывателя Windows Media.

## <a name="syntax"></a>Синтаксис


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*моденаме* 
</dt> <dd>

**Строка** , указывающая режим, который был изменен. Содержит одно из следующих значений:



| Значение   | Описание                                         |
|---------|-----------------------------------------------------|
| shuffle | Дорожки воспроизводятся в случайном порядке.                  |
| loop    | Все последовательности дорожек воспроизводятся постоянно. |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**Логическое значение** , указывающее новое состояние указанного режима.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Settings. Мода**](settings-getmode.md)
</dt> <dt>

[**Settings. setMode**](settings-setmode.md)
</dt> </dl>

 

 





