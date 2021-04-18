---
title: Медиаколлектион. Remove, метод
description: Метод Remove удаляет элемент из коллекции носителей.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- метод Remove Windows Media Player
- метод Remove Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион проигрыватель Windows Media Player, метод Remove
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685409"
---
# <a name="mediacollectionremove-method"></a>Медиаколлектион. Remove, метод

Метод **Remove** удаляет элемент из коллекции носителей.

## <a name="syntax"></a>Синтаксис


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*элемент* \[ окне\]
</dt> <dd>

Объект **мультимедиа** для удаления.

</dd> <dt>

*Удаление* \[ окне\]
</dt> <dd>

**Логическое значение** , указывающее, следует ли удалить элемент.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Этот метод удаляет элемент из библиотеки. Этот метод не удаляет файлы с компьютера пользователя.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

В следующем примере JScript, после запроса пользователя, окончательно удаляется первый элемент мультимедиа из коллекции мультимедиа с помощью *медиаколлектион*. **Удалить**. Объект **Player** создан с идентификатором "Player".


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Медиаколлектион. Add**](mediacollection-add.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





