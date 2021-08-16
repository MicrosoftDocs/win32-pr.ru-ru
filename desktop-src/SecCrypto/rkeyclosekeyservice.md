---
description: Функция Ркэйклосекэйсервице не поддерживается.
ms.assetid: 3a3d41d4-d8ce-4ed8-a70b-dd3629ab7b44
title: Функция Ркэйклосекэйсервице (Ркэйсвкк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyCloseKeyService
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5c7a075cf4869e350d90e278d009098cf4716d6518b1970c15b8b8264c93cd22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900559"
---
# <a name="rkeyclosekeyservice-function"></a>Функция Ркэйклосекэйсервице

Функция **ркэйклосекэйсервице** не поддерживается.

**Windows Server 2003:** Функция **ркэйклосекэйсервице** закрывает маркер службы ключа, Открытый с помощью предыдущего вызова функции [**ркэйопенкэйсервице**](rkeyopenkeyservice.md) . обратите внимание, что это поведение изменилось с Windows Server 2003 с пакетом обновления 1 (SP1).

## <a name="syntax"></a>Синтаксис


```C++
ULONG RKeyCloseKeyService(
  _In_    KEYSVCC_HANDLE hKeySvcCli,
  _Inout_ void           *pReserved
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хкэйсвккли* \[ окне\]
</dt> <dd>

Обработчик [**\_ обработчика кэйсвкк**](keysvcc-handle.md) , который ранее открывался [**ркэйопенкэйсервице**](rkeyopenkeyservice.md). Это значение не может быть **равно NULL**.

</dd> <dt>

*сохраняется* \[ в, out\]
</dt> <dd>

Зарезервировано. Присвойте этому параметру значение **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция выполнена успешно, возвращается значение S \_ ОК.

Если функция завершается ошибкой, возвращается значение типа **ulong** , указывающее на ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ркэйопенкэйсервице**](rkeyopenkeyservice.md)
</dt> <dt>

[**ркэйпфксинсталл**](rkeypfxinstall.md)
</dt> </dl>

 

 




