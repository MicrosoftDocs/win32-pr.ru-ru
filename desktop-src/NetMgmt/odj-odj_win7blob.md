---
title: ODJ_WIN7BLOB
description: Определение ODJ_WIN7BLOB IDL
ms.assetid: 5802e00c-b943-45d8-8298-5c2b4b996b85
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 2083648636bd58c64314ba22852839f89ed4461d
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104339565"
---
# <a name="odj_win7blob-structure"></a>Структура ODJ_WIN7BLOB

Содержит основные сведения, необходимые для приподключения клиента к домену.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _ODJ_WIN7BLOB
{
    [string] wchar_t *lpDomain;
    [string] wchar_t *lpMachineName;
    [string] wchar_t *lpMachinePassword;
    ODJ_POLICY_DNS_DOMAIN_INFO  DnsDomainInfo;
    DOMAIN_CONTROLLER_INFOW DcInfo;
    DWORD Options;
} ODJ_WIN7BLOB;
```

## <a name="members"></a>Члены

### <a name="lpdomain"></a>лпдомаин

Необходимо задать имя домена.

### <a name="lpmachinename"></a>лпмачиненаме

Необходимо задать имя компьютера.

### <a name="lpmachinepassword"></a>лпмачинепассворд

Необходимо задать пароль открытым текстом для учетной записи компьютера, идентифицируемой Лпмачиненаме

### <a name="dnsdomaininfo"></a>днсдомаининфо

Содержит сведения о присоединенном домене.

### <a name="dcinfo"></a>дЦинфо

Содержит сведения об именовании и адресации контроллера домена, который использовался для создания учетной записи компьютера Active Directory.

### <a name="options"></a>Параметры

Необходимо задать значение 0.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_ \_ \_ сведения о DNS-домене политики \_ ODJ**](odj-odj_policy_dns_domain_info.md)

[**DOMAIN_CONTROLLER_INFOW**](/windows/win32/api/dsgetdc/ns-dsgetdc-domain_controller_infow)



