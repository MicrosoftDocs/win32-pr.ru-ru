---
title: Медиаколлектион. Add, метод
description: Метод Add добавляет новый элемент мультимедиа или список воспроизведения в библиотеку. | Медиаколлектион. Add, метод
ms.assetid: 8adf93d1-368b-4916-937f-342901a1592b
keywords:
- добавить проигрыватель Windows Media метода
- добавление метода проигрыватель Windows Media, класс медиаколлектион
- класс медиаколлектион проигрыватель Windows Media, метод add
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
ms.openlocfilehash: 8b26d21f67496f345324efdca93dbf85e59947f1616e0c5620faead2807a6ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647914"
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

## <a name="remarks"></a>Remarks

Этот метод загружает существующий элемент мультимедиа или список воспроизведения в библиотеку по заданному пути к файлу. Этот метод не перемещает и не изменяет файл. Этот метод завершается ошибкой, если задан недопустимый локальный путь, но перед добавлением в библиотеку цифровые файлы мультимедиа не проверяются на допустимость.

Этот метод принимает как статические, так и автоматические файлы списков воспроизведения. *Плайлистколлектион*. метод **импортплайлист** также можно использовать для добавления статического списка воспроизведения в библиотеку.

Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="examples"></a>Примеры

в следующем примере Microsoft JScript в коллекцию носителей проигрыватель Windows Media добавляются три объекта мультимедиа. Объект **Player** создан с идентификатором "Player".


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



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

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

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





