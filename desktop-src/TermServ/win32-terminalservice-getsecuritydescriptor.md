---
title: Метод Жетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов)
description: Метод Жетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов) — возвращает дескриптор безопасности, который управляет доступом к службе.
ms.assetid: 9898091A-5BE2-42A0-BF81-13AB74696ACB
ms.tgt_platform: multiple
keywords:
- инструментарий управления Windows (WMI) сценариев, безопасность
- инструментарий управления Windows (WMI) безопасности, написание сценариев
- службы удаленных рабочих столов метода Жетсекуритидескриптор
- Службы удаленных рабочих столов метода Жетсекуритидескриптор, класс Win32_Service
- Класс Win32_Service службы удаленных рабочих столов, метод Жетсекуритидескриптор
topic_type:
- apiref
api_name:
- Win32_Service.GetSecurityDescriptor
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea5b8a9b945048f947aa273e1ccc1f4514469681
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090652"
---
# <a name="getsecuritydescriptor-method-of-the-win32_service-class-remote-desktop-services"></a>Метод Жетсекуритидескриптор класса Win32_Service (службы удаленных рабочих столов)

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

Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](/windows/desktop/CIMWin32Prov/win32-baseservice).**Свойство State** ) равно 0, 1 или 2.

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

Неизвестный сбой при запуске службы.

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

Служба не имеет потока выполнения.

</dd> <dt>

**стр**
</dt> <dd>

Служба имеет циклические зависимости при запуске.

</dd> <dt>

**стр**
</dt> <dd>

Служба выполняется с тем же именем.

</dd> <dt>

**20**
</dt> <dd>

Имя службы содержит недопустимые символы.

</dd> <dt>

**открыт**
</dt> <dd>

Службе переданы недопустимые параметры.

</dd> <dt>

**22**
</dt> <dd>

Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.

</dd> <dt>

**23**
</dt> <dd>

Служба существует в базе данных доступных в системе служб.

</dd> <dt>

**24**
</dt> <dd>

Служба в данный момент приостановлена в системе.

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
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Служба Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**\_Терминалсервице Win32**](win32-terminalservice.md)
</dt> <dt>

[**Константы прав доступа**](/windows/desktop/WmiSdk/privilege-constants)
</dt> <dt>

[Объекты дескрипторов безопасности WMI](/windows/desktop/WmiSdk/wmi-security-descriptor-objects)
</dt> <dt>

[Изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects)
</dt> <dt>

[Управление учетными записями пользователей и WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)
</dt> </dl>

 

