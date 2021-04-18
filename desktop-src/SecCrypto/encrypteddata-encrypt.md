---
description: Извлекает ключ сеанса из секрета и шифрует значение свойства содержимого с помощью этого ключа. Он возвращает зашифрованное содержимое в виде закодированной строки.
ms.assetid: aa6f6e6a-208b-4e9c-b530-08673ab9d794
title: Метод EncryptedData. Encrypt (InfoCard. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Encrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 04d7bf8a337c1bcfa0a024b84304fe50c035f9dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665181"
---
# <a name="encrypteddataencrypt-method"></a>Метод EncryptedData. Encrypt

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Метод **Encrypt** наследует ключ сеанса от секрета и шифрует значение свойства [**Content**](encrypteddata-content.md) с помощью этого ключа. Он возвращает зашифрованное содержимое в виде закодированной строки.

## <a name="syntax"></a>Синтаксис


```VB
EncryptedData.Encrypt( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Енкодингтипе* \[ в необязательное\]
</dt> <dd>

Значение перечисления типа " [**CAPICOM \_ Encoding \_**](capicom-encoding-type.md) ", которое указывает тип кодировки, используемый для кодирования зашифрованных данных. Значение по умолчанию — CAPICOM- \_ кодировать \_ Base64. Этот параметр может принимать одно из указанных ниже значений.



| Значение                                                                                                                                                                                  | Значение                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <dt>**CAPICOM \_ кодирует \_ ANY**</dt> </dl>          | Этот тип кодирования используется только в том случае, если входные данные имеют неизвестный тип кодирования. Если это значение используется для указания типа кодирования вывода, \_ \_ вместо этого будет использоваться CAPICOM-Encoding Base64. Представлено в CAPICOM 2,0.<br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <dt>**CAPICOM \_ кодирует \_ Base64**</dt> </dl> | Данные сохраняются в виде строки в кодировке Base64.<br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <dt>**\_двоичная кодировка CAPICOM \_**</dt> </dl> | Данные сохраняются в виде чисто двоичной последовательности.<br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Строка, содержащая зашифрованные закодированные данные.

## <a name="remarks"></a>Комментарии

Перед вызовом метода **Encrypt** задайте свойство [**Content**](encrypteddata-content.md) и вызовите метод [**сетсекрет**](encrypteddata-setsecret.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| Header<br/>                | <dl> <dt>InfoCard. h</dt> </dl>  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> <dt>

[**EncryptedData**](encrypteddata.md)
</dt> </dl>

 

 
