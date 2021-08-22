---
title: Событие Player. Модечанже
description: событие модечанже возникает при изменении режима проигрыватель Windows Media. | Событие Player. Модечанже
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- проигрыватель Windows Media событий модечанже
- проигрыватель Windows Media событий модечанже, класс Player
- класс проигрывателя проигрыватель Windows Media, событие модечанже
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
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054362"
---
# <a name="playermodechange-event"></a>Событие Player. Модечанже

событие **модечанже** возникает при изменении режима проигрыватель Windows Media.

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

## <a name="remarks"></a>Remarks

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Параметры. мода**](settings-getmode.md)
</dt> <dt>

[**Параметры. setMode**](settings-setmode.md)
</dt> </dl>

 

 





