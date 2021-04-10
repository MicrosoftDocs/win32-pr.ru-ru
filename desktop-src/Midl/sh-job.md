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
ms.openlocfilehash: db24f9dc84f2bb56f57327090485b406ad1a437f
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "103999821"
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

## <a name="remarks"></a>Комментарии

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
| Минимальная версия клиента | Юбилейное обновление Windows 10 (версия 1607, сборка 14393) |
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
