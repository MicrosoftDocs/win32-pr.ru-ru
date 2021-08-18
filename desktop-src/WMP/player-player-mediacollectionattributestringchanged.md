---
title: Событие Player. Медиаколлектионаттрибутестрингчанжед
description: Событие Медиаколлектионаттрибутестрингчанжед возникает при изменении значения атрибута в библиотеке. | Событие Player. Медиаколлектионаттрибутестрингчанжед
ms.assetid: 9bc81cf2-50a9-41cf-8eff-25c9395dfdac
keywords:
- проигрыватель Windows Media событий медиаколлектионаттрибутестрингчанжед
- проигрыватель Windows Media событий медиаколлектионаттрибутестрингчанжед, класс Player
- класс проигрывателя проигрыватель Windows Media, событие медиаколлектионаттрибутестрингчанжед
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
ms.openlocfilehash: 9435be90761abf88927789fad4380172f0ef6f31427848195d3aa14ea4112cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747400"
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

**Строка** , указывающая имя атрибута. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибуту](attribute-reference.md)проигрыватель Windows Media.

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

## <a name="remarks"></a>Remarks

Когда пользователь изменяет метаданные библиотеки, объект **медиаколлектион** обновляется, и это событие срабатывает для каждого измененного атрибута.

значение параметров события задается проигрыватель Windows Media, и к нему можно получить доступ или передать в метод в импортированном JScriptном файле, используя имя параметра. Имя этого параметра должно быть введено в точности так, как показано, включая прописные буквы.

**проигрыватель Windows Media 10 Mobile:** Это событие не поддерживается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 9 Series или более поздней версии.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Объект Player**](player-object.md)
</dt> <dt>

[**Player. Медиаколлектион**](player-mediacollection.md)
</dt> </dl>

 

 





