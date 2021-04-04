---
description: Пытается отправить в службу определенный пользователем управляющий код.
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Метод Усерконтролсервице класса Win32_BaseService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896366"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a>Метод Усерконтролсервице \_ класса Win32 басесервице

Метод [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) пытается отправить в службу определенный пользователем код элемента управления.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Контролкоде* \[ окне\]
</dt> <dd>

Значение, указывающее команду элемента управления для службы. Например, команда управления является командой "Pause" или "Continue". Значением может быть предопределенный код, а также значение и действие, определяемое службой. Ниже перечислены стандартные управляющие коды.

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**\_продолжение управления \_ службой**


</dt> <dd>

Уведомляет приостановленную службу о возобновлении.

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**\_контроль службы \_ опроса**


</dt> <dd>

Уведомляет службу о текущих сведениях о состоянии диспетчеру управления службами.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**\_нетбиндадд управления \_ службами**


</dt> <dd>

Уведомляет сетевую службу о том, что для привязки существует новый компонент.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**\_нетбинддисабле управления \_ службами**


</dt> <dd>

Уведомляет сетевую службу, что одна из ее привязок отключена.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**\_нетбинденабле управления \_ службами**


</dt> <dd>

Уведомляет сетевую службу, что включена отключенная привязка.

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**\_нетбиндремове управления \_ службами**


</dt> <dd>

Уведомляет сетевую службу о том, что компонент для привязки был удален.

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**\_парамчанже управления \_ службами**


</dt> <dd>

Уведомляет службу о том, что параметры запуска были изменены.

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**\_приостановка управления службой \_**


</dt> <dd>

Сообщает службе о необходимости приостановки.

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**\_Завершение управления \_ службой**


</dt> <dd>

Уведомляет службу о необходимости ее завершения.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений, перечисленных в следующем списке, или другое значение, указывающее на ошибку.

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

Служба не запустилась.

</dd> <dt>

**Время ожидания запроса на обслуживание**
</dt> <dd>

7

Служба не реагирует на запрос на запуск быстро.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

8

Интерактивный процесс.

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

Зависимость, от которой зависит эта служба, удаляется из системы.

</dd> <dt>

**Сбой зависимости службы**
</dt> <dd>

13

Служба не находит службу, необходимую зависимой службе.

</dd> <dt>

**Служба отключена**
</dt> <dd>

14

Служба отключена от системы.

</dd> <dt>

**Сбой при входе в службу**
</dt> <dd>

15

Эта служба не поддерживает проверку подлинности, необходимую для работы в системе.

</dd> <dt>

**Служба помечена для удаления**
</dt> <dd>

16

Служба удаляется из системы.

</dd> <dt>

**Служба без потока**
</dt> <dd>

17

Отсутствует поток исполнения для этой службы.

</dd> <dt>

**Состояние "циклическая зависимость"**
</dt> <dd>

18

При запуске службы обнаружены циклические зависимости.

</dd> <dt>

**Состояние "повторяющееся имя"**
</dt> <dd>

19

Служба с таким именем уже запущена.

</dd> <dt>

**Состояние "Недопустимое имя"**
</dt> <dd>

20

В имени службы присутствуют недопустимые символы.

</dd> <dt>

**Недопустимый параметр Status**
</dt> <dd>

21

Службе переданы недопустимые параметры.

</dd> <dt>

**Недопустимое состояние учетной записи службы**
</dt> <dd>

22

Учетная запись, под которой выполняется эта служба, недопустима или не имеет разрешений на запуск службы.

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

[**\_Басесервице Win32**](win32-baseservice.md)
</dt> </dl>

 

