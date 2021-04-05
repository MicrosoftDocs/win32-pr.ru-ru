---
description: Изменяет режим запуска \_ службы Win32.
ms.assetid: 4fd6a1eb-d2e0-4172-843d-24ae89c5bfcf
ms.tgt_platform: multiple
title: Метод Чанжестартмоде класса Win32_Service (поставщики WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06a4692996354614a685471f98b0243fc1091433
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072433"
---
# <a name="changestartmode-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Метод Чанжестартмоде класса Win32_Service (поставщики WMI CIMWin32)

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) чанжестартмоде изменяет режим запуска [**\_ службы Win32**](win32-service.md).

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*StartMode* \[ окне\]
</dt> <dd>

Режим запуска базовой службы Windows.

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**Запуск загрузки** ("Boot")


</dt> <dd>

Драйвер устройства запущен загрузчиком операционной системы. Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Система** ("System")


</dt> <dd>

Драйвер устройства запущен процессом инициализации операционной системы. Это значение допустимо только для служб драйверов.

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**Автоматический запуск** (автоматический)


</dt> <dd>

Служба запускается автоматически диспетчером управления службами во время запуска системы.

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**Запуск по требованию** (вручную)


</dt> <dd>

Служба, запускаемая диспетчером управления службами, когда процесс вызывает метод [**StartService**](startservice-method-in-class-win32-service.md) .

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Отключено** ("отключено")


</dt> <dd>

Служба, которая больше не может быть запущена.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или любое другое значение, указывающее на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешно**
</dt> <dd>

0

Запрос принят.

</dd> <dt>

**Не поддерживается**
</dt> <dd>

1

Запрос не поддерживается.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

2

У пользователя нет необходимых прав доступа.

</dd> <dt>

**Работающие зависимые службы**
</dt> <dd>

3

Службу нельзя остановить, так как от нее зависят другие работающие службы.

</dd> <dt>

**Недопустимый элемент управления службой**
</dt> <dd>

4

Запрошенный управляющий код недопустим или неприемлем для данной службы.

</dd> <dt>

**Служба не может принять контроль**
</dt> <dd>

5

Запрошенный управляющий код не может быть отправлен в службу, так как это состояние службы ([**Win32 \_ басесервице**](win32-baseservice.md).**Свойство State** ) равно 0, 1 или 2.

</dd> <dt>

**Служба неактивна**
</dt> <dd>

6

Служба не запущена.

</dd> <dt>

**Время ожидания запроса на обслуживание**
</dt> <dd>

7

Служба не ответила на запрос запуска за отведенное время.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

8

Неизвестный сбой при запуске службы.

</dd> <dt>

**Путь не найден**
</dt> <dd>

9

Не найден путь к каталогу исполняемого файла службы.

</dd> <dt>

**Служба уже запущена**
</dt> <dd>

10

Служба уже запущена.

</dd> <dt>

**База данных службы заблокирована**
</dt> <dd>

11

База данных для добавления новой службы заблокирована.

</dd> <dt>

**Зависимость службы удалена**
</dt> <dd>

12

Зависимость, от которой зависит эта служба, удалена из системы.

</dd> <dt>

**Сбой зависимости службы**
</dt> <dd>

13

Этой службе не удалось найти службу, которая необходима зависимой службе.

</dd> <dt>

**Служба отключена**
</dt> <dd>

14

Эта служба была отключена в системе.

</dd> <dt>

**Сбой при входе в службу**
</dt> <dd>

15

Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.

</dd> <dt>

**Служба помечена для удаления**
</dt> <dd>

16

Эта служба удаляется из системы.

</dd> <dt>

**Служба без потока**
</dt> <dd>

17

Служба не имеет потока выполнения.

</dd> <dt>

**Состояние "циклическая зависимость"**
</dt> <dd>

18

Служба имеет циклические зависимости при запуске.

</dd> <dt>

**Состояние "повторяющееся имя"**
</dt> <dd>

19

Служба выполняется с тем же именем.

</dd> <dt>

**Состояние "Недопустимое имя"**
</dt> <dd>

20

Имя службы содержит недопустимые символы.

</dd> <dt>

**Недопустимый параметр Status**
</dt> <dd>

21

Службе переданы недопустимые параметры.

</dd> <dt>

**Недопустимое состояние учетной записи службы**
</dt> <dd>

22

Учетная запись, под которой работает эта служба, либо недопустима, либо не имеет разрешений на запуск службы.

</dd> <dt>

**Служба состояний существует**
</dt> <dd>

23

Служба существует в базе данных доступных в системе служб.

</dd> <dt>

**Служба уже приостановлена**
</dt> <dd>

24

Служба в данный момент приостановлена в системе.

</dd> <dt>

**Другое**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="examples"></a>Примеры

Следующее [изменение StartMode примера службы](https://Gallery.TechNet.Microsoft.Com/6d0f06ed-f840-4228-ad2d-e16ebe6a3aed) PowerShell, извлеченного из коллекции TechNet, изменяет режим запуска службы.


```PowerShell
$wmi = get-wmiobject -class win32_service -namespace root\cimv2 -computername lisbon | 
where-object { $_.name -eq 'bits' } 
 
$rtn = $wmi.changestartmode("manual") 
if($rtn.returnvalue -eq 0) { "success" } 
ELSE 
  { " $($rtn.returnvalue) was reported" }
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

[**\_Служба Win32**](win32-service.md)
</dt> <dt>

[Задачи WMI: службы](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

