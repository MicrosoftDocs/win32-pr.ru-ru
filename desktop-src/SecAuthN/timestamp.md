---
description: Тип данных TimeStamp содержит сведения о допустимости времени маркеров безопасности. Формат значения типа данных TimeStamp совпадает со значением структуры FILETIME.
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: Метка времени (SSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647275"
---
# <a name="timestamp"></a>TimeStamp

Тип данных **timestamp** содержит сведения о допустимости времени маркеров безопасности. Формат значения типа данных **timestamp** совпадает со значением структуры [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) .


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>SSPI. h (включая Security. h)</dt> </dl> |



 

 
