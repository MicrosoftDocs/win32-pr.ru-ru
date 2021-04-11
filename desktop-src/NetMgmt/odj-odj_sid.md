---
title: ODJ_SID
description: Определение ODJ_SID IDL
ms.assetid: 1d06f725-6cd4-42cf-b171-c78a095690cb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: dd51f2e8a54eaf5be566e5a25f013ca1d87b9341
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104070811"
---
# <a name="odj_sid-structure"></a>Структура ODJ_SID

Содержит идентификатор безопасности (SID).

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _ODJ_SID
{
    UCHAR Revision;
    UCHAR SubAuthorityCount;
    SID_IDENTIFIER_AUTHORITY IdentifierAuthority;
    [size_is(SubAuthorityCount)] ULONG SubAuthority[*];
}   ODJ_SID, *PODJ_SID;
```

## <a name="members"></a>Члены

### <a name="revision"></a>Редакция

Необходимо задать версию идентификатора SID.

### <a name="subauthoritycount"></a>субаусоритикаунт

Необходимо задать число элементов в подавторе.

### <a name="identifierauthority"></a>идентифиераусорити

Необходимо задать идентификатор центра безопасности.

### <a name="subauthority"></a>Подавтор

Должен содержать массив вложенных центров SID.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_ \_ центр идентификации SID \_ ODJ**](odj-sid_identifier_authority.md)
