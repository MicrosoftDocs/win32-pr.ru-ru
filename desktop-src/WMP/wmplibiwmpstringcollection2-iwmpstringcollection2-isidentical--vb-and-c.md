---
title: IWMPStringCollection2, метод тождественности
description: Метод «идентичен» возвращает значение, указывающее, совпадает ли объект, представленный предоставленным интерфейсом, с текущим.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- метод, аналогичный проигрывателю Windows Media
- тождественный метод Windows Media Player, интерфейс IWMPStringCollection2
- Интерфейс IWMPStringCollection2 Windows Media Player, метод, идентичный
topic_type:
- apiref
api_name:
- IWMPStringCollection2.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bb760dae213f28d44fbc707b4430cb151cfe578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708465"
---
# <a name="iwmpstringcollection2isidentical-method"></a>Метод IWMPStringCollection2:: одинаковы

Метод « **идентичен** » возвращает значение, указывающее, совпадает ли объект, представленный предоставленным интерфейсом, с текущим.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean isIdentical(
  IWMPStringCollection2 pIWMPStringCollection2
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPStringCollection2 As IWMPStringCollection2 _
) As System.Boolean
Implements IWMPStringCollection2.isIdentical
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*pIWMPStringCollection2* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. IWMPStringCollection2** , представляющий объект для сравнения с текущим объектом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , которое является результатом сравнения. Значение **true** указывает, что объекты коллекции строк одинаковы.

## <a name="remarks"></a>Комментарии

Чтобы использовать этот метод, требуется доступ на чтение к библиотеке. Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс IWMPStringCollection2 (VB и C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> </dl>

 

 





