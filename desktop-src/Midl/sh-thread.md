---
title: Ключевое слово sh_thread
description: '\_Ключевое слово \ SH Thread \ указывает, что системный объект является обработчиком потока.'
keywords:
- sh_thread ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_thread keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 5cd3f5458e54ccd266f5ef0920b1cc79e1c0b42e35fac51f7ac353d22409aaa2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641339"
---
# <a name="sh_thread-keyword"></a>\_ключевое слово потока SH

Ключевое слово **\_ потока SH** указывает, что `system_handle` содержит обработчик для потока.

``` syntax
[system_handle(sh_thread)]

[system_handle(sh_thread, access-rights)]
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
    HRESULT SetThread([in, system_handle(sh_process)] HANDLE threadHandle);
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

[Процессы и потоки](../procthread/about-processes-and-threads.md)
</dt> <dt>

[Безопасность потоков и права доступа](../procthread/thread-security-and-access-rights.md)
</dt> <dt>

[Функция **CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)
</dt> <dt>

[Функция **опенсреад**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread)
</dt> </dl>