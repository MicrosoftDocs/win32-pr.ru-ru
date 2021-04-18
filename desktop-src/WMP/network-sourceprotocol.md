---
title: Network. Саурцепротокол
description: Свойство Саурцепротокол получает исходный протокол, используемый для получения данных.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Проигрыватель Windows Media Network. Саурцепротокол
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694816"
---
# <a name="networksourceprotocol"></a>Network. Саурцепротокол

Свойство **саурцепротокол** получает исходный протокол, используемый для получения данных.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **саурцепротокол**

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Комментарии

Это свойство имеет значение "" (пустая строка) при воспроизведении мультимедиа с компакт-диска или DVD-диска.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **саурцепротокол** для вывода исходного протокола, используемого для получения данных. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "SP". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
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

 

 





