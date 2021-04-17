---
title: StringCollection. Item, метод
description: Метод Item извлекает строку по указанному индексу.
ms.assetid: 5f6afff2-3ecc-4b28-8c67-f859f5440d4f
keywords:
- метод Item проигрыватель Windows Media Player
- метод Item проигрыватель Windows Media, класс StringCollection
- Класс StringCollection Windows Media Player, метод Item
topic_type:
- apiref
api_name:
- StringCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4244ad194ff3426dab81baddc0b7188214e0360
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717775"
---
# <a name="stringcollectionitem-method"></a>StringCollection. Item, метод

Метод **Item** извлекает строку по указанному индексу.

## <a name="syntax"></a>Синтаксис


```JScript
strRetVal = StringCollection.item(
  index
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), содержащее индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **строку**.

## <a name="remarks"></a>Комментарии

Объект **StringCollection** используется для получения набора значений, доступных для атрибута. Например, *медиаколлектион*. метод **жетаттрибутестрингколлектион** можно использовать для получения объекта **StringCollection** , представляющего все значения атрибута жанра в типе мультимедиа. Затем свойство **Item** можно использовать для итерации всех возможных значений атрибута жанра.

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media версии 7,0 или более поздней.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Медиаколлектион. Жетаттрибутестрингколлектион**](mediacollection-getattributestringcollection.md)
</dt> <dt>

[**Settings. Медиаакцессригхтс**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. Рекуестмедиаакцессригхтс**](settings-requestmediaaccessrights.md)
</dt> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





