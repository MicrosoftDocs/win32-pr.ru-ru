---
title: Ключевое слово sh_token
description: '\_Ключевое слово \ SH Token \ указывает, что системный объект является маркером маркера.'
keywords:
- sh_token ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_token keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: a33b070af5cd43a095fd6ad45a0dee86f1868171
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719883"
---
# <a name="sh_token-keyword"></a>\_ключевое слово токена SH

Ключевое слово **\_ токена SH** указывает, что `system_handle` содержит маркер маркера.

``` syntax
[system_handle(sh_token)]

[system_handle(sh_token, access-rights)]
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
    HRESULT SetToken([in, system_handle(sh_token)] HANDLE token);

    HRESULT GetToken([out, system_handle(sh_token, TOKEN_QUERY)] HANDLE* pToken);
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

[Маркеры доступа](../secauthz/access-tokens.md)
</dt> <dt>

[Права доступа для объектов Access-Token](../secauthz/access-rights-for-access-token-objects.md)
</dt> </dl>
