---
description: Управляет удаленным доступом к неподдерживаемым версиям Windows.
ms.assetid: eb326bba-a011-4b9c-b4ee-fc08ae364f6f
ms.tgt_platform: multiple
title: Класс __NTLMUser9X
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NTLMUser9X
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2d05920b0936e8ff4de3eb338938e03e92edb4596efbf01f1064b6952a7df661
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320582"
---
# <a name="__ntlmuser9x-class"></a>\_\_Класс NTLMUser9X

класс system **\_ \_ NTLMUser9X** управляет удаленным доступом к неподдерживаемым версиям Windows. Приведенный ниже синтаксис является упрощенной версией кода MOF и включает все унаследованные свойства. Свойства перечислены в алфавитном порядке, а не в MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
class __NTLMUser9X : __SecurityRelatedClass
{
  string Authority;
  sint32 Flags;
  sint32 Mask;
  string Name;
  sint32 Type;
};
```

## <a name="members"></a>Члены

Класс **\_ \_ NTLMUser9X** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **\_ \_ NTLMUser9X** имеет следующие свойства.

<dl> <dt>

**Центр авторизации**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Домен, к которому применяется имя пользователя.

</dd> <dt>

**Флаги**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Флаги наследования.

<dt>

0
</dt> <dd>

Без наследования.

</dd> <dt>

2
</dt> <dd>

Применяется к дочерним пространствам имен в дополнение к текущему.

</dd> </dl>

</dd> <dt>

**Виде**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

битовая маска, указывающая права доступа к пространству имен в репозитории инструментарий управления Windows (WMI) (WMI). Значения битов см. в разделе [**константы прав доступа к пространству имен**](namespace-access-rights-constants.md).

</dd> <dt>

**Имя**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Имя пользователя.

</dd> <dt>

**Тип**
</dt> <dd> <dl> <dt>

Тип данных: **Sint32**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Доступ разрешен.

<dt>

0
</dt> <dd>

Доступ разрешен.

</dd> <dt>

2
</dt> <dd>

Доступ запрещен.

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **\_ \_ NTLMUser9X** используется в качестве входного параметра для методов [**\_ \_ системсекурити:: Get9XUserList**](--systemsecurity-get9xuserlist.md) и [**\_ \_ системсекурити:: Set9XUserList**](--systemsecurity-set9xuserlist.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>       |
| Минимальная версия сервера<br/> | Windows Server 2008<br/> |
| Пространство имен<br/>                | Все пространства имен WMI<br/>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_\_секуритирелатедкласс**](/windows/desktop/WmiSdk/--securityrelatedclass)
</dt> <dt>

[Системные классы WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

