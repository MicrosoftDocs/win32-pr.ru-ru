---
description: Этот класс представляет связь между операционной системой и параметрами Autochk, которые применяются к дискам на компьютере. Обратите внимание, что этот параметр связан с операционной системой, а не с компьютерной системой, так как на компьютере может быть установлена одна или несколько операционных систем, каждая из которых имеет собственные параметры Autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Класс Win32_OperatingSystemAutochkSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cfa6e90828935dda8aa163967985813526042b8800f91cb01825fbd158f8a63d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972544"
---
# <a name="win32_operatingsystemautochksetting-class"></a>\_Класс Win32 оператингсистемауточксеттинг

Этот класс представляет связь между операционной системой и параметрами Autochk, которые применяются к дискам на компьютере. Обратите внимание, что этот параметр связан с операционной системой, а не с компьютерной системой, так как на компьютере может быть установлена одна или несколько операционных систем, каждая из которых имеет собственные параметры Autochk.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ оператингсистемауточксеттинг** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ оператингсистемауточксеттинг** имеет следующие свойства.

<dl> <dt>

**Элемент**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 с \_ операционной** системы
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("элемент"), [**ключ**](../wmisdk/key-qualifier.md)
</dt> </dl>

Подлежит уточнению

</dd> <dt>

**Параметр**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ ауточксеттинг**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("параметр"), [**Key**](../wmisdk/key-qualifier.md)
</dt> </dl>

Подлежит уточнению

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ЕЛЕМЕНТСЕТТИНГ CIM**](cim-elementsetting.md)
</dt> </dl>

 

 
