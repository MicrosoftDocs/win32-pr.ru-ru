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
ms.openlocfilehash: e575fddd5d869d7670aa3e42bf3f948badd7fd1b24befdf8839045c788e59634
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642654"
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

### <a name="properties"></a>Элемент Property

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Зависимость CIM**](cim-dependency.md)
</dt> </dl>

 

 
