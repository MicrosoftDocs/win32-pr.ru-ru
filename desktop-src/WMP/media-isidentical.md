---
title: Метод Media. одинаковы
description: Метод «идентичен» получает значение, указывающее, совпадает ли указанный объект с текущим. | Метод Media. одинаковы
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- метод проигрыватель Windows Media
- метод проигрыватель Windows Media, класс мультимедиа
- класс мультимедиа проигрыватель Windows Media, метод, идентичный
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5147d6ccc72d570709ef6ad898bf52872909dc5e3800d9cc671c774510b45d1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054642"
---
# <a name="mediaisidentical-method"></a>Метод Media. одинаковы

Метод « **идентичен** » получает значение, указывающее, совпадает ли указанный объект с текущим.

## <a name="syntax"></a>Синтаксис


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*носитель* \[ окне\]
</dt> <dd>

Объект **мультимедиа** для сравнения с текущим объектом **мультимедиа** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение**.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **идентично** , чтобы проверить, совпадает ли элемент мультимедиа с именем невмедиа с текущим элементом мультимедиа. Если они не совпадают, будет воспроизведен новый элемент мультимедиа. В противном случае текущий носитель продолжит воспроизводиться без прерывания. Объект **Player** создан с идентификатором "Player".


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> </dl>

 

 





