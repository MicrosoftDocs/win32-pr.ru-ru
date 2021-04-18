---
title: Ключевое слово sh_reg_key
description: '\_ \_ Ключевое слово \ SH reg Key \ указывает, что системный объект является маркером раздела реестра.'
keywords:
- sh_reg_key ключевого слова MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/06/2021
ms.locfileid: "105719886"
---
# <a name="sh_reg_key-keyword"></a>\_ \_ ключевое слово реестра SH reg

Ключевое слово **sh \_ reg \_ Key** указывает, что `system_handle` содержит маркер раздела реестра.

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
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
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
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

[Реестр](../sysinfo/registry.md)
</dt> <dt>

[Безопасность раздела реестра и права доступа](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[Функция **RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
