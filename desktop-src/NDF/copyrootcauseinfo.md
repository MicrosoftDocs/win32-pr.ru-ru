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
ms.openlocfilehash: 5093d7af6458668a763aa206cacd22a0526aa521
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988437"
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

Тип: **[**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

Обновляемая структура.

</dd> <dt>

_Source * \[ в\]
</dt> <dd>

Тип: **const [**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) \** _

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

[**руткаусеинфо**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo)
</dt> </dl>

 

 





