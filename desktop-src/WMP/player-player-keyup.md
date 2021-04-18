---
title: Событие Player. KeyUp
description: Событие KeyUp возникает при отпускании клавиши. | Событие Player. KeyUp
ms.assetid: 8b624374-403f-4d41-8481-5e94cee70861
keywords:
- Проигрыватель Windows Media, событие KeyUp
- Клавиша Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, событие KeyUp
topic_type:
- apiref
api_name:
- Player.KeyUp
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06e9b77871e9f62d46bdfa223bfa40b87feaf06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685301"
---
# <a name="playerkeyup-event"></a>Событие Player. KeyUp

Событие **KeyUp** возникает при отпускании клавиши.

## <a name="syntax"></a>Синтаксис


```JScript
Player.KeyUp(
  nKeyCode,
  nShiftState
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нкэйкоде* 
</dt> <dd>

**Число** (**int**), указывающее, какой физический ключ нажат. Возможные значения см. в разделе [событие Player. KeyDown](player-player-keydown.md).

</dd> <dt>

*ншифтстате* 
</dt> <dd>

**Число** (**int**), задающее битовую глубину, которая соответствует клавише Shift (бит 0), клавиша Ctrl (бит 1) и клавиша Alt (бит 2). Эти биты соответствуют значениям 1, 2 и 4 соответственно. Аргумент shift указывает состояние этих ключей. Можно установить некоторые, все или ни одного бита, указывая, что не нажаты некоторые, все или ни один из этих ключей.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





