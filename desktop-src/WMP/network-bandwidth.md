---
title: Network. пропускная способность
description: Свойство пропускной способности извлекает текущую пропускную способность клипа.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Проигрыватель Windows Media Network. пропускная способность
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704222"
---
# <a name="networkbandwidth"></a>Network. пропускная способность

Свойство **пропускной способности** извлекает текущую пропускную способность клипа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **пропускная способность**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Это свойство возвращает нуль, если *игрок*. Свойство **URL-адреса** не задано. Это свойство допустимо только для потоковой передачи мультимедиа.

## <a name="examples"></a>Примеры

В следующем примере Microsoft JScript используется *Network*. **пропускная способность** для вывода текущей пропускной способности носителя. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "BW". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

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

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





