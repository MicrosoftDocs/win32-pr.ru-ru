---
title: Медиаколлектион. Жетбяусор, метод
description: Метод Жетбяусор извлекает список воспроизведения элементов мультимедиа по указанному автору.
ms.assetid: 8f9b3ee3-a809-4d24-81ce-adad63e5347c
keywords:
- проигрыватель Windows Media метода жетбяусор
- проигрыватель Windows Media метода жетбяусор, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод жетбяусор
topic_type:
- apiref
api_name:
- MediaCollection.getByAuthor
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87989d38d49ff87ce26b7394f4ee79ef4bd7197cd0e35dcd5316797df401ba49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574631"
---
# <a name="mediacollectiongetbyauthor-method"></a>Медиаколлектион. Жетбяусор, метод

Метод **жетбяусор** извлекает список воспроизведения элементов мультимедиа по указанному автору.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getByAuthor(
  author
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Автор* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя автора.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **списка воспроизведения** .

## <a name="remarks"></a>Remarks

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *медиаколлектион*. **жетбяусор** для получения списка воспроизведения элементов мультимедиа. Список воспроизведения содержит элементы, соответствующие автору, указанному пользователем в HTML-элементе input TEXT с именем GetText. Объект **Player** создан с идентификатором "Player".


```JScript
<!-- Use an HTML BUTTON element to create the playlist and play the media items. -->
<INPUT TYPE = "BUTTON"  NAME = "PlayAuthor"  
       ID = "PlayAuthor"  
       VALUE = "Play Author"

onClick = "
    /* Retrieve the author name text from the user. */
    var author = GetAuthor.value;

    /* Create the playlist by using getByAuthor. */
    var pl = Player.mediaCollection.getByAuthor(Author);

    /* Make the new playlist the current playlist. */
    Player.currentPlaylist = pl;

    /* Play the media items in the new playlist. */
               Player.controls.play();
">

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





