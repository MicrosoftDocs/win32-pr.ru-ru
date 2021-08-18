---
description: Возвращает маркер для хеша подтверждения.
ms.assetid: c0f20084-c863-42cf-afdf-298c5a96eed9
title: Функция Сслхашхандшаке (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslHashHandshake
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 5a21bdb3fd655e5c3b39249937f04a4122c64e6c6176c0d39ae1164e48863edb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906102"
---
# <a name="sslhashhandshake-function"></a>Функция Сслхашхандшаке

Функция **сслхашхандшаке** возвращает маркер для хеша подтверждения.

## <a name="syntax"></a>Синтаксис


```C++
SECURITY_STATUS WINAPI SslHashHandshake(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _Inout_ NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_   PBYTE              pbInput,
  _In_    DWORD              cbInput,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсслпровидер* \[ окне\]
</dt> <dd>

Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*ххандшакехаш* \[ в, out\]
</dt> <dd>

Маркер для хэш-объекта.

</dd> <dt>

*пбинпут* \[ заполняет\]
</dt> <dd>

Адрес буфера, содержащего данные для хэширования.

</dd> <dt>

*кбинпут* \[ окне\]
</dt> <dd>

Размер (в байтах) буфера *пбинпут* .

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Этот параметр зарезервирован для использования в будущем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает ноль.

## <a name="remarks"></a>Remarks

Функция **сслхашхандшаке** является одной из трех функций, используемых для создания хэша, используемого во время подтверждения SSL.

1.  Для получения обработчика хэша вызывается функция [**сслкреатехандшакехаш**](sslcreatehandshakehash.md) .
2.  Функция **сслхашхандшаке** вызывается любое количество раз с обработчиком хэша для добавления данных в хэш.
3.  Функция [**сслкомпутефинишедхаш**](sslcomputefinishedhash.md) вызывается с хэш-маркером для получения дайджеста хэшированных данных.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Сслпровидер. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

