---
title: StringCollection. Жетаттрибутекаунтбитипе, метод
description: Метод Жетаттрибутекаунтбитипе извлекает количество атрибутов, связанных с указанным индексом элемента StringCollection, именем атрибута и языком.
ms.assetid: 3671b7b7-d6d4-4049-8710-d0f34c740b1e
keywords:
- проигрыватель Windows Media метода жетаттрибутекаунтбитипе
- проигрыватель Windows Media метода жетаттрибутекаунтбитипе, класс StringCollection
- класс StringCollection проигрыватель Windows Media, метод жетаттрибутекаунтбитипе
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
ms.openlocfilehash: 2e10f88a3b8e4847588ff8f7f924333c6649e59c362b3296b54ef8b83368b7af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832431"
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

## <a name="remarks"></a>Remarks

Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для конкретного элемента **StringCollection** . Номера индексов можно передать в четвертый параметр метода **StringCollection. жетитеминфобитипе** .

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------|
| Версия<br/> | проигрыватель Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Объект StringCollection**](stringcollection-object.md)
</dt> </dl>

 

 





