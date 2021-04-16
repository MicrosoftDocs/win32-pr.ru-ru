---
description: Метод класса WMI ReleaseDHCPLease освобождает IP-адрес, привязанный к конкретному сетевому адаптеру с поддержкой DHCP.
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Метод ReleaseDHCPLease класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105655998"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a>Метод ReleaseDHCPLease \_ класса Win32 NetworkAdapterConfiguration

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) ReleaseDHCPLease освобождает IP-адрес, привязанный к конкретному сетевому адаптеру с поддержкой DHCP.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль) для успешного завершения, если не требуется перезагрузка, 1 (один) для успешного завершения, когда требуется перезагрузка, и другое число в случае ошибки. Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

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

> [!Caution]  
> Если DHCP включен на локальном компьютере, параметр отключает TCP/IP для этого конкретного сетевого адаптера. Если нет альтернативного пути к целевой системе, то есть другим связанным с TCP/IP сетевым адаптером, все связи TCP/IP будут потеряны.

 

## <a name="examples"></a>Примеры

В этом примере для [обновления IP-адресов с помощью PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell в коллекции TechNet используется **ReleaseDHCPLease** для выпуска и продления IP-адреса.

Следующий код VBScript освобождает аренду DHCP для всех сетевых адаптеров, привязанных к TCP/IP, на компьютере.


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
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

 

