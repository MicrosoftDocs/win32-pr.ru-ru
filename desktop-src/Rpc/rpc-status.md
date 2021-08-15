---
title: RPC_STATUS (Рпкдце. h)
description: Тип данных состояние RPC \_ представляет тип кода состояния, зависящий от платформы.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93cc6f682dbb46b65fc261b738b94e8000f3a77d96c4bd65d1fead4bf8c0e17a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925991"
---
# <a name="rpc_status"></a>\_Состояние RPC

Тип данных **\_ Состояние RPC** представляет тип кода состояния, зависящий от платформы.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Remarks

Тип **\_ состояния RPC** возвращается большинством функций RPC и является частью определения типа функции [**RPC \_ Object \_ инк \_ fn**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Рпкдце. h (включение RPC. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**RPC \_ Object \_ инк \_ fn**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





