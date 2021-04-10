---
description: '\_Тип данных Handle обработчика SCE является непрозрачным маркером, предоставляемым набором средств настройки безопасности. Он используется в ПФСЦЕ \_ запроса \_ info и \_ \_ функциях поддержки пфсце Set info для передачи информации между вложением и базой данных безопасности.'
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: SCE_HANDLE (Сцесвк. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144437"
---
# <a name="sce_handle"></a>\_обработчик SCE

Тип **данных \_ Handle обработчика SCE** является непрозрачным маркером, предоставляемым набором средств настройки безопасности. Он используется в [**пфсце \_ запроса \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) и функциях поддержки [**пфсце \_ Set \_ info**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) для передачи информации между вложением и базой данных безопасности.


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                         |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                |
| Header<br/>                   | <dl> <dt>Сцесвк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ \_ сведения о запросе пфсце**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[**\_сведения о наборе пфсце \_**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

