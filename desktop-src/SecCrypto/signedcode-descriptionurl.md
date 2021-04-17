---
description: Задает или получает URL-адрес для описания подписанного исполняемого файла.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Сигнедкоде. Дескриптионурл, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685209"
---
# <a name="signedcodedescriptionurl-property"></a>Сигнедкоде. Дескриптионурл, свойство

\[Свойство **дескриптионурл** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Свойство **дескриптионурл** задает или получает URL-адрес для описания подписанного исполняемого файла.

## <a name="syntax"></a>Синтаксис


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a>Значение свойства

URL-адрес описания подписанного исполняемого файла.

## <a name="remarks"></a>Комментарии

**Дескриптионурл** — это URL-адрес, по которому отображается [**Описание**](signedcode-description.md) в диалоговых окнах проверки Authenticode. Если это свойство имеет **значение NULL**, **Описание** не работает как ссылка.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнедкоде**](signedcode.md)
</dt> </dl>

 

 
