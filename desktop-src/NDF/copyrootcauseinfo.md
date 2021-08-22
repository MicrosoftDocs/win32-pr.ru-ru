---
title: Функция Копируткаусеинфо (Ндаттрибутилс. h)
description: Создает копию структуры Руткаусеинфо.
ms.assetid: 6bcd1341-657a-40c1-bebd-1c0f780ae337
keywords:
- Копируткаусеинфо функция NDF
topic_type:
- apiref
api_name:
- CopyRootCauseInfo
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98bb09fd9a61da536ddd17a4067838b33d4f86ffb8ee29fb404dc861220a5166
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685834"
---
# <a name="copyrootcauseinfo-function"></a>Функция Копируткаусеинфо

Функция **копируткаусеинфо** создает копию структуры [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CopyRootCauseInfo(
  _Out_       RootCauseInfo *Dest,
  _In_  const RootCauseInfo *Source
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Конечный адрес* \[ заполняет\]
</dt> <dd>

Тип: **[ **руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)\***

Обновляемая структура.

</dd> <dt>

*Исходный код* \[ окне\]
</dt> <dd>

Тип: **const [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \***

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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Ндаттрибутилс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





