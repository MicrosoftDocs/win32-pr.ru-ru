---
description: Запускает отладчик, зарегистрированный в данный момент для этого процесса.
ms.assetid: 63c30db8-6117-4353-9132-4f39c72a6637
ms.tgt_platform: multiple
title: Метод Аттачдебугжер класса Win32_Process
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.AttachDebugger
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 86ec5e31afef484733381d94bfdfa48595401d963443c2ab407ee6166d5d0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959173"
---
# <a name="attachdebugger-method-of-the-win32_process-class"></a>Метод Аттачдебугжер \_ класса процесса Win32

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) аттачдебугжер запускает отладчик, который в настоящее время зарегистрирован для этого процесса.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 AttachDebugger();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение**
</dt> <dd>

0

Успешное завершение.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

У пользователя нет доступа к запрошенной информации.

</dd> <dt>

**Недостаточно привилегий**
</dt> <dd>

3

У пользователя недостаточно прав.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

8

Неизвестный сбой.

</dd> <dt>

**Путь не найден**
</dt> <dd>

9

Указанный путь не существует.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

21

Указан недопустимый параметр.

</dd> <dt>

**Другое**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



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

[**\_Процесс Win32**](win32-process.md)
</dt> </dl>

 

