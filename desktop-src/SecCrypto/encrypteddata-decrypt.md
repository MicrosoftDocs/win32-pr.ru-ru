---
description: Расшифровывает зашифрованную и закодированную строку данных.
ms.assetid: 7601083d-0adb-48e1-98a7-804a49f71206
title: Метод EncryptedData. дешифровки
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8bf8a108efdc462a9f08a508a05b736817ec38ce43ee50dbd3fdd11aa2af9f74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766709"
---
# <a name="encrypteddatadecrypt-method"></a>Метод EncryptedData. дешифровки

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Метод **дешифровки** расшифровывает зашифрованную и закодированную строку данных. Результирующие данные в виде открытого текста становятся свойством [**Content**](encrypteddata-content.md) объекта [**EncryptedData**](encrypteddata.md) . Расшифровка содержимого завершается ошибкой, если только секрет, заданный методом [**сетсекрет**](encrypteddata-setsecret.md) , точно совпадает с секретом, используемым для получения ключа, используемого для шифрования содержимого.

## <a name="syntax"></a>Синтаксис


```VB
EncryptedData.Decrypt( _
  ByVal EncryptedMessage _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Енкриптедмессаже* \[ окне\]
</dt> <dd>

Строка, содержащая закодированные зашифрованные данные для расшифровки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Ключ сеанса, полученный из текущего секрета, используется для расшифровки. Этот метод не будет создавать правильный открытый текст, если только текущий секрет не совпадает с секретом, используемым для шифрования сообщения.

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

 

 
