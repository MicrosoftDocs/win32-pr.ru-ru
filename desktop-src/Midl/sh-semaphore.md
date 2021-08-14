---
title: Ключевое слово sh_semaphore
description: '\_Ключевое слово \ SH семафор \ указывает, что системный объект является обработчиком семафора.'
keywords:
- sh_semaphore ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a48d0b085f3653679c7399ad0f234e7b7a1ecf1b1532480c003923967ac4830a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383224"
---
# <a name="sh_semaphore-keyword"></a>\_ключевое слово семафора SH

Ключевое слово **\_ семафора SH** указывает, что объект `system_handle` содержит маркер для семафора.

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
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
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
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

[Объекты семафора](../sync/semaphore-objects.md)
</dt> <dt>

[Безопасность объекта синхронизации и права доступа](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Функция **createsemaphore-**](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[Функция **креатесемафорикс**](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
