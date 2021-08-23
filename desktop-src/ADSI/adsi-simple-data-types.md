---
title: Простые типы данных ADSI (iAds. h)
description: Интерфейсы служб Active Directory (ADSI) определяют и используют следующие простые типы данных.
ms.assetid: 0bd34f13-269f-4f5d-8a18-74577522e402
ms.tgt_platform: multiple
keywords:
- ADS_BOOLEAN
- ADS_CASE_EXACT_STRING
- ADS_CASE_IGNORE_STRING
- ADS_DN_STRING
- ADS_INTEGER
- ADS_LARGE_INTEGER
- ADS_NUMERIC_STRING
- ADS_OBJECT_CLASS
- ADS_PRINTABLE_STRING
- ADS_SEARCH_HANDLE
- ADS_UTC_TIME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 422fc0e20195e576f3ade8b39948992d61a376b58fd22f399ca1009db79cbdb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023702"
---
# <a name="adsi-simple-data-types"></a>Простые типы данных ADSI

Интерфейсы служб Active Directory (ADSI) определяют и используют следующие простые типы данных.


```C++
typedef DWORD ADS_BOOLEAN, *PADS_BOOLEAN;
typedef LPWSTR ADS_CASE_EXACT_STRING, *PADS_CASE_EXACT_STRING;
typedef LPWSTR ADS_CASE_IGNORE_STRING, *PADS_CASE_IGNORE_STRING;
typedef LPWSTR ADS_DN_STRING, *PADS_DN_STRING;
typedef DWORD ADS_INTEGER, *PADS_INTEGER;
typedef LARGE_INTEGER ADS_LARGE_INTEGER, *PADS_LARGE_INTEGER;
typedef LPWSTR ADS_NUMERIC_STRING, *PADS_NUMERIC_STRING;
typedef LPWSTR ADS_OBJECT_CLASS, *PADS_OBJECT_CLASS;
typedef LPWSTR ADS_PRINTABLE_STRING, *PADS_PRINTABLE_STRING;
typedef HANDLE ADS_SEARCH_HANDLE, *PADS_SEARCH_HANDLE;
typedef SYSTEMTIME ADS_UTC_TIME, *PADS_UTC_TIME;
```



<dl> <dt>

**логические БАННЕРы \_**
</dt> <dd>

DWORD

</dd> <dt>

**\_ \_ Точная \_ строка в рекламном случае**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_ \_ строка игнорируемого варианта рекламы \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_строка DN баннера \_**
</dt> <dd>

LPWSTR

</dd> <dt>

**РЕКЛАМное \_ целое**
</dt> <dd>

DWORD

</dd> <dt>

**\_большое \_ целое число ADS**
</dt> <dd>

[**БОЛЬШОЕ \_ целое число**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)

</dd> <dt>

**\_численная \_ строка ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_класс объектов \_ ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_Печатная \_ строка ADS**
</dt> <dd>

LPWSTR

</dd> <dt>

**\_маркер поиска баннеров \_**
</dt> <dd>

HANDLE

</dd> <dt>

**время ADS в \_ формате UTC \_**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)

</dd> </dl>

## <a name="remarks"></a>Remarks

Когда ADSI считывает атрибут, определенный как **целое число** в схеме LDAP, он всегда будет выполнять целое число как 32-разрядное значение и может усечь данные. Это касается только LDAP-серверов, которые допускают произвольный размер целочисленных значений. Если атрибут является пользовательским атрибутом, определенным путем расширения схемы, эту проблему можно избежать, определив настраиваемый атрибут в виде строки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                          |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                    |
| Заголовок<br/>                   | <dl> <dt>IAds. h</dt> </dl> |



 

