---
title: IWMPStringCollection2, метод тождественности
description: Метод «идентичен» возвращает значение, указывающее, совпадает ли объект, представленный предоставленным интерфейсом, с текущим.
ms.assetid: 826e7fd8-88f8-4a2a-9ca0-82a500099272
keywords:
- метод проигрыватель Windows Media
- метод проигрыватель Windows Media, интерфейс IWMPStringCollection2
- проигрыватель Windows Media интерфейса IWMPStringCollection2, метод тождественности
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
ms.openlocfilehash: 4576522c1b6d6834ded5e100a2618dcb45204f887420968a5828fdc5c9bd0fef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330908"
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

## <a name="remarks"></a>Remarks

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
</dt> </dl>

 

 





