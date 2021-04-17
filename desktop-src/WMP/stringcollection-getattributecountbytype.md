---
title: StringCollection. Жетаттрибутекаунтбитипе, метод
description: Метод Жетаттрибутекаунтбитипе извлекает количество атрибутов, связанных с указанным индексом элемента StringCollection, именем атрибута и языком.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- Жетаттрибутекаунтбитипе метод Windows Media Player
- Жетаттрибутекаунтбитипе метод Windows Media Player, класс StringCollection
- Класс StringCollection Windows Media Player, метод Жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- StringCollection.getAttributeCountByType
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2acf2d7a1f8849f9bd0e83ead3880ca90d2d6149
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717933"
---
# <a name="stringcollectiongetattributecountbytype-method"></a>StringCollection. Жетаттрибутекаунтбитипе, метод

Метод **жетаттрибутекаунтбитипе** извлекает количество атрибутов, связанных с указанным индексом элемента **StringCollection** , именем атрибута и языком.

## <a name="syntax"></a>Синтаксис


```JScript
retVal = StringCollection.getAttributeCountByType(
  index,
  name,
  language
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*индекс* \[ окне\]
</dt> <dd>

**Число** (**Long**), указывающее Отсчитываемый от нуля индекс элемента **StringCollection** , из которого необходимо получить атрибут.

</dd> <dt>

*имя* \[ окне\]
</dt> <dd>

**Строка** , содержащая имя атрибута.

</dd> <dt>

*языковая* \[ окне\]
</dt> <dd>

**Строка** , содержащая язык. Если задано значение null или пустая строка (""), используется текущая строка языкового стандарта. В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **число** (**Long**).

## <a name="remarks"></a>Комментарии

Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для конкретного элемента **StringCollection** . Номера индексов можно передать в четвертый параметр метода **StringCollection. жетитеминфобитипе** .

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | Проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





