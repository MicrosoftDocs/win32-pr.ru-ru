---
title: Медиаколлектион. isDeleted, метод
description: Метод IsDeleted извлекает значение, указывающее, находится ли указанный элемент мультимедиа в папке удаленных элементов.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- метод IsDeleted Windows Media Player
- метод IsDeleted Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод isDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685410"
---
# <a name="mediacollectionisdeleted-method"></a>Медиаколлектион. isDeleted, метод

Метод **IsDeleted** извлекает значение, указывающее, находится ли указанный элемент мультимедиа в папке удаленных элементов.

## <a name="syntax"></a>Синтаксис


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*элемент* \[ окне\]
</dt> <dd>

Объект **мультимедиа** , который может быть удален.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение**.

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Этот метод всегда возвращает **значение false**.

## <a name="examples"></a>Примеры

В следующем примере JScript используется *медиаколлектион*. **удаляется, чтобы проверить** , находится ли конкретный элемент мультимедиа, хранящийся в переменной с именем медиаобжект, в папке удаленных элементов. Если элемент мультимедиа еще не был удален, он перемещается в папку Удаленные элементы. Объект **Player** создан с идентификатором "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

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

[**Медиаколлектион. Сетделетед**](mediacollection-setdeleted.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





