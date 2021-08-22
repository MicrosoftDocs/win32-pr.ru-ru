---
title: Network. Рецеиведпаккетс
description: Свойство Рецеиведпаккетс Извлекает число полученных пакетов.
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- проигрыватель Windows Media Network. рецеиведпаккетс
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9544332fa6e81211dae45cddc74ce9daee0d47e70d467137aaca2084bbc6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054502"
---
# <a name="networkreceivedpackets"></a>Network. Рецеиведпаккетс

Свойство **рецеиведпаккетс** Извлекает число полученных пакетов.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **рецеиведпаккетс**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

Каждый раз, когда воспроизведение клипа останавливается и перезапускается, это свойство устанавливается в нулевое значение. Он не сбрасывается, если воспроизведение файла приостановлено.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **рецеиведпаккетс** для вывода числа полученных пакетов. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "RP". В примере для обновления экрана используется таймер с интервалом в 1 секунду. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> </dl>

 

 





