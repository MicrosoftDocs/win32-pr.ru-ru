---
title: Network. Фрамесскиппед
description: Свойство Фрамесскиппед извлекает общее число кадров, пропущенных во время воспроизведения.
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- проигрыватель Windows Media Network. фрамесскиппед
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
ms.openlocfilehash: 1031585feae5fa2c7fdd9f5fb64bf958e77b8029d502f3e99476024276a652cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901674"
---
# <a name="networkframesskipped"></a>Network. Фрамесскиппед

Свойство **фрамесскиппед** извлекает общее число кадров, пропущенных во время воспроизведения.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **фрамесскиппед**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **фрамесскиппед** для вывода общего числа кадров, пропущенных во время воспроизведения, когда пользователь нажимает кнопку. Сведения отображаются в HTML-элементе DIV, созданном с помощью ID = "FS". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

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

 

 





