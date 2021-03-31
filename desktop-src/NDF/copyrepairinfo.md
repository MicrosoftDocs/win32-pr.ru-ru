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
ms.openlocfilehash: 7a24d15ec5a8a69b3c8c40700273ebcb6f32bcfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988436"
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

Тип: **[**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Обновляемая структура.

</dd> <dt>

_Source * \[ в\]
</dt> <dd>

Тип: **const [**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo) \** _

Существующая копируемая структура.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Возможные возвращаемые значения включают, но не ограничиваются следующим.



| Код возврата                                                                                   | Описание                                                                 |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>          | Операция успешно выполнена.<br/>                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Один или несколько параметров указаны неправильно.<br/>          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Недостаточно памяти для выполнения этой операции.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**репаиринфо**](/windows/win32/api/ndattrib/ns-ndattrib-repairinfo)
</dt> </dl>

 

 





