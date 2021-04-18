---
title: Network. Лостпаккетс
description: Свойство Лостпаккетс Извлекает число потерянных пакетов.
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- Проигрыватель Windows Media Network. Лостпаккетс
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648758"
---
# <a name="networklostpackets"></a>Network. Лостпаккетс

Свойство **лостпаккетс** Извлекает число потерянных пакетов.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **лостпаккетс**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Это свойство допустимо только для потоковой передачи мультимедиа и будет равняться нулю при использовании протокола HTTP, который бездействует без потерь.

Пакеты могут быть потеряны по ряду причин, например типу и качеству сетевого подключения.

Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство устанавливается в нулевое значение. Он не сбрасывается, если воспроизведение приостановлено и перезапущено. Это свойство возвращает действительные сведения только во время выполнения и только в случае, если *проигрыватель*. Задано свойство **URL-адреса** .

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **лостпаккетс** для вывода общего числа пакетов, потерянных во время воспроизведения, когда пользователь нажимает кнопку. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "LP". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

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

 

 





