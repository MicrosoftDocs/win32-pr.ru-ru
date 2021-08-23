---
title: Network. пропускная способность
description: Свойство пропускной способности извлекает текущую пропускную способность клипа.
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- проигрыватель Windows Media сети. пропускная способность
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
ms.openlocfilehash: 40bd97ae2efe7513bc69d308a29356cfc7b141ecc84b816bdc7fad68d79aa785
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616881"
---
# <a name="networkbandwidth"></a>Network. пропускная способность

Свойство **пропускной способности** извлекает текущую пропускную способность клипа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **пропускная способность**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

Это свойство возвращает нуль, если *игрок*. Свойство **URL-адреса** не задано. Это свойство допустимо только для потоковой передачи мультимедиа.

## <a name="examples"></a>Примеры

в следующем примере Microsoft JScript используется *сеть*. **пропускная способность** для вывода текущей пропускной способности носителя. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "BW". Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





