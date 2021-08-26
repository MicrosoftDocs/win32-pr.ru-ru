---
title: Network. Буфферингтиме
description: Свойство Буфферингтиме указывает или получает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.
ms.assetid: b52b7f44-6be1-4299-94da-c37d758795af
keywords:
- проигрыватель Windows Media Network. буфферингтиме
topic_type:
- apiref
api_name:
- Network.bufferingTime
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afe4a68a7ad1ae8a1444f1e2f31ad09461e05d221e8fceae52960bd5927aac0c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901734"
---
# <a name="networkbufferingtime"></a>Network. Буфферингтиме

Свойство **буфферингтиме** указывает или получает время (в миллисекундах), выделенное для буферизации входящих данных перед началом воспроизведения.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *сеть*. **буфферингтиме**

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** для чтения и записи (**длинное**) в диапазоне от нуля до 60 000 со значением по умолчанию 5 000.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *сеть*. **буфферингтиме** , чтобы указать количество секунд, выделенных для буферизации входящих данных. Сведения извлекаются из HTML-элемента ввода текста, созданного с помощью ID = "Буфтекст". Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Create a BUTTON element to change the bufferingTime value. -->
<INPUT TYPE = "BUTTON" NAME = "bufTime" ID = "bufTime" 
       VALUE = "Change Buffer Time"

    onClick = "
       /* Test whether the user entered a valid value. */
       if (bufText.value >= 0 & bufText.value <= 60) 
           Player.network.bufferingTime = bufText.value * 1000;
       else
           alert('Buffering time must be between 0 and 60.');
">

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

 

 





