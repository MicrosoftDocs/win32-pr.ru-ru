---
title: Кдромколлектион. Count
description: Свойство Count извлекает количество доступных компакт-дисков и DVD-дисководов в системе.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- кдромколлектион. count проигрыватель Windows Media
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db279f746640d09fac8b3852773afc27330fc9ca48d59a1470de7d42709e60f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864104"
---
# <a name="cdromcollectioncount"></a>Кдромколлектион. Count

Свойство **Count** извлекает количество доступных компакт-дисков и DVD-дисководов в системе.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Remarks

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Дисководы DVD-дисков подсчитываются точно так же, как и дисководы компакт-дисков. однако элемент управления проигрыватель Windows Media поддерживает только функции DVD для операционных систем Windows XP и более поздних версий. Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.

**проигрыватель Windows Media 10 Mobile:** Этот метод всегда возвращает значение 0.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *кдромколлектион*. **число** , которое показывает число дисков CD и DVD, доступных на компьютере пользователя. Объект Player создан с ИДЕНТИФИКАТОРом "Player".


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





