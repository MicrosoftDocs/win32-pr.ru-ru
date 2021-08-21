---
title: Событие Player. Куррентитемчанже
description: Событие Куррентитемчанже возникает при изменении Controls. currentItem.
ms.assetid: e6f68aeb-d7e7-460b-adc9-647f28c678a1
keywords:
- проигрыватель Windows Media событий куррентитемчанже
- проигрыватель Windows Media событий куррентитемчанже, класс Player
- класс проигрывателя проигрыватель Windows Media, событие куррентитемчанже
topic_type:
- apiref
api_name:
- Player.CurrentItemChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ed0ca3c8333c7261c8332bcc124c905c5540f5cdf0dbefe3f34f121eb901cc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118338129"
---
# <a name="playercurrentitemchange-event"></a>Событие Player. Куррентитемчанже

Событие **куррентитемчанже** возникает при использовании *элементов управления*. **currentItem** изменения.

## <a name="syntax"></a>Синтаксис


```JScript
Player.CurrentItemChange()
```



## <a name="parameters"></a>Параметры

У этого события нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="examples"></a>Примеры

в следующем примере JScript демонстрируется обработчик событий для *проигрывателя*. событие **куррентитемчанже** . Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an HTML text box to display the media item name. -->
<INPUT TYPE="TEXT" NAME="MEDIA">

<!-- Create an event handler. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player EVENT = currentItemChange()>

   // Display the name of the new media item.
   MEDIA.value = Player.currentMedia.name;

</SCRIPT>
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Controls. currentItem**](controls-currentitem.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





