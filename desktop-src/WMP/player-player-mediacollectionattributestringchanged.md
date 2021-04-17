---
title: Событие Player. Медиаколлектионаттрибутестрингчанжед
description: Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке. | Событие Player. Медиаколлектионаттрибутестрингчанжед
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингчанжед
- Проигрыватель Windows Media Event Медиаколлектионаттрибутестрингчанжед, класс Player
- Класс проигрывателя Windows Media Player, событие Медиаколлектионаттрибутестрингчанжед
topic_type:
- apiref
api_name:
- Player.MediaCollectionAttributeStringChanged
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92eba7f0f585b9bbff7a8eb52ab13ec0d74aaa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704210"
---
# <a name="playermediacollectionattributestringchanged-event"></a>Событие Player. Медиаколлектионаттрибутестрингчанжед

Событие **медиаколлектионаттрибутестрингчанжед** возникает при изменении значения атрибута в библиотеке.

## <a name="syntax"></a>Синтаксис


```JScript
Player.MediaCollectionAttributeStringChanged(
  bstrAttribName,
  bstrOldAttribVal,
  bstrNewAttribVal
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бстраттрибнаме* 
</dt> <dd>

**Строка** , указывающая имя атрибута. Сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрывателя Windows Media.

</dd> <dt>

*бстролдаттрибвал* 
</dt> <dd>

**Строка** , указывающая старое значение атрибута.

</dd> <dt>

*бстрневаттрибвал* 
</dt> <dd>

**Строка** , указывающая новое значение атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Это событие не возвращает значение.

## <a name="remarks"></a>Комментарии

Когда пользователь изменяет метаданные библиотеки, объект **медиаколлектион** обновляется, и это событие срабатывает для каждого измененного атрибута.

Значение параметров события указывается проигрывателем Windows Media, доступ к которому можно получить или передать в метод в импортированном файле JScript с использованием имени параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**Проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





