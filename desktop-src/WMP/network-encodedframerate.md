---
title: Network. Енкодедфрамерате
description: Свойство Енкодедфрамерате извлекает частоту кадров видео, заданную автором содержимого в кадрах в секунду.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Проигрыватель Windows Media Network. Енкодедфрамерате
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
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708365"
---
# <a name="networkencodedframerate"></a>Network. Енкодедфрамерате

Свойство **енкодедфрамерате** извлекает частоту кадров видео, заданную автором содержимого в кадрах в секунду.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **енкодедфрамерате**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **енкодедфрамерате** для вывода частоты кадров, указанной при кодировании файла. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FR". Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> <dt>

[**Network. частота**](network-framerate.md)
</dt> </dl>

 

 





