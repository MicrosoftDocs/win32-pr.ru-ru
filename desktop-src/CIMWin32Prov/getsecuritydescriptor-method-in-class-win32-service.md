---
description: Метод Жетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32) — возвращает дескриптор безопасности, который управляет доступом к службе.
ms.assetid: 99c8346e-e8d6-4f3c-bbdc-437dcf852b2a
ms.tgt_platform: multiple
title: Метод Жетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.GetSecurityDescriptor
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 44c19f22cf57a811a7caebfbcc9bf4202c8d2ad7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096992"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Метод Жетсекуритидескриптор класса Win32_Service (поставщики WMI CIMWin32)

Метод **жетсекуритидескриптор** возвращает дескриптор безопасности, который управляет доступом к службе. Дескриптор возвращается в виде экземпляра [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetSecurityDescriptor(
  [out] Win32_SecurityDescriptor Descriptor
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дескриптор* \[ заполняет\]
</dt> <dd>

Дескриптор безопасности, связанный со службой.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно**
</dt> <dd>

0

Запрос принят.

</dd> <dt>


</dt> <dd>

1

Запрос не поддерживается.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

У пользователя нет необходимых прав доступа.

</dd> <dt>


</dt> <dd>

3

Службу нельзя остановить, так как от нее зависят другие работающие службы.

</dd> <dt>


</dt> <dd>

4

Запрошенный управляющий код недопустим или неприемлем для данной службы.

</dd> <dt>


</dt> <dd>

5

Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.

</dd> <dt>


</dt> <dd>

6

Служба не запущена.

</dd> <dt>


</dt> <dd>

7

Служба не ответила на запрос запуска за отведенное время.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

8

Неизвестный сбой при запуске службы.

</dd> <dt>

**Отсутствует привилегия**
</dt> <dd>

9

Не найден путь к каталогу исполняемого файла службы.

</dd> <dt>


</dt> <dd>

10

Служба уже запущена.

</dd> <dt>


</dt> <dd>

11

База данных для добавления новой службы заблокирована.

</dd> <dt>


</dt> <dd>

12

Зависимость, от которой зависит эта служба, удалена из системы.

</dd> <dt>


</dt> <dd>

13

Этой службе не удалось найти службу, которая необходима зависимой службе.

</dd> <dt>


</dt> <dd>

14

Эта служба была отключена в системе.

</dd> <dt>


</dt> <dd>

15

Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.

</dd> <dt>


</dt> <dd>

16

Эта служба удаляется из системы.

</dd> <dt>


</dt> <dd>

17

Служба не имеет потока выполнения.

</dd> <dt>


</dt> <dd>

18

Служба имеет циклические зависимости при запуске.

</dd> <dt>


</dt> <dd>

19

Служба выполняется с тем же именем.

</dd> <dt>


</dt> <dd>

20

Имя службы содержит недопустимые символы.

</dd> <dt>

**недопустимый параметр.**
</dt> <dd>

21

Службе переданы недопустимые параметры.

</dd> <dt>


</dt> <dd>

22

Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.

</dd> <dt>


</dt> <dd>

23

Служба существует в базе данных доступных в системе служб.

</dd> <dt>


</dt> <dd>

24

Служба в данный момент приостановлена в системе.

</dd> <dt>

**Другое**
</dt> <dd>

22 4294967295

</dd> </dl>

## <a name="remarks"></a>Remarks

Экземпляр [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) представляет тип данных [**\_ \_ элемента управления дескриптора безопасности**](/windows/desktop/SecAuthZ/security-descriptor-control) и содержит [*список управления доступом на уровне пользователей*](/windows/desktop/SecGloss/d-gly) (DACL) и [*системный список управления доступом*](/windows/desktop/SecGloss/s-gly) (SACL). Дополнительные сведения см. в разделе [списки управления доступом](/windows/desktop/SecAuthZ/access-control-lists).

Если параметр **SeSecurityPrivilege** не предоставлен или не включен при получении дескриптора безопасности, в возвращенном дескрипторе безопасности возвращается только список DACL. Дополнительные сведения см. в статьях [**константы прав**](/windows/desktop/WmiSdk/privilege-constants) и [выполнение привилегированных операций](/windows/desktop/WmiSdk/executing-privileged-operations).

## <a name="examples"></a>Примеры

При получении дескриптора безопасности в VBScript обязательно выполните команду "безопасность" и запустите от имени администратора, как показано в следующем фрагменте кода. В противном случае код может вызвать ошибку разрешений.


```VB
Set objWMIService = GetObject("winmgmts:" _
  & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")
```



Аналогичным образом в VB.NET обязательно установите значение "Енаблепривилежес = true" и запустите приложение от имени администратора.


```VB
Scope = New ManagementScope([String].Format("\\{0}\root\CIMV2", ComputerName), Nothing)
Scope.Options.EnablePrivileges = True
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Служба Win32**](win32-service.md)
</dt> <dt>

[**Константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Управление учетными записями пользователей и WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

