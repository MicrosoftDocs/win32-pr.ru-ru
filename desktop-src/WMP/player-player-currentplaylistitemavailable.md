---
title: Событие Player. Куррентплайлиститемаваилабле
description: Событие Куррентплайлиститемаваилабле возникает, когда текущий список воспроизведения станет доступным. | Событие Player. Куррентплайлиститемаваилабле
ms.assetid: 4894e2fc-3464-413f-8abf-8b5e91899946
keywords:
- Проигрыватель Windows Media Event Куррентплайлиститемаваилабле
- Проигрыватель Windows Media Event Куррентплайлиститемаваилабле, класс Player
- Класс проигрывателя Windows Media Player, событие Куррентплайлиститемаваилабле
topic_type:
- apiref
api_name:
- Player.CurrentPlaylistItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe5809e50d572cfb8eb7a36220d083ec18a0a76
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704506"
---
# <a name="playercurrentplaylistitemavailable-event"></a>Событие Player. Куррентплайлиститемаваилабле

Событие **куррентплайлиститемаваилабле** возникает, когда текущий список воспроизведения станет доступным.

## <a name="syntax"></a>Синтаксис


```JScript
Player.CurrentPlaylistItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстритемнаме* 
</dt> <dd>

**Строка** , содержащая имя текущего элемента списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Имя текущего списка воспроизведения можно использовать для получения соответствующего объекта **списка воспроизведения** с помощью *плайлистколлектион*. метод **жетбинаме** .

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Плайлистколлектион. Жетбинаме**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





