---
description: Пытается поместить службу, управляемую драйвером системы, в состояние возобновления.
ms.assetid: 16bacf06-4236-4d58-9b09-cb86bb73d78a
ms.tgt_platform: multiple
title: Метод ResumeService класса Win32_SystemDriver
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ResumeService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d326fcd0a3bc9801f5e214cdc8740170cf1f1cf8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990422"
---
# <a name="resumeservice-method-of-the-win32_systemdriver-class"></a>Метод ResumeService \_ класса Win32 SystemDriver

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ResumeService пытается поместить службу, управляемую драйвером системы, в состояние возобновления.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ResumeService();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль), если запрос **ResumeService** был принят, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.

<dl> <dt>

**0**
</dt> <dd>

Запрос принят.

</dd> <dt>

**1**
</dt> <dd>

Запрос не поддерживается.

</dd> <dt>

**2**
</dt> <dd>

У пользователя нет необходимых прав доступа.

</dd> <dt>

**3**
</dt> <dd>

Службу нельзя остановить, так как от нее зависят другие работающие службы.

</dd> <dt>

**4**
</dt> <dd>

Запрошенный управляющий код недопустим или неприемлем для данной службы.

</dd> <dt>

**5**
</dt> <dd>

Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.

</dd> <dt>

**6**
</dt> <dd>

Служба не запущена.

</dd> <dt>

**7**
</dt> <dd>

Служба не ответила на запрос запуска за отведенное время.

</dd> <dt>

**8**
</dt> <dd>

При запуске службы произошла неизвестная ошибка.

</dd> <dt>

**9**
</dt> <dd>

Не найден путь к каталогу исполняемого файла службы.

</dd> <dt>

**10**
</dt> <dd>

Служба уже запущена.

</dd> <dt>

**11**
</dt> <dd>

База данных для добавления новой службы заблокирована.

</dd> <dt>

**12**
</dt> <dd>

Зависимость, от которой зависит эта служба, удалена из системы.

</dd> <dt>

**13**
</dt> <dd>

Этой службе не удалось найти службу, которая необходима зависимой службе.

</dd> <dt>

**14**
</dt> <dd>

Эта служба была отключена в системе.

</dd> <dt>

**15**
</dt> <dd>

Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.

</dd> <dt>

**16**
</dt> <dd>

Эта служба удаляется из системы.

</dd> <dt>

**17**
</dt> <dd>

Отсутствует поток исполнения для этой службы.

</dd> <dt>

**стр**
</dt> <dd>

При запуске службы обнаружены циклические зависимости.

</dd> <dt>

**стр**
</dt> <dd>

Служба с таким именем уже запущена.

</dd> <dt>

**20**
</dt> <dd>

В имени службы присутствуют недопустимые символы.

</dd> <dt>

**открыт**
</dt> <dd>

Службе переданы недопустимые параметры.

</dd> <dt>

**22**
</dt> <dd>

Учетная запись, под которой будет запускаться эта служба, недопустима или не имеет разрешений на запуск службы.

</dd> <dt>

**23**
</dt> <dd>

Служба существует в базе данных доступных в системе служб.

</dd> <dt>

**24**
</dt> <dd>

Служба в данный момент приостановлена в системе.

</dd> </dl>

## <a name="examples"></a>Примеры

Следующий код PowerShell пытается возобновить работу службы "класс принтера Microsoft USB".


```PowerShell
$usbPrintDriver = Get-WmiObject -query "SELECT * FROM Win32_SystemDriver WHERE Name = 'usbprint'"
$Return = $usbPrintDriver.ResumeService()
"Resume Service Called. The return value is " + $return.ReturnValue + "."
"To figure out what this means, go look at the docs above this code snippet."
```



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

[**\_SystemDriver Win32**](win32-systemdriver.md)
</dt> </dl>

 

