---
title: Список воспроизведения. attributeName
description: Свойство attributeName извлекает имя атрибута по указанному индексу.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Проигрыватель Windows Media для списка воспроизведения. attributeName
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704450"
---
# <a name="playlistattributename"></a>Список воспроизведения. attributeName

Свойство **attributeName** извлекает имя атрибута по указанному индексу.

## <a name="syntax"></a>Синтаксис

*проигрыватель*. *куррентплайлист*. **attributeName**( *индекс* )

## <a name="parameters"></a>Параметры

*index*

**Число** (**Long**), содержащее индекс.

## <a name="possible-values"></a>Возможные значения

Это свойство является **строкой**, доступная только для чтения.

## <a name="remarks"></a>Комментарии

Число атрибутов извлекается свойством **аттрибутекаунт** . При наличии индекса атрибут **attributeName** возвращает **строку** , которую можно использовать в сочетании с **сетитеминфо** или **getItemInfo** для указания или получения значения атрибута.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

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

[**Список воспроизведения. Аттрибутекаунт**](playlist-attributecount.md)
</dt> <dt>

[**Список воспроизведения. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Список воспроизведения. Сетитеминфо**](playlist-setiteminfo.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





