---
title: Событие Player. Плайлистколлектионплайлистаддед
description: Событие Плайлистколлектионплайлистаддед возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения. | Событие Player. Плайлистколлектионплайлистаддед
ms.assetid: 07acb5e6-d832-4f0b-a6bb-2b7ba27c368d
keywords:
- Проигрыватель Windows Media Event Плайлистколлектионплайлистаддед
- Проигрыватель Windows Media Event Плайлистколлектионплайлистаддед, класс Player
- Класс проигрывателя Windows Media Player, событие Плайлистколлектионплайлистаддед
topic_type:
- apiref
api_name:
- Player.PlaylistCollectionPlaylistAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e6a229aff95d29ae93433dab538521d88c50c1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704533"
---
# <a name="playerplaylistcollectionplaylistadded-event"></a>Событие Player. Плайлистколлектионплайлистаддед

Событие **плайлистколлектионплайлистаддед** возникает при добавлении списка воспроизведения в коллекцию списков воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Player.PlaylistCollectionPlaylistAdded(
  bstrPlaylistName
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрплайлистнаме* 
</dt> <dd>

**Строка** , указывающая имя добавленного списка воспроизведения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Имя добавленного списка воспроизведения можно использовать для получения соответствующего объекта **списка воспроизведения** с помощью *плайлистколлектион*. метод **жетбинаме** .

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

[**Плайлистколлектион. Жетбинаме**](playlistcollection-getbyname.md)
</dt> </dl>

 

 





