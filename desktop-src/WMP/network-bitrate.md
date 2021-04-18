---
title: Network. скорость
description: Свойство скорость получает текущую скорость получения.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Проигрыватель Windows Media с сетевым. скоростью
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
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704220"
---
# <a name="networkbitrate"></a>Network. скорость

Свойство **скорость** получает текущую скорость получения.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **скорость**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Это значение представляет собой сочетание скорости потока для текущих видео-и звуковых потоков.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **скорость** для вывода скорости текущего мультимедиа. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "BR". Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сетевой объект**](network-object.md)
</dt> </dl>

 

 





