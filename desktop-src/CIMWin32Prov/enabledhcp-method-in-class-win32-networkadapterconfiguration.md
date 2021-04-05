---
description: Метод класса WMI EnableDHCP включает протокол DHCP для службы с этим сетевым адаптером. DHCP разрешает динамическое выделение IP-адресов.
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Метод EnableDHCP класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990501"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a>Метод EnableDHCP \_ класса Win32 NetworkAdapterConfiguration

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) EnableDHCP включает протокол DHCP для службы с этим сетевым адаптером. DHCP разрешает динамическое выделение IP-адресов.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое число в случае ошибки. Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение, перезагрузка не требуется**
</dt> <dd>

0

Успешное завершение, перезагрузка не требуется.

</dd> <dt>

**Успешное завершение, требуется перезагрузка**
</dt> <dd>

1

Успешное завершение, требуется перезагрузка.

</dd> <dt>

**Метод не поддерживается на этой платформе**
</dt> <dd>

64

Метод не поддерживается на этой платформе.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

65

Неизвестный сбой.

</dd> <dt>

**Недопустимая маска подсети**
</dt> <dd>

66

Недопустимая маска подсети.

</dd> <dt>

**Произошла ошибка при обработке возвращенного экземпляра**
</dt> <dd>

67

Произошла ошибка при обработке возвращенного экземпляра.

</dd> <dt>

**Недопустимый входной параметр**
</dt> <dd>

68

Недопустимый входной параметр.

</dd> <dt>

**Указано более 5 шлюзов**
</dt> <dd>

69

Указано более пяти шлюзов.

</dd> <dt>

**Недопустимый IP-адрес**
</dt> <dd>

70

Недопустимый IP-адрес.

</dd> <dt>

**Недопустимый IP-адрес шлюза**
</dt> <dd>

71

Недопустимый IP-адрес шлюза.

</dd> <dt>

**Произошла ошибка при доступе к реестру для запрашиваемой информации**
</dt> <dd>

72

Произошла ошибка при доступе к реестру для запрашиваемой информации.

</dd> <dt>

**Недопустимое имя домена**
</dt> <dd>

73

Недопустимое имя домена.

</dd> <dt>

**Недопустимое имя узла**
</dt> <dd>

74

Недопустимое имя узла.

</dd> <dt>

**Не определен основной или дополнительный WINS-сервер**
</dt> <dd>

75

Не определен основной или дополнительный WINS-сервер.

</dd> <dt>

**Недопустимый файл**
</dt> <dd>

76

Недопустимый файл.

</dd> <dt>

**Недопустимый системный путь**
</dt> <dd>

77

Недопустимый системный путь.

</dd> <dt>

**Не удалось скопировать файл**
</dt> <dd>

78

Не удалось скопировать файл.

</dd> <dt>

**Недопустимый параметр безопасности**
</dt> <dd>

79

Недопустимый параметр безопасности.

</dd> <dt>

**Не удалось настроить службу TCP/IP**
</dt> <dd>

80

Не удалось настроить службу TCP/IP.

</dd> <dt>

**Не удалось настроить службу DHCP**
</dt> <dd>

81

Не удалось настроить службу DHCP.

</dd> <dt>

**Не удалось продлить аренду DHCP**
</dt> <dd>

82

Не удалось продлить аренду DHCP.

</dd> <dt>

**Не удалось освободить аренду DHCP**
</dt> <dd>

83

Не удалось освободить аренду DHCP.

</dd> <dt>

**IP-адрес не включен на адаптере**
</dt> <dd>

84

IP-адрес не включен на адаптере.

</dd> <dt>

**IPX не включен на адаптере**
</dt> <dd>

85

IPX не включен на адаптере.

</dd> <dt>

**Ошибка границ кадра или сети**
</dt> <dd>

86

Ошибка границ кадра или номера сети.

</dd> <dt>

**Недопустимый тип кадра**
</dt> <dd>

87

Недопустимый тип кадра.

</dd> <dt>

**Недопустимый номер сети**
</dt> <dd>

88

Недопустимый номер сети.

</dd> <dt>

**Дублирующийся номер сети**
</dt> <dd>

89

Дублирующийся номер сети.

</dd> <dt>

**Параметр вне границ**
</dt> <dd>

90

Параметр вне допустимых границ.

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

91

Доступ запрещен.

</dd> <dt>

**Нет памяти**
</dt> <dd>

92

Недостаточно памяти.

</dd> <dt>

**Уже существует**
</dt> <dd>

93

Уже существует.

</dd> <dt>

**Путь, файл или объект не найдены**
</dt> <dd>

94

Путь, файл или объект не найдены.

</dd> <dt>

**Не удалось уведомить службу**
</dt> <dd>

95

Не удалось уведомить службу.

</dd> <dt>

**Не удалось уведомить службу DNS**
</dt> <dd>

96

Не удалось уведомить службу DNS.

</dd> <dt>

**Интерфейс не может быть настроен**
</dt> <dd>

97

Интерфейс недоступен для настройки.

</dd> <dt>

**Не все аренды DHCP могут быть освобождены или обновлены**
</dt> <dd>

98

Не все аренды DHCP могут быть освобождены или обновлены.

</dd> <dt>

**DHCP не включен на адаптере**
</dt> <dd>

100

DHCP не включен на адаптере.

</dd> <dt>

**Другое**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот метод не очищает статические шлюзы по умолчанию, имеющиеся на компьютере.

## <a name="examples"></a>Примеры

Пример кода VBScript для [включения DHCP и назначения DNS-серверов](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) в коллекции TechNet использует EnableDHCP для включения DHCP и назначения DNS-серверов компьютеру.

В следующем примере кода VBScript показано, как включить использование DHCP в экземпляре [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) . В этом случае мы указываем адаптер с индексом 0. Правильный индекс должен быть выбран из экземпляров Win32 \_ сетевого адаптера для других интерфейсов.

> [!Note]  
> Поддерживается только на платформах NT.

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



В следующем образце кода Perl показано, как включить использование DHCP в экземпляре [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) . В этом случае мы указываем адаптер с индексом 0. Правильный индекс должен быть выбран из экземпляров Win32 \_ сетевого адаптера для других интерфейсов.

> [!Note]  
> Поддерживается только на платформах NT.

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
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

[Аппаратные классы системы компьютера](computer-system-hardware-classes.md)
</dt> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Задачи WMI: Сетевые подключения](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Задачи WMI: учетные записи и домены](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Поддержка IPv6 и IPv4 в WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

