---
title: IWMPStringCollection2 Жетаттрибутекаунтбитипе, метод
description: Метод Жетаттрибутекаунтбитипе возвращает число атрибутов, связанных с указанным индексом коллекции строк, именем атрибута и языком.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- проигрыватель Windows Media метода жетаттрибутекаунтбитипе
- проигрыватель Windows Media метода жетаттрибутекаунтбитипе, интерфейс IWMPStringCollection2
- проигрыватель Windows Media интерфейса IWMPStringCollection2, метод жетаттрибутекаунтбитипе
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c236d03cad0612d8306b8ccde370136cb9b31acca82e0aa52761ed56fb4b9bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330918"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>Метод IWMPStringCollection2:: Жетаттрибутекаунтбитипе

Метод **жетаттрибутекаунтбитипе** возвращает число атрибутов, связанных с указанным индексом коллекции строк, именем атрибута и языком.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*лколлектиониндекс* \[ окне\]
</dt> <dd>

Значение **System. Int32** , указывающее Отсчитываемый от нуля индекс элемента коллекции строк, из которого необходимо получить атрибут.

</dd> <dt>

*бстртипе* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем атрибута.

</dd> <dt>

*бстрлангуаже* \[ окне\]
</dt> <dd>

**Строка System. String** , которая является именем языка. Если задано значение null или строка нулевой длины (""), используется текущая строка языкового стандарта. В противном случае значение должно быть допустимой строкой языка RFC 1766, например "en-US".

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Int32** , которое является счетчиком.

## <a name="remarks"></a>Remarks

Этот метод используется для определения количества атрибутов, соответствующих определенному имени атрибута для данного элемента **StringCollection** . Номера индексов можно передать в четвертый параметр метода **жетитеминфобитипе** .

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPStringCollection2 (VB и C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. Жетитеминфобитипе (VB и C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





