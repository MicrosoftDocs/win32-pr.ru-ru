---
title: Ключевое слово sh_mutex
description: '\_Ключевое слово \ SH Mutex \ указывает, что системный объект является обработчиком мьютекса.'
keywords:
- sh_mutex ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a355eb0121875e186a485ee6f7f96519a4fa0cfb1c75c806e1baea895691c914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641369"
---
# <a name="sh_mutex-keyword"></a>\_ключевое слово мьютекса SH

Ключевое слово **\_ мьютекса SH** указывает, что объект `system_handle` содержит маркер для мьютекса.

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a>Параметры

Это ключевое слово является параметром для [**system_handle**](system-handle.md).

В документации по [**system_handle**](system-handle.md) также содержатся сведения о необязательном использовании параметра *Access-Rights* . Поведение по умолчанию `DUPLICATE_SAME_ACCESS` для каждой спецификации [ **функции дупликатехандле**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) .

## <a name="remarks"></a>Remarks

Чтобы использовать это ключевое слово с `system_handle` атрибутом, `-target` необходимо установить для флага значение `NT100` (или более высокий) при выполнении midl.exe.

## <a name="examples"></a>Примеры

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
|-|-|
| Минимальная версия клиента | Windows 10 Годовщина обновления (версия 1607, сборка 14393) |
| Минимальная версия сервера | Windows Server 2016 (сборка 14393) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Мьютексные объекты](../sync/mutex-objects.md)
</dt> <dt>

[Безопасность объекта синхронизации и права доступа](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Функция **CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[Функция **креатемутексекс**](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>