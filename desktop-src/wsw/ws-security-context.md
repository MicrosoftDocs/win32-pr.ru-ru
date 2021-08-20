---
title: WS_SECURITY_CONTEXT (WebService. h)
description: Непрозрачный тип, используемый для ссылки на объект контекста безопасности.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c34f201c40e3079a3c26ced97e2664679f04ccec6b7804844dd305422abadfdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192360"
---
# <a name="ws_security_context"></a>\_контекст безопасности \_ WS

Непрозрачный тип, используемый для ссылки на [объект контекста безопасности](security-context.md).


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a>Remarks

Этот объект не является потокобезопасным. Дополнительные сведения см. в статье [безопасность потоков](thread-safety.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[приложения UWP для классических приложений Windows 7 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для настольных приложений Server 2008 R2 \|\]<br/>                           |
| Header<br/>                   | <dl> <dt>WebService. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Контекст безопасности](security-context.md)
</dt> <dt>

[Потокобезопасность](thread-safety.md)
</dt> </dl>

 

 





