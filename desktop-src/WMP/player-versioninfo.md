---
title: Player. versionInfo
description: свойство versionInfo извлекает строковое значение, указывающее версию проигрыватель Windows Media.
ms.assetid: 4b644de2-fcb9-407b-9eea-3eb683a17150
keywords:
- проигрыватель Windows Media Player. versionInfo
topic_type:
- apiref
api_name:
- Player.versionInfo
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2251d610ad8a522155e37c8d416123c9d09faef5da2b4af4da75aeb745940f0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995834"
---
# <a name="playerversioninfo"></a>Player. versionInfo

свойство **versionInfo** извлекает строковое значение, указывающее версию проигрыватель Windows Media.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **versionInfo**

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой** только для чтения в следующем формате: "*X*. 0,0. *Yyyy*"где *X* представляет основной номер версии, а *yyyy* — номер сборки.

## <a name="examples"></a>Примеры

в следующем примере создается HTML-элемент BUTTON, который при нажатии отображает окно сообщения, содержащее сведения о версии для проигрыватель Windows Media. Объект **Player** создан с идентификатором "Player".


```
<INPUT TYPE = "BUTTON"  ID = "VERSION"  VALUE = "Show Version"
    onClick = "
        /* Build the message containing the version info. */
        var message = 'Windows Media Player Version: ';
        message += '\n';
        message += Player.versionInfo;
 
        /* Display the message box. */
        alert(message);
">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> </dl>

 

 





