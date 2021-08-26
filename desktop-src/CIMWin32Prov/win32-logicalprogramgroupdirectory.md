---
description: '\_класс WMI взаимосвязей Win32 логикалпрограмграупдиректори связывает логические группы программ (группирования в меню) и каталоги файлов, в которых они хранятся.'
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Класс Win32_LogicalProgramGroupDirectory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fa9bf70e82f5a46c8a9a346b33d18e3c9f4a12322ad10a5fca1233df5a36c1d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973314"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>\_Класс Win32 логикалпрограмграупдиректори

[Класс WMI](/windows/desktop/WmiSdk/retrieving-a-class) взаимосвязей **Win32 \_ логикалпрограмграупдиректори** связывает логические группы программ (группирования в меню " **Пуск** ") и каталоги файлов, в которых они хранятся.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ логикалпрограмграупдиректори** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ логикалпрограмграупдиректори** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ логикалпрограмграуп**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ логикалпрограмграуп")
</dt> </dl>

Ссылка на экземпляр, представляющий логическую группу программ.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ Каталог Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**Переопределение**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI- \| \_ Каталог Win32")
</dt> </dl>

Ссылка на экземпляр, представляющий каталог файлов для логической группы программ.

</dd> </dl>

## <a name="remarks"></a>Remarks

Класс **Win32 \_ логикалпрограмграупдиректори** является производным от [**\_ зависимости CIM**](cim-dependency.md).

вызывающий процесс, использующий этот класс, должен иметь привилегию **SE \_ reside \_ NAME** на компьютере, где размещается реестр. Например, если перечислить этот класс на локальном компьютере, учетная запись, под которой выполняется приложение, должна иметь эту привилегию. Дополнительные сведения см. в разделе [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

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

[**\_Зависимость CIM**](cim-dependency.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

