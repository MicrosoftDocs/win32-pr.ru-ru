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
ms.openlocfilehash: 3a35362876c067de011ec69a858e20150308cbd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897390"
---
# <a name="rkeyclosekeyservice-function"></a>Функция Ркэйклосекэйсервице

Функция **ркэйклосекэйсервице** не поддерживается.

**Windows Server 2003:** Функция **ркэйклосекэйсервице** закрывает маркер службы ключа, Открытый с помощью предыдущего вызова функции [**ркэйопенкэйсервице**](rkeyopenkeyservice.md) . Обратите внимание, что это поведение изменилось в Windows Server 2003 с пакетом обновления 1 (SP1).

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
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Ркэйсвкк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ркэйопенкэйсервице**](rkeyopenkeyservice.md)
</dt> <dt>

[**ркэйпфксинсталл**](rkeypfxinstall.md)
</dt> </dl>

 

 




