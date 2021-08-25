---
title: Network. Енкодедфрамерате
description: Свойство Енкодедфрамерате извлекает частоту кадров видео, заданную автором содержимого в кадрах в секунду.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- проигрыватель Windows Media Network. енкодедфрамерате
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f64b6f57b4cfd0e7bc94715f80c1066ebe23a601e64c173926cf2cd9e36393
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901704"
---
# <a name="networkencodedframerate"></a>Network. Енкодедфрамерате

Свойство **енкодедфрамерате** извлекает частоту кадров видео, заданную автором содержимого в кадрах в секунду.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **енкодедфрамерате**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **енкодедфрамерате** для вывода частоты кадров, указанной при кодировании файла. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FR". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
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

[**Network. частота**](network-framerate.md)
</dt> </dl>

 

 





