---
description: Извлекает сведения о наборе шифров для указанного протокола, набора шифров и набора типов ключей.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: Функция СсллукупЦиферсуитеинфо (Сслпровидер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913635"
---
# <a name="ssllookupciphersuiteinfo-function"></a>Функция СсллукупЦиферсуитеинфо

Функция **ссллукупЦиферсуитеинфо** извлекает сведения о наборе шифров для указанного протокола, набора шифров и набора типов ключей.

## <a name="syntax"></a>Синтаксис


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хсслпровидер* \[ окне\]
</dt> <dd>

Обработчик для экземпляра поставщика протокола [*SSL протокола*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*двпротокол* \[ окне\]
</dt> <dd>

Одно из значений [**идентификатора протокола поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .

</dd> <dt>

*двЦиферсуите* \[ окне\]
</dt> <dd>

Один из значений [**идентификаторов комплекта шифров поставщика CNG SSL**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .

</dd> <dt>

*двкэйтипе* \[ окне\]
</dt> <dd>

Одно из значений [**идентификаторов типа ключа поставщика SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .

</dd> <dt>

*пЦиферсуите* \[ заполняет\]
</dt> <dd>

Адрес буфера, содержащего структуру [**\_ \_ \_ набора шифров NCRYPT SSL**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) , в которую записываются сведения о наборе шифров.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Этот параметр зарезервирован для использования в будущем.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если функция завершается с ошибкой, она возвращает ноль.

Если функция завершается ошибкой, она возвращает ненулевое значение ошибки.

Возможные коды возврата включают, но не ограничиваются следующим.



| Возвращаемый код и значение                                                                                                                                                    | Описание                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> Не <dt>**превышать \_ Недопустимый 0x80090026L \_ Handle**</dt> <dt></dt> </dl> | Недопустимый маркер *хсслпровидер* .<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Сслпровидер. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

