---
title: Медиаколлектион. Жетаттрибутестрингколлектион, метод
description: Метод Жетаттрибутестрингколлектион извлекает объект StringCollection, представляющий набор всех значений для указанного атрибута в пределах указанного типа мультимедиа.
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- Жетаттрибутестрингколлектион метод Windows Media Player
- Жетаттрибутестрингколлектион метод Windows Media Player, класс Медиаколлектион
- Класс Медиаколлектион Windows Media Player, метод Жетаттрибутестрингколлектион
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689060"
---
# <a name="mediacollectiongetattributestringcollection-method"></a>Медиаколлектион. Жетаттрибутестрингколлектион, метод

Метод **жетаттрибутестрингколлектион** извлекает объект **StringCollection** , представляющий набор всех значений для указанного атрибута в пределах указанного типа мультимедиа.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*атрибут* \[ окне\]
</dt> <dd>

**Строка** , указывающая атрибут.

</dd> <dt>

*mediaType* \[ окне\]
</dt> <dd>

**Строка** , представляющая тип носителя. Содержит одно из следующих значений: "звук", "видео", "список воспроизведения" или "другое".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает объект **StringCollection** .

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

Дополнительные сведения об атрибутах, поддерживаемых проигрывателем Windows Media, см. в разделе [Справочник по атрибутам](attribute-reference.md) .

## <a name="examples"></a>Примеры

В следующем примере JScript используется *медиаколлектион*. **жетаттрибутестрингколлектион** для вывода списка значений, соответствующих определенному атрибуту для звуковых элементов в коллекции мультимедиа. HTML-элемент SELECT, созданный с помощью ID = "Attribute", позволяет пользователю выбрать атрибут, например исполнитель, жанр или альбом. Элемент TEXTAREA HTML, созданный с помощью ID = "Аттрибутевалс", отображает результат. Объект **Player** создан с идентификатором "Player".


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект Медиаколлектион**](mediacollection-object.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





