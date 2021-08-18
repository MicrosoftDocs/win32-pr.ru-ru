---
title: Событие Player. Медиаколлектионаттрибутестрингаддед
description: Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку. | Событие Player. Медиаколлектионаттрибутестрингаддед
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- проигрыватель Windows Media событий медиаколлектионаттрибутестрингаддед
- проигрыватель Windows Media событий медиаколлектионаттрибутестрингаддед, класс Player
- класс проигрывателя проигрыватель Windows Media, событие медиаколлектионаттрибутестрингаддед
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringAdded
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d01bd86cb3004cb3f481222f392ba47bd1c47373f55c37ee8f0e7ded57a3d268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995874"
---
# <a name="playermediacollectionattributestringadded-event"></a>Событие Player. Медиаколлектионаттрибутестрингаддед

Событие **медиаколлектионаттрибутестрингаддед** возникает при добавлении значения атрибута в библиотеку.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MediaCollectionAttributeStringAdded(
  bstrAttribName,
  bstrAttribVal
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраттрибнаме* 
</dt> <dd>

**Строка** , указывающая имя атрибута. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибуту](attribute-reference.md)проигрыватель Windows Media.

</dd> <dt>

*бстраттрибвал* 
</dt> <dd>

**Строка** , указывающая значение атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Remarks

При добавлении элемента мультимедиа в библиотеку его метаданные добавляются в объект **медиаколлектион** , и это событие срабатывает для каждого добавленного атрибута.

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





