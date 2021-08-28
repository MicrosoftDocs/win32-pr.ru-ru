---
title: Метод Media. Жетаттрибутенаме
description: Метод Жетаттрибутенаме извлекает имя атрибута, соответствующего указанному индексу.
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- проигрыватель Windows Media метода жетаттрибутенаме
- проигрыватель Windows Media метода жетаттрибутенаме, класс мультимедиа
- класс мультимедиа проигрыватель Windows Media, метод жетаттрибутенаме
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b9a288830283b3711c6e4eb652be968979628af48d2ce5b718150b9018568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123434"
---
# <a name="mediagetattributename-method"></a>Метод Media. Жетаттрибутенаме

Метод **жетаттрибутенаме** извлекает имя атрибута, соответствующего указанному индексу.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее индекс атрибута.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку** , указывающую имя атрибута.

## <a name="remarks"></a>Remarks

Возвращаемое имя атрибута можно использовать в сочетании с **getItemInfo** для получения значения для определенного именованного атрибута.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрыватель Windows Media.

**проигрыватель Windows Media 10 Mobile:** Атрибуты для элемента мультимедиа доступны только во время воспроизведения, если они не извлекаются из элемента через коллекцию мультимедиа.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **жетаттрибутенаме** для заполнения текстовой области HTML с именем myText с индексом и именем каждого атрибута для текущего элемента мультимедиа. Объект **Player** создан с идентификатором "Player".


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Объект мультимедиа**](media-object.md)
</dt> <dt>

[**Media. Аттрибутекаунт**](media-attributecount.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





