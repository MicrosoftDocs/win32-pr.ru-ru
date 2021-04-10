---
description: Переименовывает имя учетной записи пользователя.
ms.assetid: 90258256-7470-4ec8-afce-bea0f64b90fb
ms.tgt_platform: multiple
title: Метод Rename класса Win32_UserAccount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_UserAccount.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 27d495804fb68bc74eda269c2dd7921540f05f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142322"
---
# <a name="rename-method-of-the-win32_useraccount-class"></a>Метод Rename класса Win32 \_ UserAccount

Метод класса **Rename** [WMI](/windows/desktop/WmiSdk/retrieving-a-class) переименовывает имя учетной записи пользователя.

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

Новое имя учетной записи.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно**
</dt> <dd>

0

Успешно.

</dd> <dt>

**Экземпляр не найден**
</dt> <dd>

1

Экземпляр не найден.

</dd> <dt>

**Требуется экземпляр**
</dt> <dd>

2

Требуется экземпляр.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

3

Недопустимый параметр.

</dd> <dt>

**Пользователь не найден**
</dt> <dd>

4

Пользователь не найден.

</dd> <dt>

**Домен не найден**
</dt> <dd>

5

Домен не найден.

</dd> <dt>

**Операция разрешена только на основном контроллере домена**
</dt> <dd>

6

Операция разрешена только на основном контроллере домена.

</dd> <dt>

**Операция не разрешена для последней учетной записи администратора.**
</dt> <dd>

7

</dd> <dt>

**Операция не разрешена для указанных специальных групп. пользователь, администратор, локальный или гость.**
</dt> <dd>

8

Операция запрещена для указанных специальных групп: пользователь, администратор, локальный или гость.

</dd> <dt>

**Другая ошибка API**
</dt> <dd>

9

Другая ошибка API.

</dd> <dt>

**Внутренняя ошибка**
</dt> <dd>

10

Внутренняя ошибка.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Эта функция реализуется как метод для предоставления отдельного контекста для нового имени, которое отличается от значения свойства ключа для имени, связанного с изменяемым экземпляром.

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

[**\_UserAccount Win32**](win32-useraccount.md)
</dt> <dt>

[Классы операционной системы](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

