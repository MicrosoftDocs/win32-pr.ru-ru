---
title: OP_JOINPROV2_PART
description: Определение OP_JOINPROV2_PART IDL
ms.assetid: c220627e-49bd-49f2-a03c-9cdef4b973ca
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f8537b6ca9627a15470115a20f99082dae80e040
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104134758"
---
# <a name="op_joinprov2_part-structure"></a>Структура OP_JOINPROV2_PART

Содержит дополнительные сведения, используемые для настройки клиента, присоединяемого к домену.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_JOINPROV2_PART
{
    DWORD     dwFlags;
    [string] wchar_t *lpNetbiosName;
    [string] wchar_t *lpSiteName;
    [string] wchar_t *lpPrimaryDNSDomain;
    DWORD             dwReserved;
    [string] wchar_t *lpReserved;
} OP_JOINPROV2_PART, *POP_JOINPROV2_PART;
```

## <a name="members"></a>Члены

### <a name="dwflags"></a>dwFlags

Необходимо задать либо ноль, либо одно из следующих значений:

|Значение|Значение|
| --- | --- |
|OP_JP2_FLAG_PERSISTENTSITE (0x00000001)|Сайт, указанный в Лпситенаме, должен считаться постоянным сайтом для клиента.|

### <a name="lpnetbiosname"></a>лпнетбиоснаме

Содержит NetBIOS-имя учетной записи компьютера в формате Юникода.

### <a name="lpsitename"></a>лпситенаме

Содержит имя Active Directory сайта, который должен использовать клиент.

### <a name="lpprimarydnsdomain"></a>лппримариднсдомаин

Содержит первичное доменное имя DNS, которое должен использовать клиент.

### <a name="dwreserved"></a>двресервед

Зарезервировано для будущего использования и должно иметь значение 0.

### <a name="lpreserved"></a>lpReserved

Зарезервировано для будущего использования и должно иметь значение NULL.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)
