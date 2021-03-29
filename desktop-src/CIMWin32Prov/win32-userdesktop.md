---
description: '\_Класс WMI взаимосвязей Win32 усердесктоп связывает учетную запись пользователя и параметры рабочего стола, относящиеся к нему.'
ms.assetid: 5ea83ad6-bd0a-4c16-85b2-e3e61ef05903
ms.tgt_platform: multiple
title: Класс Win32_UserDesktop
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserDesktop
- Win32_UserDesktop.Element
- Win32_UserDesktop.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 39b45ee7859fea9f1068123041a87309cf40c2d2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895590"
---
# <a name="win32_userdesktop-class"></a>\_Класс Win32 усердесктоп

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ усердесктоп** связывает учетную запись пользователя и параметры рабочего стола, относящиеся к нему.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FF-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_UserDesktop : CIM_ElementSetting
{
  Win32_UserAccount REF Element;
  Win32_Desktop     REF Setting;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ усердесктоп** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **Win32 \_ усердесктоп** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ UserAccount**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("элемент"), [**маппингстрингс**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ UserAccount")
</dt> </dl>

Ссылка на экземпляр, представляющий учетную запись пользователя, Рабочий стол которой можно настроить с помощью свойства **Settings** этого класса.

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **\_ классическую панель Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](../wmisdk/key-qualifier.md), [**Переопределение**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Маппингстрингс**](../wmisdk/standard-qualifiers.md) ("Инструментарий WMI \| Win32 \_ Desktop")
</dt> </dl>

Ссылка на экземпляр, представляющий параметры рабочего стола, которые служат для настройки конкретной учетной записи пользователя.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Класс **Win32 \_ усердесктоп** является производным от [**CIM \_ елементсеттинг**](cim-elementsetting.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ЕЛЕМЕНТСЕТТИНГ CIM**](cim-elementsetting.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
