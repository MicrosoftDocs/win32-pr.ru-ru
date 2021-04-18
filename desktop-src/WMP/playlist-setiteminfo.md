---
title: Метод списка воспроизведения. Сетитеминфо
description: Метод Сетитеминфо задает значение атрибута списка воспроизведения.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- Сетитеминфо метод Windows Media Player
- Сетитеминфо метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод Сетитеминфо
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708616"
---
# <a name="playlistsetiteminfo-method"></a>Метод списка воспроизведения. Сетитеминфо

Метод **сетитеминфо** задает значение атрибута списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута, который необходимо задать. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> <dt>

*значение* \[ окне\]
</dt> <dd>

**Строка** , содержащая новое значение атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Особое использование метода **сетитеминфо** заключается в сортировке элементов списка воспроизведения с помощью атрибута SortAttribute. В следующем примере в JScript выполняется сортировка списка воспроизведения по значениям атрибута Усерластплайедтиме. Список воспроизведения переменных является ссылкой на объект **списка воспроизведения** .


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



Чтобы использовать этот метод, требуется полный доступ к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**Проигрыватель Windows Media 10 Mobile:** Этот метод не поддерживается.

## <a name="examples"></a>Примеры

Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](playlist-attributecount.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Список воспроизведения. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





