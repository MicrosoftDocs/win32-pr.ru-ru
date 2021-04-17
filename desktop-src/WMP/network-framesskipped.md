---
title: Network. Фрамесскиппед
description: Свойство Фрамесскиппед извлекает общее число кадров, пропущенных во время воспроизведения.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- Проигрыватель Windows Media Network. Фрамесскиппед
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708323"
---
# <a name="networkframesskipped"></a>Network. Фрамесскиппед

Свойство **фрамесскиппед** извлекает общее число кадров, пропущенных во время воспроизведения.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **фрамесскиппед**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="examples"></a>Примеры

В следующем примере JScript используется *Network*. **фрамесскиппед** для вывода общего числа кадров, пропущенных во время воспроизведения, когда пользователь нажимает кнопку. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FS". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

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

 

 





