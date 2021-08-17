---
description: Тип данных TimeStamp содержит сведения о допустимости времени маркеров безопасности. Формат значения типа данных TimeStamp совпадает со значением структуры FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Метка времени (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e521818c9001213396c0046b92f8f0bd9727dddfeaf99b2e23b652a48f8ff95d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786369"
---
# <a name="timestamp"></a>TimeStamp

Тип данных **timestamp** содержит сведения о допустимости времени маркеров безопасности. Формат значения типа данных **timestamp** совпадает со значением структуры [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения XP\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (включая Security. h)</dt> </dl> |



 

 
