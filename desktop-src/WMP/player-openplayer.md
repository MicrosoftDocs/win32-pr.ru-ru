---
title: Метод Player. Опенплайер
description: метод опенплайер открывается проигрыватель Windows Media с использованием указанного URL-адреса. | Метод Player. Опенплайер
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- проигрыватель Windows Media метода опенплайер
- метод опенплайер проигрыватель Windows Media, класс Player
- класс Player проигрыватель Windows Media, метод опенплайер
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
ms.openlocfilehash: 42245ec29f7d7caeac17f116d1f592f74f10ba95716d5d16734ecd21bbcbb60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747572"
---
# <a name="playeropenplayer-method"></a>Метод Player. Опенплайер

метод **опенплайер** открывается проигрыватель Windows Media с использованием указанного URL-адреса.

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

## <a name="remarks"></a>Remarks

этот метод запускает проигрыватель Windows Media с указанным URL-адресом, установленным в качестве текущего элемента мультимедиа. Если проигрыватель был ранее закрыт в режиме обложки, он будет открыт с использованием обложки, последней выбранной пользователем. В противном случае проигрыватель откроется в полноэкранном режиме.

если этот метод вызывается из элемента управления Windows Media плайерактивекс, внедренного в удаленный режим, его поведение идентично *плайераппликатион*. метод **свитчтоплайераппликатион** .

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Плайераппликатион. Свитчтоплайераппликатион**](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





