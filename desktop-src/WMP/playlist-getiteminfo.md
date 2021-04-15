---
title: Метод списка воспроизведения. getItemInfo
description: Метод getItemInfo извлекает значение атрибута списка воспроизведения.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- getItemInfo метод Windows Media Player
- getItemInfo метод Windows Media Player, класс списка воспроизведения
- Класс списка воспроизведения проигрыватель Windows Media Player, метод getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647949"
---
# <a name="playlistgetiteminfo-method"></a>Метод списка воспроизведения. getItemInfo

Метод **getItemInfo** извлекает значение атрибута списка воспроизведения.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя извлекаемого атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

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

[**Список воспроизведения. Сетитеминфо**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





