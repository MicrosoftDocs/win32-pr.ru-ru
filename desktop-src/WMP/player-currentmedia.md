---
title: Player. Куррентмедиа
description: Свойство Куррентмедиа указывает или получает текущий объект мультимедиа.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- проигрыватель Windows Media Player. куррентмедиа
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df5e8cd2032d772cbd781d0b45794e86cc19eff7c730a6a963778d54a6f283d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054402"
---
# <a name="playercurrentmedia"></a>Player. Куррентмедиа

Свойство **куррентмедиа** указывает или получает текущий объект мультимедиа.

## <a name="syntax"></a>Синтаксис

*проигрыватель* . **куррентмедиа**

## <a name="possible-values"></a>Возможные значения

Это свойство является объектом мультимедиа для чтения и записи.

## <a name="remarks"></a>Remarks

если *Параметры*. Свойство **автозапуска** имеет значение true, воспроизведение начинается автоматически при установке **куррентмедиа**.

Это свойство принимает объект мультимедиа, который можно получить с помощью *списка воспроизведения*. **элемент**. Чтобы загрузить элемент **мультимедиа** с помощью имени файла, задайте свойство URL-адреса или используйте **невмедиа**.

## <a name="examples"></a>Примеры

в следующем примере JScript извлекается первый элемент мультимедиа из библиотеки. Затем он использует **куррентмедиа** , чтобы сделать полученный элемент мультимедиа текущим элементом мультимедиа, а затем отобразить имя текущего элемента мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Невмедиа**](player-newmedia.md)
</dt> <dt>

[**Список воспроизведения. элемент**](playlist-item.md)
</dt> <dt>

[**Параметры. автозапуск**](settings-autostart.md)
</dt> </dl>

 

 





