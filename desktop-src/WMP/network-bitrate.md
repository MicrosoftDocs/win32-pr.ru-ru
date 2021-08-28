---
title: Network. скорость
description: Свойство скорость получает текущую скорость получения.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- проигрыватель Windows Media Network. скорость
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec142885bdd718903e956f8e86b59c3753cb024ecccc5efb2f8494797ea6a818
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901784"
---
# <a name="networkbitrate"></a>Network. скорость

Свойство **скорость** получает текущую скорость получения.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **скорость**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

Это значение представляет собой сочетание скорости потока для текущих видео-и звуковых потоков.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **скорость** для вывода скорости текущего мультимедиа. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "BR". Объект **Player** создан с идентификатором "Player".


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

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
</dt> </dl>

 

 





