---
title: Событие Player. Медиачанже
description: Событие Медиачанже возникает при изменении элемента мультимедиа. | Событие Player. Медиачанже
ms.assetid: c4bdd2ae-c51f-4577-b762-bc84aaf52f76
keywords:
- Проигрыватель Windows Media Event Медиачанже
- Проигрыватель Windows Media Event Медиачанже, класс Player
- Класс проигрывателя Windows Media Player, событие Медиачанже
topic_type:
- apiref
api_name:
- Player.MediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99a63e087356b5d39ae8d751236b8128330c4f3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708487"
---
# <a name="playermediachange-event"></a>Событие Player. Медиачанже

Событие **медиачанже** возникает при изменении элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MediaChange(
  Item
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Элемент* 
</dt> <dd>

Объект **мультимедиа** , представляющий измененный элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript для вывода имени текущего элемента мультимедиа используется элемент HTML DIV с именем MediaName. Код обновляет текст в DIV при каждом возникновении события **медиачанже** . Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for media change. -->
<SCRIPT FOR = "Player" EVENT = "mediaChange(Item)">
   // Test whether a valid currentMedia object exists.
   if (Player.currentMedia){
      // Display the name of the current media item.
      MediaName.innerHTML = Player.currentMedia.name;
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
</dt> </dl>

 

 





