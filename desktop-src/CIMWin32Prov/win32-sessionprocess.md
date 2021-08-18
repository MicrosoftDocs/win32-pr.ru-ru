---
description: '\_Класс WMI взаимосвязей Win32 сессионпроцесс представляет связь между сеансом входа и процессами, связанными с этим сеансом.'
ms.assetid: 19d4ecf9-27b5-4a0b-9c76-7d10679aaf5e
ms.tgt_platform: multiple
title: Класс Win32_SessionProcess
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SessionProcess
- Win32_SessionProcess.Antecedent
- Win32_SessionProcess.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f31473cf1efa0310669523f0481b58d8b54036f738a69191f19a0a52d804eb05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416819"
---
# <a name="win32_sessionprocess-class"></a>\_Класс Win32 сессионпроцесс

[Класс WMI](../wmisdk/retrieving-a-class.md) взаимосвязей **Win32 \_ сессионпроцесс** представляет связь между сеансом входа и процессами, связанными с этим сеансом.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства. Свойства и методы имеют алфавитный порядок, а не порядок MOF.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("9CD8E1CE-0D27-4a41-AADE-F8D200230FF4"), AMENDMENT]
class Win32_SessionProcess : Win32_SessionResource
{
  Win32_LogonSession REF Antecedent;
  Win32_Process      REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ сессионпроцесс** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **Win32 \_ сессионпроцесс** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **Win32 \_ LogonSession**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) ("Antecedent"), [**ключ**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ LogonSession Win32**](win32-logonsessionmappeddisk.md) , представляющий сеанс, связанный с процессом.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ процесс Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**Переопределение**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**ключ**](../wmisdk/key-qualifier.md)
</dt> </dl>

[**\_ Процесс Win32**](win32-processor.md) , представляющий процесс, связанный с сеансом.

</dd> </dl>

## <a name="remarks"></a>Remarks

**Win32 \_ Сессионпроцесс** возвращает все сеансы для администратора при входе в систему с повышенными правами или при удаленном запуске. Это расширение поведения класса.

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

[**\_Сессионресаурце Win32**](win32-sessionresource.md)
</dt> <dt>

[Классы операционной системы](./operating-system-classes.md)
</dt> </dl>

 

 
