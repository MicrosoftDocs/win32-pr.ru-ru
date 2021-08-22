---
title: Ивмплибрари, метод тождественности
description: Метод «идентичен» возвращает значение, указывающее, совпадает ли указанный объект с текущим.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- метод проигрыватель Windows Media
- метод проигрыватель Windows Media, интерфейс ивмплибрари
- проигрыватель Windows Media интерфейса ивмплибрари, метод тождественности
topic_type:
- apiref
api_name:
- IWMPLibrary.isIdentical
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0ed37725bbda5b170ece8ce71c12499b42f0b361cbac3bbe65f1b875af06fc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506054"
---
# <a name="iwmplibraryisidentical-method"></a>Метод Ивмплибрари:: одинаковы

Метод « **идентичен** » возвращает значение, указывающее, совпадает ли указанный объект с текущим.

## <a name="syntax"></a>Синтаксис


```CSharp
public System.Boolean isIdentical(
  IWMPLibrary pIWMPLibrary
);
```


```VB

Public Function isIdentical( _
  ByVal pIWMPLibrary As IWMPLibrary _
) As System.Boolean
Implements IWMPLibrary.isIdentical
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*пивмплибрари* \[ окне\]
</dt> <dd>

Интерфейс **вмплиб. ивмплибрари** , представляющий объект для сравнения с текущим объектом.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение **System. Boolean** , которое является результатом сравнения. Значение **true** указывает, что объекты одинаковы.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Интерфейс Ивмплибрари (VB и C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





