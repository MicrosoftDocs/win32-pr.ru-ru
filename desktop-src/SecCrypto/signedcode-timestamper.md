---
description: Свойство отметки времени извлекает Стампер времени подписанного исполняемого файла.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Сигнедкоде. TimeStamp, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5bd6f9376f74d46373f6731c66b2452503c6105fff31ce28b4fc76ac126c44d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118899353"
---
# <a name="signedcodetimestamper-property"></a>Сигнедкоде. TimeStamp, свойство

\[Свойство **метки времени** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Свойство **отметки времени** извлекает Стампер времени подписанного исполняемого файла.

## <a name="syntax"></a>Синтаксис


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a>Значение свойства

Объект- [**подписавший**](signer.md) , предоставляющий доступ к времени Стампер подписанного исполняемого файла.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнедкоде**](signedcode.md)
</dt> </dl>

 

 
