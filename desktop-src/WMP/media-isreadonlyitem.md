---
title: Метод Media. Исреадонлитем
description: Метод Исреадонлитем возвращает значение, указывающее, можно ли изменять указанный атрибут элемента мультимедиа.
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- проигрыватель Windows Media метода исреадонлитем
- проигрыватель Windows Media метода исреадонлитем, класс мультимедиа
- класс мультимедиа проигрыватель Windows Media, метод исреадонлитем
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 501aacb7b9a56fd9780aba75a15aa9f717640ebff7619df020bad432cdffd459
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123394"
---
# <a name="mediaisreadonlyitem-method"></a>Метод Media. Исреадонлитем

Метод **исреадонлитем** возвращает значение, указывающее, можно ли изменять указанный атрибут элемента мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , указывающая имя атрибута для проверки. дополнительные сведения об атрибутах, поддерживаемых проигрыватель Windows Media, см. в [справочнике по атрибутам](attribute-reference.md)проигрыватель Windows Media.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **логическое значение**.

## <a name="remarks"></a>Remarks

Если атрибут доступен только для чтения, то он не может быть задан с помощью метода **сетитеминфо** . обратите внимание, что этот метод может возвращать различные значения для конкретного атрибута при использовании с разными версиями проигрыватель Windows Media.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

**проигрыватель Windows Media 10 Mobile:** Это свойство всегда возвращает **значение true**.

## <a name="examples"></a>Примеры

в следующем примере JScript используется *носитель*. **исреадонлитем** для заполнения HTML-элемента textarea с именем рвтекст сведениями о текущем элементе мультимедиа. Код выводит каждый атрибут текущего элемента мультимедиа вместе с текстом, указывающим, доступен ли атрибут только для чтения или для чтения и записи. Объект **Player** создан с идентификатором "Player".


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
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

[**Media. Сетитеминфо**](media-setiteminfo.md)
</dt> <dt>

[**Параметры. медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Параметры. рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





