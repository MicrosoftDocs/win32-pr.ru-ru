---
title: Событие Player. Медиаколлектионаттрибутестрингремовед
description: Событие Медиаколлектионаттрибутестрингремовед возникает при удалении значения атрибута из библиотеки. | Событие Player. Медиаколлектионаттрибутестрингремовед
ms.assetid: f1253996-10d1-42fa-89f9-1e52ca830aea
keywords:
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингремовед
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингремовед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионаттрибутестрингремовед
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
ms.openlocfilehash: b1b85dfd566c507f6ae5557134ac95544e42d688
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704070"
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

**Строка** , указывающая имя атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> <dt>

*бстраттрибвал* 
</dt> <dd>

**Строка** , указывающая значение атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

При удалении элемента мультимедиа из библиотеки его метаданные удаляются из объекта **медиаколлектион** , и это событие срабатывает для каждого удаляемого атрибута.

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





