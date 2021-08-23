---
title: Медиаколлектион. Жеталл, метод
description: Метод Жеталл извлекает список воспроизведения, содержащий все элементы мультимедиа в библиотеке.
ms.assetid: c22532ee-5714-4762-966f-7dc6543384f4
keywords:
- проигрыватель Windows Media метода жеталл
- проигрыватель Windows Media метода жеталл, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод жеталл
topic_type:
- apiref
api_name:
- MediaCollection.getAll
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1d3bba961f9400470c16e3d773a5765d389ce05bc23c2e948f0b94c7ad22229
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135068"
---
# <a name="mediacollectiongetall-method"></a>Медиаколлектион. Жеталл, метод

Метод **жеталл** извлекает список воспроизведения, содержащий все элементы мультимедиа в библиотеке.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getAll()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **списка воспроизведения** .

## <a name="remarks"></a>Remarks

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере JScript используется *медиаколлектион*. **жеталл** для воспроизведения элементов мультимедиа случайным образом из коллекции носителей. Объект **Player** создан с идентификатором "Player".


```JScript
// Store the count of all media items in the media collection.
var count = Player.mediaCollection.getAll().count;

// Generate a random number using the media count.
var rand = Math.random() * count;

// Round down the random number to the nearest integer.
rand = Math.floor(rand);

// Make the random media item the current media item.
Player.currentMedia = Player.mediaCollection.getAll().item(rand);

// Play the media item.
// Player.controls.play();

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

 

 





