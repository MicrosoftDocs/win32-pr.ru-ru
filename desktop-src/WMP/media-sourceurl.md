---
title: Media. Саурцеурл
description: Свойство Саурцеурл извлекает URL-адрес элемента мультимедиа.
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- проигрыватель Windows Media Media. саурцеурл
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e2f99aeb64a73bcf36e2cbd472aedfa8f509a5073e70792e7b47343a1b37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415954"
---
# <a name="mediasourceurl"></a>Media. Саурцеурл

Свойство **саурцеурл** извлекает URL-адрес элемента мультимедиа.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентмедиа*. саурцеурл

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **саурцеурл** для получения URL-адреса первого элемента мультимедиа в образце списка воспроизведения; затем URL-адрес элемента мультимедиа присваивается свойству **URL-адрес** объекта Player. Объект **Player** создан с идентификатором "Player".


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> </dl>

 

 





