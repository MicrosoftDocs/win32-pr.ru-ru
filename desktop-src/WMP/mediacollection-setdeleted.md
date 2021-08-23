---
title: Медиаколлектион. Сетделетед, метод
description: Метод Сетделетед перемещает указанный элемент мультимедиа в папку Удаленные элементы. | Медиаколлектион. Сетделетед, метод
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- проигрыватель Windows Media метода сетделетед
- проигрыватель Windows Media метода сетделетед, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод сетделетед
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
ms.openlocfilehash: 63dcb4c0062acbd5f457cd09b9c1370ff9c4f7683fd8758a4a64ce5f510a6948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647844"
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

## <a name="remarks"></a>Remarks

Этот метод не удаляет файлы с компьютера пользователя.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *медиаколлектион*. **сетделетед** переместить определенный элемент мультимедиа, хранящийся в переменной с именем медиаобжект, в папку Удаленные элементы. *Медиаколлектион*. метод **IsDeleted** сначала проверяет, был ли уже удален элемент. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0, проигрыватель Windows Media версии 7,1 или проигрыватель Windows Media для Windows XP. этот метод не поддерживается для ряда проигрыватель Windows Media 9 или более поздних версий.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Медиаколлектион. isDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





