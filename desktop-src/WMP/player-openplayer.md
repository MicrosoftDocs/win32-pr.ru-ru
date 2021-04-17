---
title: Метод Player. Опенплайер
description: Метод Опенплайер открывает проигрыватель Windows Media с использованием указанного URL-адреса. | Метод Player. Опенплайер
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- Опенплайер метод Windows Media Player
- метод Опенплайер проигрывателя Windows Media Player, класс Player
- Класс проигрывателя Windows Media Player, метод Опенплайер
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704347"
---
# <a name="playeropenplayer-method"></a>Метод Player. Опенплайер

Метод **опенплайер** открывает проигрыватель Windows Media с использованием указанного URL-адреса.

## <a name="syntax"></a>Синтаксис


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*URL-адрес* \[ окне\]
</dt> <dd>

**Строка** , представляющая URL-адрес элемента мультимедиа для воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод запускает проигрыватель Windows Media с указанным URL-адресом в качестве текущего элемента мультимедиа. Если проигрыватель был ранее закрыт в режиме обложки, он будет открыт с использованием обложки, последней выбранной пользователем. В противном случае проигрыватель откроется в полноэкранном режиме.

Если этот метод вызывается из элемента управления Плайерактивекс Windows Media, внедренного в удаленный режим, его поведение идентично *плайераппликатион*. метод **свитчтоплайераппликатион** .

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Плайераппликатион. Свитчтоплайераппликатион**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





