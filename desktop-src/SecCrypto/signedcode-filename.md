---
description: Свойство FileName задает или получает путь к исполняемому файлу. Это свойство по умолчанию.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Сигнедкоде. FileName, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 981ff6e1343f836ef145d1dac8c66b93d7a89c885a04cb2fe024740d7e35a53d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900384"
---
# <a name="signedcodefilename-property"></a>Сигнедкоде. FileName, свойство

\[Свойство **filename** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Свойство **filename** задает или получает путь к исполняемому файлу. Это свойство по умолчанию.

## <a name="syntax"></a>Синтаксис


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a>Значение свойства

Путь к исполняемому файлу.

## <a name="remarks"></a>Remarks

Если значение свойства **filename** изменено, состояние всего объекта [**сигнедкоде**](signedcode.md) сбрасывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**сигнедкоде**](signedcode.md)
</dt> </dl>

 

 
