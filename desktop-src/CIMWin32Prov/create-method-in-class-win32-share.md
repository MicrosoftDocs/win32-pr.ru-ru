---
description: Инициирует общий доступ к ресурсу сервера.
ms.assetid: 36530e1b-9109-4a6c-bba9-d9358101f5e2
ms.tgt_platform: multiple
title: Метод Create класса Win32_Share
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Share.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d7a74838d9f6c532d3433240a5b8a70846b63776
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990810"
---
# <a name="create-method-of-the-win32_share-class"></a>Метод Create \_ класса общего ресурса Win32

Метод **создания**   [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) инициирует общий доступ для ресурса сервера.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 Create(
  [in]           string                   Path,
  [in]           string                   Name,
  [in]           uint32                   Type,
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] string                   Password,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Путь* \[ окне\]
</dt> <dd>

Локальный путь к общей папке Windows.

Например, "C: \\ Program Files".

</dd> <dt>

*Имя* \[ окне\]
</dt> <dd>

Передает псевдоним в путь, настроенный как общий ресурс в компьютерной системе под Windows.

Например, "Public".

</dd> <dt>

*Тип* \[ окне\]
</dt> <dd>

Передает тип общего ресурса. Типы включают диски, очереди печати, межпроцессные коммуникации (IPC) и общие устройства. Может принимать одно из следующих значений.

<dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

**Дисковый накопитель** (0)


</dt> <dd></dd> <dt>

<span id="Print_Queue"></span><span id="print_queue"></span><span id="PRINT_QUEUE"></span>

**Очередь печати** (1)


</dt> <dd></dd> <dt>

<span id="Device"></span><span id="device"></span><span id="DEVICE"></span>

**Устройство** (2)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (3)


</dt> <dd></dd> <dt>

<span id="Disk_Drive_Admin"></span><span id="disk_drive_admin"></span><span id="DISK_DRIVE_ADMIN"></span>

**Администратор дискового накопителя** (2147483648)


</dt> <dd></dd> <dt>

<span id="Print_Queue_Admin"></span><span id="print_queue_admin"></span><span id="PRINT_QUEUE_ADMIN"></span>

**Администратор очереди печати** (2147483649)


</dt> <dd></dd> <dt>

<span id="Device_Admin"></span><span id="device_admin"></span><span id="DEVICE_ADMIN"></span>

**Администратор устройства** (2147483650)


</dt> <dd></dd> <dt>

<span id="IPC_Admin"></span><span id="ipc_admin"></span><span id="IPC_ADMIN"></span>

**Администратор IPC** (2147483651)


</dt> <dd></dd> </dl> </dd> <dt>

*MaximumAllowed* \[ в необязательное\]
</dt> <dd>

Максимальное количество пользователей, которым разрешено одновременно использовать этот ресурс.

Пример: 10. Это необязательный параметр.

</dd> <dt>

*Описание* \[ в необязательное\]
</dt> <dd>

Необязательный комментарий для описания ресурса, к которому предоставляется общий доступ. Это необязательный параметр.

</dd> <dt>

*Пароль* \[ в необязательное\]
</dt> <dd>

Пароль (если сервер работает с безопасностью на уровне общих ресурсов) для общего ресурса. Если сервер работает с защитой на уровне пользователя, этот параметр игнорируется. Это необязательный параметр.

</dd> <dt>

*Доступ к* \[ в необязательное\]
</dt> <dd>

Дескриптор безопасности для разрешений уровня пользователя. Дескриптор безопасности содержит сведения о разрешениях, владельце и доступе ресурса. Если этот параметр не указан или имеет **значение NULL**, у каждого пользователя есть доступ на чтение к общей папке. Дополнительные сведения см. в разделе [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) и [изменение параметров безопасности доступа для защищаемых объектов](/windows/desktop/WmiSdk/changing-access-security-on-securable-objects).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Отказано в доступе** (2)
</dt> <dt>

**Неизвестный сбой** (8)
</dt> <dt>

**Недопустимое имя** (9)
</dt> <dt>

**Недопустимый уровень** (10)
</dt> <dt>

**Недопустимый параметр** (21)
</dt> <dt>

**Повторяющаяся общая папка** (22)
</dt> <dt>

**Путь перенаправления** (23)
</dt> <dt>

**Неизвестное устройство или каталог** (24)
</dt> <dt>

**Не найдено сетевое имя** (25)
</dt> <dt>

**Другие** (26 4294967295)
</dt> </dl>

## <a name="remarks"></a>Комментарии

**CREATE** является статическим методом.

Только члены локальной группы "Администраторы" или "Операторы учетных записей" могут успешно выполнять инструкцию **CREATE**. Оператор Print может добавлять только очереди принтера. Оператор связи может добавлять только очереди устройств связи.

## <a name="examples"></a>Примеры

В примере [экспорта и импорта общие папки](https://Gallery.TechNet.Microsoft.Com/Export-and-Import-84d4fce1) PowerShell экспортируются и импортируются файловые ресурсы и устанавливаются разрешения для общего ресурса. Аналогичным образом, пример [создания общего доступа и Set Permissions](https://gallery.technet.microsoft.com/scriptcenter/Create-a-Share-and-Set-eb177a79) также создает новый общий ресурс и задает разрешения для общего ресурса.

Следующий код PowerShell создает общую папку.


```PowerShell
# create pointer to class
$comp=[WMICLASS]"Win32_share"

# create a new share
$comp.create("c:\","mynewshare",0)

# see results
gwmi win32_share 
```



Предыдущий пример кода возвращает следующее:

``` syntax
__GENUS          : 2
__CLASS          : __PARAMETERS
__SUPERCLASS     : 
__DYNASTY        : __PARAMETERS
__RELPATH        : 
__PROPERTY_COUNT : 1
__DERIVATION     : {}
__SERVER         : 
__NAMESPACE      : 
__PATH           : 
ReturnValue      : 2
PSComputerName   : 

Name        : ADMIN$
Path        : C:\Windows
Description : Remote Admin

Name        : C$
Path        : C:\
Description : Default share

Name        : CCMLOGS$
Path        : C:\Windows\CCM\Logs
Description : Public Share

Name        : ccmsetup$
Path        : C:\Windows\ccmsetup
Description : Public Share

Name        : Drop
Path        : C:\Drop
Description : 

Name        : IPC$
Path        : 
Description : Remote IPC

Name        : Share
Path        : C:\Share
Description : 
```

В следующем \# образце кода C описывается вызов метода Create.


```CSharp
private static void makeShare(string servername, string filepath, string sharename)
{
try
 {
 // assemble the string so the scope represents the remote server
 string scope = string.Format("\\\\{0}\\root\\cimv2", servername);

 // connect to WMI on the remote server
 ManagementScope ms = new ManagementScope(scope);

 // create a new instance of the Win32_Share WMI object
 ManagementClass cls = new ManagementClass("Win32_Share");

 // set the scope of the new instance to that created above
 cls.Scope = ms;

 // assemble the arguments to be passed to the Create method
 object[] methodargs = { filepath, sharename, "0" };

 // invoke the Create method to create the share
 object result = cls.InvokeMethod("Create", methodargs);
 }
catch (SystemException e)
 {
  Console.WriteLine("Error attempting to create share {0}:", sharename);
  Console.WriteLine(e.Message);
 }

}
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

[**\_Общий ресурс Win32**](win32-share.md)
</dt> </dl>

 

