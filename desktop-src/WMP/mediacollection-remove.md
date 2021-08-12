---
title: Медиаколлектион. Remove, метод
description: Метод Remove удаляет элемент из коллекции носителей.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- удалить метод проигрыватель Windows Media
- метод remove проигрыватель Windows Media, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод remove
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
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574611"
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

## <a name="remarks"></a>Remarks

Этот метод удаляет элемент из библиотеки. Этот метод не удаляет файлы с компьютера пользователя.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем JScript примере после запроса пользователя окончательно удаляется первый элемент мультимедиа из коллекции мультимедиа с помощью *медиаколлектион*. **Удалить**. Объект **Player** создан с идентификатором "Player".


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
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Медиаколлектион. Add**](mediacollection-add.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





