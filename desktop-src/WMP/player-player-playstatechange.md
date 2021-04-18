---
title: Событие Player. Плайстатечанже
description: Событие Плайстатечанже возникает при изменении свойства Плайстате.
ms.assetid: d4c4b114-04b6-4079-b6a2-52b336fc6dc1
keywords:
- Проигрыватель Windows Media Event Плайстатечанже
- Проигрыватель Windows Media Event Плайстатечанже, класс Player
- Класс проигрывателя Windows Media Player, событие Плайстатечанже
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
ms.openlocfilehash: e621d8698a5379b0d39a55db141fc0012f6ef969
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704199"
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

## <a name="remarks"></a>Комментарии

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

Состояния проигрывателя Windows Media не гарантированно выполняются в определенном порядке. Кроме того, не все состояния должны происходить во время последовательности событий. Не следует писать код, зависящий от порядка состояний.

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
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Плайстате**](player-playstate.md)
</dt> </dl>

 

 





