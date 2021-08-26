---
title: Network. частота
description: Свойство частота кадров извлекает текущую частоту кадров видео в кадрах за сотни секунд. Например, значение 2998 означает 29,98 кадров в секунду.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- проигрыватель Windows Media Network. частоты кадров
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
ms.openlocfilehash: 4da4a0f292c4693c263115dc1ad59ea3c71946d81838d427e6d8e043ac499709
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901654"
---
# <a name="networkframerate"></a>Network. частота

Свойство **Частота** кадров извлекает текущую частоту кадров видео в кадрах за сотни секунд. Например, значение 2998 означает 29,98 кадров в секунду.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **Частота кадров**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **Частота кадров для вывода** текущей частоты кадров. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FR". Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> <dt>

[**Network. Енкодедфрамерате**](network-encodedframerate.md)
</dt> </dl>

 

 





