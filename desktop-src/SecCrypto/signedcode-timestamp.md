---
description: Создает подпись метки времени Authenticode для подписанного исполняемого файла, указанного в свойстве Сигнедкоде. FileName.
ms.assetid: 8f4c9901-b509-4e4c-82f9-a802b0896a11
title: Сигнедкоде. timestamp, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Timestamp
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b0f4478e4ece5188a96257a8a1dcc9722caa140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688797"
---
# <a name="signedcodetimestamp-method"></a>Сигнедкоде. timestamp, метод

\[Метод **timestamp** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Метод **timestamp** создает подпись метки времени Authenticode для подписанного исполняемого файла, указанного в свойстве **сигнедкоде. filename** . Эта метка времени представляет собой подпись счетчика для подписанного исполняемого файла, которая выполняется центром меток времени.

## <a name="syntax"></a>Синтаксис


```VB
SignedCode.Timestamp( _
  ByVal URL _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*URL-адрес* \[ окне\]
</dt> <dd>

Строка, содержащая URL-адрес сервера отметок времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Отметка времени расширяет допустимость сертификата, проверяя, подписан ли исполняемый файл на время отметки времени.

Перед вызовом этого метода подписанный исполняемый файл должен быть указан в свойстве **сигнедкоде. filename** , а для подписывания исполняемого файла должен быть вызван метод [**сигнедкоде. Sign**](signedcode-sign.md) .

Если подписанный исполняемый файл уже имеет отметку времени, этот метод перезаписывает существующую метку времени.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнедкоде**](signedcode.md)
</dt> </dl>

 

 
