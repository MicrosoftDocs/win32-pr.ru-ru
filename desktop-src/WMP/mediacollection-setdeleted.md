---
title: Медиаколлектион. Сетделетед, метод
description: Метод Сетделетед перемещает указанный элемент мультимедиа в папку Удаленные элементы. | Медиаколлектион. Сетделетед, метод
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- Сетделетед метод Windows Media Player
- Сетделетед метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Сетделетед
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f545953899883933286f3c38def62d9f254dfdc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685408"
---
# <a name="mediacollectionsetdeleted-method"></a>Медиаколлектион. Сетделетед, метод

Метод **сетделетед** перемещает указанный элемент мультимедиа в папку Удаленные элементы.

## <a name="syntax"></a>Синтаксис


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*элемент* \[ окне\]
</dt> <dd>

Перемещаемый объект **мультимедиа** .

</dd> <dt>

*значение true* \[ окне\]
</dt> <dd>

Всегда указывайте это значение.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод не удаляет файлы с компьютера пользователя.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *медиаколлектион*. **сетделетед** переместить определенный элемент мультимедиа, хранящийся в переменной с именем медиаобжект, в папку Удаленные элементы. *Медиаколлектион*. метод **IsDeleted** сначала проверяет, был ли уже удален элемент. Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0, Windows Media Player версии 7,1 или Windows Media Player для Windows XP. Этот метод не поддерживается для серии проигрывателя Windows Media 9 или более поздней версии.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Медиаколлектион. isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





