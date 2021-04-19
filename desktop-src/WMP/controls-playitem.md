---
title: Controls. Плайитем, метод
description: Метод Плайитем воспроизводит указанный элемент мультимедиа. | Controls. Плайитем, метод
ms.assetid: 410e315d-8d5f-4f45-82a7-4249e656c809
keywords:
- Плайитем метод Windows Media Player
- метод Плайитем Windows Media Player, класс Controls
- Класс управляет проигрывателем Windows Media Player, метод Плайитем
topic_type:
- apiref
api_name:
- Controls.playItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9096e378a328f43147a0a94d97034c8e566b611
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699007"
---
# <a name="controlsplayitem-method"></a>Controls. Плайитем, метод

Метод **плайитем** воспроизводит указанный элемент мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
Controls.playItem(
  theMediaItem
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*семедиаитем* \[ окне\]
</dt> <dd>

Объект **мультимедиа** для воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Элемент мультимедиа будет загружаться и воспроизводиться автоматически независимо от значения *параметров*. свойство " **Автозапуск** ". Чтобы загрузить элемент без автоматического воспроизведения, задайте *Параметры*. **Автозапуск** в значение false и назначение значения *проигрывателю*. **URL-адрес**, после которого можно вызвать **Воспроизведение** , чтобы начать воспроизведение элемента.

Примечание

**плайитем** работает только с элементами в *куррентплайлист*. Вызов **плайитем** со ссылкой на сохраненный элемент мультимедиа не поддерживается.

## <a name="examples"></a>Примеры

В следующем примере JScript используется **плайитем** для воспроизведения элемента мультимедиа из текущего списка воспроизведения. Элемент для воспроизведения выбирается в зависимости от его позиции в списке воспроизведения. Объект **Player** создан с идентификатором "Player".


```JScript
// Declare a variable to hold the position of the media item 
// in the current playlist. An arbitrary value is supplied here.
var index = 3

// Retrieve the media item at the fourth position in the current playlist.
var media = Player.currentPlaylist.item(index);

// Play the media item.
Player.controls.playItem(media);

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Controls**](controls-object.md)
</dt> <dt>

[**Список воспроизведения. элемент**](playlist-item.md)
</dt> </dl>

 

 





