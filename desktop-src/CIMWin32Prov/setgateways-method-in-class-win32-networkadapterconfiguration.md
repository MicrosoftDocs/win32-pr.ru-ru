---
description: Сетгатевайс &\# 32; Метод класса WMI указывает список шлюзов для маршрутизации пакетов в подсеть, отличную от подсети, к которой подключен сетевой адаптер.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Метод Сетгатевайс класса Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896085"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Метод Сетгатевайс \_ класса Win32 NetworkAdapterConfiguration

Метод  [класса WMI](/windows/desktop/WmiSdk/retrieving-a-class) сетгатевайс указывает список шлюзов для маршрутизации пакетов в подсеть, отличную от подсети, к которой подключен сетевой адаптер.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Дефаултипгатевай* \[ окне\]
</dt> <dd>

Список IP-адресов шлюзов, на которые направляются сетевые пакеты.

</dd> <dt>

*Гатевайкостметрик* \[ в необязательное\]
</dt> <dd>

Присваивает значение, которое находится в диапазоне от 1 до 9999, которое используется для вычисления самого быстрого и наиболее надежного маршрута. Значения этого параметра соответствуют значениям в параметре *дефаултипгатевай* . Значение по умолчанию для шлюза — 1.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (ноль) для успешного завершения, если перезагрузка не требуется, 1 (один) для успешного завершения, когда требуется перезагрузка, и любое другое значение при возникновении ошибки. Дополнительные сведения о кодах ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Общие значения **HRESULT** см. в разделе [коды системных ошибок](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Успешное завершение, перезагрузка не требуется**
</dt> <dd>

0

</dd> <dt>

**Успешное завершение, требуется перезагрузка**
</dt> <dd>

1

</dd> <dt>

**Метод не поддерживается на этой платформе**
</dt> <dd>

64

Метод не поддерживается, если сетевой адаптер находится в режиме DHCP.

</dd> <dt>

**Неизвестный сбой**
</dt> <dd>

65

</dd> <dt>

**Недопустимая маска подсети**
</dt> <dd>

66

</dd> <dt>

**Произошла ошибка при обработке возвращенного экземпляра**
</dt> <dd>

67

</dd> <dt>

**Недопустимый входной параметр**
</dt> <dd>

68

</dd> <dt>

**Указано более 5 шлюзов**
</dt> <dd>

69

</dd> <dt>

**Недопустимый IP-адрес**
</dt> <dd>

70

</dd> <dt>

**Недопустимый IP-адрес шлюза**
</dt> <dd>

71

</dd> <dt>

**Произошла ошибка при доступе к реестру для запрашиваемой информации**
</dt> <dd>

72

</dd> <dt>

**Недопустимое имя домена**
</dt> <dd>

73

</dd> <dt>

**Недопустимое имя узла**
</dt> <dd>

74

</dd> <dt>

**Не определен основной или дополнительный WINS-сервер**
</dt> <dd>

75

</dd> <dt>

**Недопустимый файл**
</dt> <dd>

76

</dd> <dt>

**Недопустимый системный путь**
</dt> <dd>

77

</dd> <dt>

**Не удалось скопировать файл**
</dt> <dd>

78

</dd> <dt>

**Недопустимый параметр безопасности**
</dt> <dd>

79

</dd> <dt>

**Не удалось настроить службу TCP/IP**
</dt> <dd>

80

</dd> <dt>

**Не удалось настроить службу DHCP**
</dt> <dd>

81

</dd> <dt>

**Не удалось продлить аренду DHCP**
</dt> <dd>

82

</dd> <dt>

**Не удалось освободить аренду DHCP**
</dt> <dd>

83

</dd> <dt>

**IP-адрес не включен на адаптере**
</dt> <dd>

84

</dd> <dt>

**IPX не включен на адаптере**
</dt> <dd>

85

</dd> <dt>

**Ошибка границ кадра или сети**
</dt> <dd>

86

</dd> <dt>

**Недопустимый тип кадра**
</dt> <dd>

87

</dd> <dt>

**Недопустимый номер сети**
</dt> <dd>

88

</dd> <dt>

**Дублирующийся номер сети**
</dt> <dd>

89

</dd> <dt>

**Параметр вне границ**
</dt> <dd>

90

</dd> <dt>

**Доступ запрещен**
</dt> <dd>

91

</dd> <dt>

**Нет памяти**
</dt> <dd>

92

</dd> <dt>

**Уже существует**
</dt> <dd>

93

</dd> <dt>

**Путь, файл или объект не найдены**
</dt> <dd>

94

</dd> <dt>

**Не удалось уведомить службу**
</dt> <dd>

95

</dd> <dt>

**Не удалось уведомить службу DNS**
</dt> <dd>

96

</dd> <dt>

**Интерфейс не может быть настроен**
</dt> <dd>

97

</dd> <dt>

**Не все аренды DHCP могут быть освобождены или обновлены**
</dt> <dd>

98

</dd> <dt>

**DHCP не включен на адаптере**
</dt> <dd>

100

</dd> <dt>

**Другое**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Комментарии

Этот метод работает, только если сетевой адаптер (NIC) находится в режиме статического IP-адреса.

Чтобы очистить шлюз, задайте для шлюза тот же IP-адрес, который используется в [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).

## <a name="examples"></a>Примеры

В примере [изменения шлюзов для сетевого адаптера](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript настраиваются два шлюза для сетевого адаптера.

В примере « [Назначение статического IP-адреса](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) на языке VBScript» задается IP-адрес и шлюз компьютера.

[Статический IP-адрес, а затем присоединение к](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) образцу PowerShell для домена помогает в перестроении компьютеров.

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

 

