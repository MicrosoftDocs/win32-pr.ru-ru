---
description: Возвращает число объектов ExtendedProperty в коллекции.
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: Расширенных свойств. Count, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c34aa63da5276c573d5c3f260d5d7a5956045813695991756ede6c9f69be29ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007272"
---
# <a name="extendedpropertiescount-property"></a>Расширенных свойств. Count, свойство

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте службы вызова платформы (PInvoke) для вызова функции Win32 API [**цертжетцертификатеконтекстпроперти**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) и получения свойств. Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода. [.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]

Свойство **Count** извлекает количество объектов [**ExtendedProperty**](extendedproperty.md) в коллекции.

## <a name="syntax"></a>Синтаксис


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a>Значение свойства

Число объектов [**ExtendedProperty**](extendedproperty.md) в коллекции.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
