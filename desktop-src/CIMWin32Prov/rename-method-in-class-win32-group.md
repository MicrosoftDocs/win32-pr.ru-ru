---
description: Позволяет изменить имя группы.
ms.assetid: 7eb1360e-7416-4a90-abc6-c9a85a114316
ms.tgt_platform: multiple
title: Метод Rename класса Win32_Group
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Group.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c111a0c12d0fdc1ce3f6d6bcaa0e7b0f57831054
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655639"
---
# <a name="rename-method-of-the-win32_group-class"></a>Метод Rename \_ класса группы Win32

Метод **переименования** [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) позволяет изменить имя группы.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Rename(
  [in] string Name
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Имя учетной записи пользователя Windows в домене, указанном свойством **domain** данного класса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод **Rename** может возвращать коды ошибок, перечисленные в следующем списке. Для целочисленных значений, отличных от перечисленных, см. [ \_ коды возврата WMI](/windows/desktop/WmiSdk/wmi-return-codes).

<dl> <dt>

**Успешно**
</dt> <dd>

0

Успешно.

</dd> <dt>

**Экземпляр не найден**
</dt> <dd>

1

</dd> <dt>

**Требуется экземпляр**
</dt> <dd>

2

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

3

</dd> <dt>

**Группа не найдена**
</dt> <dd>

4

</dd> <dt>

**Домен не найден**
</dt> <dd>

5

</dd> <dt>

**Операция разрешена только на основном контроллере домена**
</dt> <dd>

6

</dd> <dt>

**Операция не разрешена для указанных специальных групп. пользователь, администратор, локальный или гость.**
</dt> <dd>

7

</dd> <dt>

**Другая ошибка API**
</dt> <dd>

8

</dd> <dt>

**Внутренняя ошибка**
</dt> <dd>

9

</dd> </dl>

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

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**\_Группа Win32**](win32-group.md)
</dt> <dt>

[**\_Логикалфилесекуритисеттинг Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting)
</dt> </dl>

 

