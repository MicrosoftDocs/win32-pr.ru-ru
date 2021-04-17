---
title: Событие Player. Медиаколлектионаттрибутестрингаддед
description: Событие Медиаколлектионаттрибутестрингаддед возникает при добавлении значения атрибута в библиотеку. | Событие Player. Медиаколлектионаттрибутестрингаддед
ms.assetid: 0a7fd61f-0429-4c1c-8790-d2f0e7f41d44
keywords:
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингаддед
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингаддед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионаттрибутестрингаддед
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
ms.openlocfilehash: 61ec30cf22b36fe97902d6eb6d6949daeb751f8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708486"
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

**Строка** , указывающая имя атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> <dt>

*бстраттрибвал* 
</dt> <dd>

**Строка** , указывающая значение атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

При добавлении элемента мультимедиа в библиотеку его метаданные добавляются в объект **медиаколлектион** , и это событие срабатывает для каждого добавленного атрибута.

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

 

 





