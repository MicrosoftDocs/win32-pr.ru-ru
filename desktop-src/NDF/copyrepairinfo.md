---
title: Функция Копирепаиринфо (Ндаттрибутилс. h)
description: Создает копию структуры Репаиринфо.
ms.assetid: a1147ce6-9a90-4a46-8fe4-da3353391a13
keywords:
- Копирепаиринфо функция NDF
topic_type:
- apiref
api_name:
- CopyRepairInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a054df2b16684840f22295f0c26de6029ef150a97ca8839c98d94713ab030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620439"
---
# <a name="copyrepairinfo-function"></a>Функция Копирепаиринфо

Функция **копирепаиринфо** создает копию структуры [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CopyRepairInfo(
  _Out_       RepairInfo *Dest,
  _In_  const RepairInfo *Source
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Конечный адрес* \[ заполняет\]
</dt> <dd>

Тип: **[ **репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)\***

Обновляемая структура.

</dd> <dt>

*Исходный код* \[ окне\]
</dt> <dd>

Тип: **const [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \***

Существующая копируемая структура.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возможные возвращаемые значения включают, но не ограничиваются следующим.



| Код возврата                                                                                   | Описание                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Операция успешно выполнена.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Один или несколько параметров указаны неправильно.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для выполнения этой операции.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





