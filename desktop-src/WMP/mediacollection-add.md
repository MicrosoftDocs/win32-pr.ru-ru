---
title: Медиаколлектион. Add, метод
description: Метод Add добавляет новый элемент мультимедиа или список воспроизведения в библиотеку. | Медиаколлектион. Add, метод
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- Добавление метода Windows Media Player
- Добавление метода Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион проигрыватель Windows Media Player, метод Add
topic_type:
- apiref
api_name:
- MediaCollection.add
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7731a42c8e1317355b129acb6921676c0a33f4a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689064"
---
# <a name="mediacollectionadd-method"></a>Медиаколлектион. Add, метод

Метод **Add** добавляет новый элемент мультимедиа или список воспроизведения в библиотеку.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.add(
  path
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*путь* \[ окне\]
</dt> <dd>

**Строка** , содержащая путь.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **мультимедиа** .

## <a name="remarks"></a>Комментарии

Этот метод загружает существующий элемент мультимедиа или список воспроизведения в библиотеку по заданному пути к файлу. Этот метод не перемещает и не изменяет файл. Этот метод завершается ошибкой, если задан недопустимый локальный путь, но перед добавлением в библиотеку цифровые файлы мультимедиа не проверяются на допустимость.

Этот метод принимает как статические, так и автоматические файлы списков воспроизведения. *Плайлистколлектион*. метод **импортплайлист** также можно использовать для добавления статического списка воспроизведения в библиотеку.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

Следующий пример Microsoft JScript добавляет три объекта мультимедиа в коллекцию носителей проигрывателя Windows Media. Объект **Player** создан с идентификатором "Player".


```JScript
// Adding a media object using a website.
Player.mediaCollection.add("https://www.proseware.com/Media/Laure.wma");

// Adding a media object from a local network.
// You must add an escape sequence of a backslash for 
// every original backslash.
Player.mediaCollection.add("\\\\yourservername\\Public\\Jeanne.wma");

// Adding a media object from a file on a local drive.
// Be sure to add appropriate escape sequences.
Player.mediaCollection.add("C:\\WMSDK\\WMPSDK\\docs\\samples\\media\\house.wma");
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Управление списками воспроизведения**](managing-playlists.md)
</dt> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Медиаколлектион. Remove**](mediacollection-remove.md)
</dt> <dt>

[**Плайлистколлектион. Импортплайлист**](playlistcollection-importplaylist.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





