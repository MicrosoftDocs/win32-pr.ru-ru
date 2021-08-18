---
title: OP_CERT_PFX_STORE
description: Определение OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 28e8b9e1a6d73f3d93e1700f812b21a0edf21982b7d5b9c927f4e7391b961850
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911544"
---
# <a name="op_cert_pfx_store-structure"></a>Структура OP_CERT_PFX_STORE

Содержит сериализованную структуру PFX.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a>Члены

### <a name="ptemplatename"></a>птемплатенаме

Необходимо задать имя шаблона сертификата, используемого для создания сертификата.

### <a name="ulprivatekeyexportpolicy"></a>улприватекэйекспортполици

Содержит одно значение из перечисления [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .

### <a name="ppolicyserverurl"></a>пполицисерверурл

Необходимо задать URL-адрес сервера политики.

### <a name="ulpolicyserverurlflags"></a>улполицисерверурлфлагс

Содержит одно значение из перечисления [**полицисерверурлфлагс**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .

### <a name="ppolicyserverid"></a>пполицисерверид

Содержит строку, однозначно идентифицирующую сервер политики.

### <a name="cbpfx"></a>кбпфкс

Содержит размер Ппфкс в байтах.

### <a name="ppfx"></a>ппфкс

Содержит сериализованную структуру PFX (см. [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)
