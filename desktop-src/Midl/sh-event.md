---
title: Ключевое слово sh_event
description: '\_Ключевое слово \ SH Event \ указывает, что системный объект является обработчиком события.'
keywords:
- sh_event ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: b2f489c27d32c40f80cef326b99131158df92cad2183cee1dc5a3dd74310cf6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013652"
---
# <a name="sh_event-keyword"></a>\_ключевое слово события SH

Ключевое слово **\_ события SH** указывает, что `system_handle` содержит обработчик для события.

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
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
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a>Требования

| &nbsp; | &nbsp; |
|-|-|
| Минимальная версия клиента | Windows 10 Годовщина обновления (версия 1607, сборка 14393) |
| Минимальная версия сервера | Windows Server 2016 (сборка 14393) |

## <a name="see-also"></a>См. также

<dl> <dt>

[**system_handle**](system-handle.md)
</dt> <dt>

[Объекты событий](../sync/event-objects.md)
</dt> <dt>

[Безопасность объекта синхронизации и права доступа](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[Функция **CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[Функция **креативентекс**](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
