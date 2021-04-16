---
title: Кдромколлектион. Count
description: Свойство Count извлекает количество доступных компакт-дисков и DVD-дисководов в системе.
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- Проигрыватель Windows Media Кдромколлектион. Count
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
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699177"
---
# <a name="cdromcollectioncount"></a>Кдромколлектион. Count

Свойство **Count** извлекает количество доступных компакт-дисков и DVD-дисководов в системе.

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a>Возможные значения

Это свойство является **числом** только для чтения (**длинное целое**).

## <a name="remarks"></a>Комментарии

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Дисководы DVD-дисков подсчитываются точно так же, как и дисководы компакт-дисков. Однако элемент управления проигрывателя Windows Media поддерживает только функции DVD для операционных систем Windows XP и более поздних версий. Обычно дисководы DVD могут воспроизводить компакт-диски, но дисководы компакт-дисков не могут воспроизводить DVD-носители.

**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда возвращает значение 0.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *кдромколлектион*. **число** , которое показывает число дисков CD и DVD, доступных на компьютере пользователя. Объект Player создан с ИДЕНТИФИКАТОРом "Player".


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Кдромколлектион**](cdromcollection-object.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





