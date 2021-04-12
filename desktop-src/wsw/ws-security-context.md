---
title: WS_SECURITY_CONTEXT (WebService. h)
description: Непрозрачный тип, используемый для ссылки на объект контекста безопасности.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136271"
---
# <a name="ws_security_context"></a>\_контекст безопасности \_ WS

Непрозрачный тип, используемый для ссылки на [объект контекста безопасности](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>Комментарии

Этот объект не является потокобезопасным. Дополнительные сведения см. в статье [безопасность потоков](thread-safety.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>WebService. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Контекст безопасности](security-context.md)
</dt> <dt>

[Потокобезопасность](thread-safety.md)
</dt> </dl>

 

 





