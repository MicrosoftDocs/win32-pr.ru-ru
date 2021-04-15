---
description: '\_Ассоциация Подсеансов Win32 определяет связи между сеансами, в которых один сеанс является частью, или использует другой сеанс, например, когда сеанс терминала использует сеанс входа в систему.'
ms.assetid: 2269de22-b086-4f71-8b19-bc53e1c88dc7
ms.tgt_platform: multiple
title: Класс Win32_SubSession
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SubSession
- Win32_SubSession.Antecedent
- Win32_SubSession.Dependent
api_type:
- DllExport
api_location:
- cimwin32.dll
ms.openlocfilehash: 540cfb4c00b5df64e4ff11a1cc462eaed03be434
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539218"
---
# <a name="win32_subsession-class"></a>\_Класс Подсеанса Win32

\_Ассоциация Подсеансов Win32 определяет связи между сеансами, в которых один сеанс является частью, или использует другой сеанс, например, когда сеанс терминала использует сеанс входа в систему.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, AMENDMENT]
class Win32_SubSession : CIM_Dependency
{
  Win32_Session REF Antecedent;
  Win32_Session REF Dependent;
};
```

## <a name="members"></a>Члены

Класс **\_ подсеанса Win32** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **\_ подсеанса Win32** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **\_ сеанс Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) (Antecedent)
</dt> </dl>

[**\_ Сеанс Win32**](win32-session.md) , описывающий сеанс, который имеет вложенный сеанс.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **\_ сеанс Win32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](../wmisdk/standard-qualifiers.md) (зависимый)
</dt> </dl>

[**\_ Сеанс Win32**](win32-session.md) , описывающий сеанс, который является подсеансом.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

 
