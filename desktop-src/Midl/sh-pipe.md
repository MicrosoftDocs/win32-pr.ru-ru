---
title: Ключевое слово sh_pipe
description: '\_Ключевое слово \ SH pipe \ указывает, что системный объект является маркером канала.'
keywords:
- sh_pipe ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_pipe
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 9f9deab2bf5a751d3b2d5956d4d33a1d5b347e18
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719878"
---
# <a name="sh_pipe-keyword"></a>\_ключевое слово канала SH

Ключевое слово « **\_ канал SH** » указывает, что `system_handle` содержит маркер для канала.

``` syntax
[system_handle(sh_pipe)]

[system_handle(sh_pipe, access-rights)]
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
    HRESULT GetNewPipe([out, system_handle(sh_pipe)] HANDLE* mySidePipe);

    HRESULT PutReadOnlyPipe([in, system_handle(sh_pipe, FILE_GENERIC_READ)] HANDLE theirSidePipe);
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

[О каналах](../ipc/about-pipes.md)
</dt> <dt>

[Безопасность файлов и права доступа](../fileio/file-security-and-access-rights.md)
</dt> <dt>

[Функция **креатепипе**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe)
</dt> <dt>

[Функция **креатенамедпипе**](/windows/win32/api/winbase/nf-winbase-createnamedpipea)
</dt> </dl>
