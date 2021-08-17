---
title: Событие Player. Медиаколлектионаттрибутестрингремовед
description: Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки. | Событие Player. Медиаколлектионаттрибутестрингремовед
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- проигрыватель Windows Media событий медиаколлектионаттрибутестрингремовед
- проигрыватель Windows Media событий медиаколлектионаттрибутестрингремовед, класс Player
- класс проигрывателя проигрыватель Windows Media, событие медиаколлектионаттрибутестрингремовед
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringRemoved
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b89e46d4dbe86f185fb636b5c8de453e2addbf83c92d1231b5f067ce0b3b1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747410"
---
# <a name="playermediacollectionattributestringremoved-event"></a>Событие Player. Медиаколлектионаттрибутестрингремовед

Событие **медиаколлектионаттрибутестрингремовед** возникает при удалении значения атрибута из библиотеки.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MediaCollectionAttributeStringRemoved(
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

При удалении элемента мультимедиа из библиотеки его метаданные удаляются из объекта **медиаколлектион** , и это событие срабатывает для каждого удаляемого атрибута.

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





