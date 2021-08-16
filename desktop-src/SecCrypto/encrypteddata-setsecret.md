---
description: Задает значение секрета, используемого для получения криптографического ключа сеанса, используемого для шифрования и расшифровки данных.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Метод EncryptedData. Сетсекрет
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0e56bd490c4e665d900eb39fb57d09019ab4cfa3b1eb3ad06ad74cb4e83514ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766449"
---
# <a name="encrypteddatasetsecret-method"></a>Метод EncryptedData. Сетсекрет

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Метод **сетсекрет** задает значение секрета, используемого для получения криптографического [*ключа сеанса*](../secgloss/s-gly.md) , используемого для шифрования и расшифровки данных.

## <a name="syntax"></a>Синтаксис


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*неввал* \[ окне\]
</dt> <dd>

Строка, содержащая секрет, используемый для создания криптографического ключа сеанса.

</dd> <dt>

*Секреттипе* \[ в необязательное\]
</dt> <dd>

Значение перечисления [**типа CAPICOM- \_ Secret \_**](capicom-secret-type.md) , указывающее тип секрета, используемого для создания ключа сеанса. Значение по умолчанию — \_ пароль CAPICOM Secret \_ . Этот параметр может иметь следующее значение.



| Значение                                                                                                                                                                                        | Значение                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**\_пароль для секрета CAPICOM \_**</dt> </dl> | Ключ шифрования должен быть производным от пароля.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Секрет используется для создания ключа сеанса для шифрования или расшифровки. Для обеих операций необходимо использовать один и тот же секрет. Если секрет, используемый для шифрования данных, потерян, зашифрованные данные не могут быть расшифрованы.

Если это необходимо для вашего приложения, рассмотрите возможность использования [**криптпротектмемори**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) или [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) для защиты секрета до и после использования. По завершении очистите память, связанную с секретом.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
