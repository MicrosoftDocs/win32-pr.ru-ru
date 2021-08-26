---
title: Список воспроизведения. attributeName
description: Свойство attributeName извлекает имя атрибута по указанному индексу.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- проигрыватель Windows Media списка воспроизведения. attributeName
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
ms.openlocfilehash: 695e0ee00aca0fe7743a028e0e7830e1839c0b2f89b42a94e9ce1dbe29ef35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003214"
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

## <a name="remarks"></a>Remarks

Число атрибутов извлекается свойством **аттрибутекаунт** . При наличии индекса атрибут **attributeName** возвращает **строку** , которую можно использовать в сочетании с **сетитеминфо** или **getItemInfo** для указания или получения значения атрибута.

Чтобы получить значение этого свойства, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибуту](attribute-reference.md)проигрыватель Windows Media.

Пример кода, в котором используется это свойство, см. в свойстве [аттрибутекаунт](playlist-attributecount.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект списка воспроизведения**](playlist-object.md)
</dt> <dt>

[**Список воспроизведения. Аттрибутекаунт**](playlist-attributecount.md)
</dt> <dt>

[**Список воспроизведения. getItemInfo**](playlist-getiteminfo.md)
</dt> <dt>

[**Список воспроизведения. Сетитеминфо**](playlist-setiteminfo.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





