---
title: Network. Довнлоадпрогресс
description: Свойство Довнлоадпрогресс извлекает процент завершенной загрузки.
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- проигрыватель Windows Media Network. довнлоадпрогресс
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc8d2707cd5fc24129363d53f9ee58fedf7b15c5da4eb5b80f032524ee66c09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901724"
---
# <a name="networkdownloadprogress"></a>Network. Довнлоадпрогресс

Свойство **довнлоадпрогресс** извлекает процент завершенной загрузки.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **довнлоадпрогресс**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

когда элемент управления проигрыватель Windows Media подключается к файлу мультимедиа, который можно воспроизвести и скачать одновременно, свойство **довнлоадпрогресс** возвращает процент общего файла, который был скачан. В настоящее время эта функция поддерживается только на веб-серверах. Следующие форматы файлов можно скачать и воспроизвести одновременно:

-   Advanced Systems Format (ASF)
-   Звуковые файлы в формате WMA
-   Видеофайлы в формате WMV
-   MP3
-   КОДИРОВЩИК
-   WAV
-   Некоторые файлы AVI

Используйте *проигрыватель*. Событие **буферизации** для определения начала и окончания загрузки.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **довнлоадпрогресс** , чтобы отобразить процент завершенной загрузки. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "DP". В примере для обновления экрана используется таймер с интервалом в 1 секунду. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
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

[**Событие проигрывателя. буферизация**](player-player-buffering.md)
</dt> </dl>

 

 





