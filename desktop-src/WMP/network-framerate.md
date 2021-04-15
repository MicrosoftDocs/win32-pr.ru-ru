---
title: Network. частота
description: Свойство частота кадров извлекает текущую частоту кадров видео в кадрах за сотни секунд. Например, значение 2998 означает 29,98 кадров в секунду.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Проигрыватель Windows Media Network. частоты кадров
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708324"
---
# <a name="networkframerate"></a>Network. частота

Свойство **Частота** кадров извлекает текущую частоту кадров видео в кадрах за сотни секунд. Например, значение 2998 означает 29,98 кадров в секунду.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **Частота кадров**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **Частота кадров для вывода** текущей частоты кадров. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FR". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
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

[**Сетевой объект**](network-object.md)
</dt> <dt>

[**Network. Енкодедфрамерате**](network-encodedframerate.md)
</dt> </dl>

 

 





