---
title: Класс Win32_TSSessionDirectory
description: Определяет параметры конфигурации подключение к удаленному рабочему столу Broker (RDCB) для \_ класса Win32 тссессиондиректорисеттинг.
ms.assetid: ef9042c2-4a35-49e9-b195-fb37c0919068
ms.tgt_platform: multiple
keywords:
- Класс Win32_TSSessionDirectory службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_TSSessionDirectory, описание
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory
- Win32_TSSessionDirectory.Caption
- Win32_TSSessionDirectory.Description
- Win32_TSSessionDirectory.InstallDate
- Win32_TSSessionDirectory.Name
- Win32_TSSessionDirectory.Status
- Win32_TSSessionDirectory.SessionDirectoryLocation
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryLocation
- Win32_TSSessionDirectory.SessionDirectoryActive
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryActive
- Win32_TSSessionDirectory.SessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryExposeServerIP
- Win32_TSSessionDirectory.SessionDirectoryClusterName
- Win32_TSSessionDirectory.PolicySourceLoadBalancing
- Win32_TSSessionDirectory.GetLoadBalancingState
- Win32_TSSessionDirectory.GetServerWeight
- Win32_TSSessionDirectory.PolicySourceSessionDirectoryClusterName
- Win32_TSSessionDirectory.SessionDirectoryIPAddress
- Win32_TSSessionDirectory.GetTSRedirectorMode
- Win32_TSSessionDirectory.PolicySourceTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb50ed77b99f415ae551dfcf69655af5c1d77501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988507"
---
# <a name="win32_tssessiondirectory-class"></a>\_Класс Win32 тссессиондиректори

Определяет параметры конфигурации подключение к удаленному рабочему столу Broker (RDCB) для класса [**Win32 \_ тссессиондиректорисеттинг**](win32-tssessiondirectorysetting.md) .

> [!Note]  
> В Windows Server 2008 R2 имя посредника сеансов служб терминалов было изменено на RDCB. Эти свойства применяются ко всем поддерживаемым операционным системам, если не указано иное.

 

Следующий синтаксис упрощен из MOF-кода и включает все определенные и унаследованные свойства в алфавитном порядке. Справочные сведения о методах см. в таблице методов далее в этом разделе.

## <a name="syntax"></a>Синтаксис

``` syntax
[dynamic, provider("Win32_WIN32_TSSESSIONDIRECTORY_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TSSessionDirectory : CIM_Setting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   SessionDirectoryLocation;
  uint32   PolicySourceSessionDirectoryLocation;
  uint32   SessionDirectoryActive;
  uint32   PolicySourceSessionDirectoryActive;
  uint32   SessionDirectoryExposeServerIP;
  uint32   PolicySourceSessionDirectoryExposeServerIP;
  string   SessionDirectoryClusterName;
  uint32   PolicySourceLoadBalancing;
  uint32   GetLoadBalancingState;
  uint32   GetServerWeight;
  uint32   PolicySourceSessionDirectoryClusterName;
  string   SessionDirectoryIPAddress;
  uint32   GetTSRedirectorMode;
  uint32   PolicySourceTSRedirectorMode;
};
```

## <a name="members"></a>Члены

Класс **Win32 \_ тссессиондиректори** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Класс **Win32 \_ тссессиондиректори** содержит следующие методы.



| Метод                                                                                                  | Описание                                                                                                  |
|:--------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| [**креатеусердисктемплате**](createuserdisktemplate-win32-tssessiondirectory.md)                       | Создает шаблон диска пользователя.<br/>                                                                     |
| [**дисаблеусервхд**](disableuservhd-win32-tssessiondirectory.md)                                       | Отключает виртуальный жесткий диск профиля пользователя.<br/>                                                                      |
| [**енаблеусервхд**](enableuservhd-win32-tssessiondirectory.md)                                         | Включает виртуальный жесткий диск профиля пользователя на сервере узлов удаленных рабочих столов.<br/>                                                     |
| [**жеткуррентредиректаблеаддрессес**](getcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Получает настроенный в данный момент список доступных адресов DNS и тип перенаправления.<br/>        |
| [**жетредиректаблеаддрессес**](getredirectableaddresses-win32-tssessiondirectory.md)                   | Получает полный список доступных адресов DNS.<br/>                                                |
| [**пингсессиондиректори**](pingsessiondirectory-win32-tssessiondirectory.md)                           | Проверяет, доступен ли сервер RDCB.<br/>                                      |
| [**сеткуррентредиректаблеаддрессес**](setcurrentredirectableaddresses-win32-tssessiondirectory.md)     | Задает настроенный список доступных адресов DNS и тип перенаправления.<br/>                     |
| [**сетлоадбаланЦингстате**](setloadbalancingstate-win32-tssessiondirectory.md)                         | Задает значение, указывающее, будет ли сервер участвовать в балансировке нагрузки RDCB.<br/> |
| [**сетсервервеигхт**](setserverweight-win32-tssessiondirectory.md)                                     | Задает значение веса сервера для балансировки нагрузки RDCB.<br/>                             |
| [**сетсессиондиректоряктиве**](win32-tssessiondirectory-setsessiondirectoryactive.md)                 | Отключает и включает RDCB.<br/>                                                    |
| [**сетсессиондиректорекспосесерверип**](win32-tssessiondirectory-setsessiondirectoryexposeserverip.md) | Задает свойство **сессиондиректорекспосесерверип** .<br/>                                             |
| [**сетсессиондиректорипроперти**](win32-tssessiondirectory-setsessiondirectoryproperty.md)             | Задает свойство **сессиондиректорилокатион** или свойство **сессиондиректориклустернаме** .<br/>   |
| [**сеттсредиректормоде**](settsredirectormode-win32-tssessiondirectory.md)                             | Этот метод недоступен.<br/>                                                                     |



 

### <a name="properties"></a>Свойства

Класс **Win32 \_ тссессиондиректори** имеет следующие свойства.

<dl> <dt>

**Заголовок**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Краткое описание (однострочная строка) объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**жетлоадбаланЦингстате**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроен ли сервер для участия в балансировке нагрузки RDCB.

<dt>

0
</dt> <dd>

Сервер не настроен для участия в балансировке нагрузки RDCB.

</dd> <dt>

1
</dt> <dd>

Сервер настроен для участия в балансировке нагрузки RDCB.

</dd> </dl>

</dd> <dt>

**жетсервервеигхт**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Возвращает значение веса сервера, используемое в балансировке нагрузки RDCB.

</dd> <dt>

**жеттсредиректормоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроен ли сервер для работы в качестве перенаправления службы удаленных рабочих столов.

<dt>

0
</dt> <dd>

Сервер настроен на работу в качестве перенаправления службы удаленных рабочих столов.

</dd> <dt>

1
</dt> <dd>

Сервер не настроен на работу в качестве перенаправления службы удаленных рабочих столов.

</dd> </dl>

**Windows Server 2008:** Это свойство недоступно.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Тип данных: **DateTime**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**маппингстрингс**](/windows/desktop/WmiSdk/standard-qualifiers) (MIF. \|Значение ComponentID \| 001,5 в DMTF
</dt> </dl>

Дата установки объекта. Отсутствие значения не означает, что объект не установлен.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Имя объекта.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

</dd> <dt>

**полицисаурцелоадбаланЦинг**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **жетлоадбаланЦингстате** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцесессиондиректоряктиве**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **сессиондиректоряктиве** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцесессиондиректориклустернаме**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **сессиондиректориклустернаме** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцесессиондиректорекспосесерверип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **сессиондиректорекспосесерверип** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцесессиондиректорилокатион**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, настроено ли свойство **сессиондиректорилокатион** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**полицисаурцетсредиректормоде**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Это свойство недоступно.

**Windows Server 2008 R2:** Указывает, настроено ли свойство **жеттсредиректормоде** сервером или групповой политикой.

<dt>

0 (0x0)
</dt> <dd>

Сервер

</dd> <dt>

1 (0x1)
</dt> <dd>

Групповая политика

</dd> </dl>

</dd> <dt>

**сессиондиректоряктиве**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Указывает, участвует ли службы удаленных рабочих столов в RDCB.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Службы удаленных рабочих столов участие в RDCB отключено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Службы удаленных рабочих столов участие в RDCB включено.

</dd> </dl>

</dd> <dt>

**сессиондиректориклустернаме**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Виртуальный IP-адрес кластера, к которому принадлежит сервер узла сеансов удаленных рабочих столов.

</dd> <dt>

**сессиондиректорекспосесерверип**
</dt> <dd> <dl> <dt>

Тип данных: **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, разрешено ли получение IP-адреса RDCB.

<dt>

<span id="FALSE"></span><span id="false"></span>

<span id="FALSE"></span><span id="false"></span>**False** (0)


</dt> <dd>

Получение запрещено.

</dd> <dt>

<span id="TRUE"></span><span id="true"></span>

<span id="TRUE"></span><span id="true"></span>**True** (1)


</dt> <dd>

Извлечение разрешено.

</dd> </dl>

</dd> <dt>

**сессиондиректорипаддресс**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

IP-адрес адаптера локальной сети, используемого каталогом сеансов.

</dd> <dt>

**сессиондиректорилокатион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Сетевое DNS-имя или IP-адрес сервера, на котором запущена служба RDCB.

</dd> <dt>

**Состояние**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Текущее состояние объекта. Можно определить различные операционные и неоперационные состояния. Рабочие состояния включают: "ОК", "деградация" и "пред-ошибка" (элемент, например жесткий диск с поддержкой SMART, может работать правильно, но прогнозировать сбой в ближайшем будущем). Неработающие состояния включают: "ошибка", "Запуск", "остановка" и "служба". Последняя, «служба», может применяться во время зеркального копирования диска, перезагрузки списка разрешений пользователя или другой административной работы. Не вся такая работа выполняется в интерактивном состоянии, но управляемый элемент не является ни "ОК", ни одним из других состояний.

Это свойство наследуется от [**CIM \_ манажедсистемелемент**](cim-managedsystemelement.md).

<dt>



 ("ОК")


</dt> <dd></dd> <dt>



 ("Ошибка")


</dt> <dd></dd> <dt>



 ("Пониженное состояние")


</dt> <dd></dd> <dt>



 ("Неизвестно")


</dt> <dd></dd> <dt>



 ("Пред Fail")


</dt> <dd></dd> <dt>



 ("Запуск")


</dt> <dd></dd> <dt>



 ("Остановка")


</dt> <dd></dd> <dt>



 ("Служба")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Комментарии

Чтобы подключиться к \\ \\ корневому \\ \\ пространству имен CIMV2 терминалсервицес, уровень проверки подлинности должен включать в себя конфиденциальность пакетов. Для вызовов C/C++ это уровень проверки подлинности **AUTHN на \_ \_ \_ уровне \_ \_ безопасности RPC C уровня "PKT**". Для Visual Basic и написания сценариев это уровень проверки подлинности **вбемаусентикатионлевелпктприваци** или "пктприваци" со значением шесть.

В следующем примере Visual Basic Scripting Edition (VBScript) показано, как подключиться к удаленному компьютеру с использованием конфиденциальности пакетов.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



В Windows Server 2008 имя функции каталога сеансов служб терминалов было изменено на посредник сеансов служб терминалов.

В Windows Server 2008 R2 имя компонента посредника сеансов служб терминалов изменилось на подключение к удаленному рабочему столу Broker.

Файлы MOF-файл (MOF) содержат определения для классов инструментарий управления Windows (WMI) (WMI). MOF-файлы не устанавливаются в составе пакета средств разработки программного обеспечения Microsoft Windows (SDK). Они устанавливаются на сервере при добавлении связанной роли с помощью диспетчер сервера. Дополнительные сведения о файлах MOF см. в разделе [MOF-файл (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тскфгвми. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Параметр CIM**](cim-setting.md)
</dt> <dt>

[**\_Тссессиондиректорисеттинг Win32**](win32-tssessiondirectorysetting.md)
</dt> </dl>

 

