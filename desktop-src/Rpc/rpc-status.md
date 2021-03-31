---
title: RPC_STATUS (Рпкдце. h)
description: Тип данных состояние RPC \_ представляет тип кода состояния, зависящий от платформы.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071590"
---
# <a name="rpc_status"></a>\_Состояние RPC

Тип данных **\_ Состояние RPC** представляет тип кода состояния, зависящий от платформы.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Комментарии

Тип **\_ состояния RPC** возвращается большинством функций RPC и является частью определения типа функции [**RPC \_ Object \_ инк \_ fn**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                          |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                |
| Заголовок<br/>                   | <dl> <dt>Рпкдце. h (включение RPC. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**RPC \_ Object \_ инк \_ fn**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





