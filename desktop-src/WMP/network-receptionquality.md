---
title: Network. Рецептионкуалити
description: Свойство Рецептионкуалити извлекает процент полученных пакетов за последние 30 секунд.
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- Проигрыватель Windows Media Network. Рецептионкуалити
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698916"
---
# <a name="networkreceptionquality"></a>Network. Рецептионкуалити

Свойство **рецептионкуалити** извлекает процент полученных пакетов за последние 30 секунд.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **рецептионкуалити**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Количество пакетов, полученных, потерянных и восстановленных во время потоковой передачи, отслеживается каждую секунду. **рецептионкуалити** — процент пакетов, которые не были потеряны за последние 30 секунд.

Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение. Если воспроизведение приостановлено, оно не сбрасывается.

Это свойство возвращает действительные сведения только во время выполнения и только в случае, если *проигрыватель*. Также задано свойство **URL-адреса** .

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **рецептионкуалити** , чтобы отобразить процент полученных пакетов. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "РК". В примере для обновления экрана используется таймер с 30-секундным интервалом. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
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

 

 





