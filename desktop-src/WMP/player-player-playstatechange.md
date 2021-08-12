---
title: Событие Player. Плайстатечанже
description: Событие Плайстатечанже возникает при изменении свойства Плайстате.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- проигрыватель Windows Media событий плайстатечанже
- проигрыватель Windows Media событий плайстатечанже, класс Player
- класс проигрывателя проигрыватель Windows Media, событие плайстатечанже
topic_type:
- apiref
api_name:
- Player.PlayStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3995f7373984ae9e3b0e24f9f41390154326cfd87bd8589970dc76520c6efd93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572530"
---
# <a name="playerplaystatechange-event"></a>Событие Player. Плайстатечанже

Событие **плайстатечанже** возникает при изменении свойства **плайстате** .

## <a name="syntax"></a>Синтаксис


```JScript
Player.PlayStateChange(
  NewState
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*NewState* 
</dt> <dd>

Число (**Long**), которое указывает новый **плайстате**. См. [плайстате](player-playstate.md) для таблицы возможных значений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

состояния проигрыватель Windows Media не гарантированно выполняются в каком бы то ни было определенном порядке. Кроме того, не все состояния должны происходить во время последовательности событий. Не следует писать код, зависящий от порядка состояний.

## <a name="examples"></a>Примеры

В следующем примере показан обработчик событий для *проигрывателя*. событие **плайстатечанже** . Текстовый элемент HTML с именем «myText» отображает новое состояние воспроизведения. Объект Player создан с ИДЕНТИФИКАТОРом "Player".


```JScript
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = playStateChange(NewState)>

// Test for the player current state, display a message for each.
switch (NewState){
    case 1:
        myText.value = "Stopped";
        break;

    case 2:
        myText.value = "Paused";
        break;

    case 3:
        myText.value = "Playing";
        break;

    // Other cases go here.

    default:
        myText.value = "";
}
</SCRIPT>
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Плайстате**](player-playstate.md)
</dt> </dl>

 

 





