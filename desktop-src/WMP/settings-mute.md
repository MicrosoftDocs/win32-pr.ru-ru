---
title: Параметры. выкл.
description: Свойство выкл. указывает и получает значение, указывающее, отключено ли звуковое сопровождение.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Параметры. выключение проигрывателя Windows Media
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704381"
---
# <a name="settingsmute"></a>Параметры. выкл.

Свойство **выкл** . указывает и получает значение, указывающее, отключено ли звуковое сопровождение.

## <a name="syntax"></a>Синтаксис

Player. Settings. выкл.

## <a name="possible-values"></a>Возможные значения

Это свойство является **логическим значением** для чтения и записи.



| Значение | Описание                  |
|-------|------------------------------|
| true  | Звук отключен.              |
| false | По умолчанию. Звук не отключен. |



 

## <a name="examples"></a>Примеры

В следующем примере создается элемент CHECKBOX HTML, позволяющий пользователю отключить звук и снять с него микрофон. Объект **Player** создан с идентификатором "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект параметров**](settings-object.md)
</dt> </dl>

 

 





