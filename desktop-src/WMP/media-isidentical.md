---
title: Метод Media. одинаковы
description: Метод «идентичен» получает значение, указывающее, совпадает ли указанный объект с текущим. | Метод Media. одинаковы
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- метод, аналогичный проигрывателю Windows Media
- тождественный метод Windows Media Player, класс мультимедиа
- Класс мультимедиа проигрыватель Windows Media Player, метод тождественности
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
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695152"
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

В следующем примере JScript используется *носитель*. **идентично** , чтобы проверить, совпадает ли элемент мультимедиа с именем невмедиа с текущим элементом мультимедиа. Если они не совпадают, будет воспроизведен новый элемент мультимедиа. В противном случае текущий носитель продолжит воспроизводиться без прерывания. Объект **Player** создан с идентификатором "Player".


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
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
</dt> </dl>

 

 





