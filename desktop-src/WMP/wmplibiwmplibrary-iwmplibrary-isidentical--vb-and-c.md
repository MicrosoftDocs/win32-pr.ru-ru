---
title: Ивмплибрари, метод тождественности
description: Метод «идентичен» возвращает значение, указывающее, совпадает ли указанный объект с текущим.
ms.assetid: c4eebc46-6a5f-4f9a-8cd4-7421b156670c
keywords:
- метод, аналогичный проигрывателю Windows Media
- тождественный метод Windows Media Player, интерфейс Ивмплибрари
- Интерфейс Ивмплибрари Windows Media Player, метод, идентичный
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
ms.openlocfilehash: 53071caa98b8f8e3ccb95e926969926cc68e7860
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708527"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Версия<br/>   | Проигрыватель Windows Media 11.<br/>                                                                                    |
| Пространство имен<br/> | **вмплиб**<br/>                                                                                                  |
| Сборка<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Интерфейс Ивмплибрари (VB и C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





