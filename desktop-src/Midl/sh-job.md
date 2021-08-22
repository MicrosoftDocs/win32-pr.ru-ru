---
title: Ключевое слово sh_job
description: '\_Ключевое слово \ SH Job \ указывает, что системный объект является обработчиком задания.'
keywords:
- sh_job ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_job
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: dd71db0310b450db1d9c87879e8ac10ad998d1d21e48a60eb9d816c0a0718b42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146287"
---
# <a name="sh_job-keyword"></a>\_ключевое слово задания SH

Ключевое слово **\_ задания SH** указывает, что `system_handle` содержит обработчик для задания.

``` syntax
[system_handle(sh_job)]

[system_handle(sh_job, access-rights)]
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
    HRESULT SetJob([in, system_handle(sh_job)] HANDLE job);

    HRESULT GetJobForAccounting([out, system_handle(sh_job, JOB_OBJECT_QUERY)] HANDLE* pJob);
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

[Объекты заданий](../procthread/job-objects.md)
</dt> <dt>

[Права доступа и безопасности объекта задания](../procthread/job-object-security-and-access-rights.md)
</dt> <dt>

[Функция **креатежобобжект**](/windows/win32/api/winbase/nf-winbase-createjobobjecta)
</dt> </dl>
