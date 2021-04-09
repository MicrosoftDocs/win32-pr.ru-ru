---
title: Протокол WS-Management
description: Общедоступный стандарт для удаленного обмена данными управления с любым устройством компьютера, реализующим протокол.
ms.assetid: 2c47acd2-5d52-4e0f-8848-a11aff59f963
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61e01fdc860eeb5510dd78a4127fdc22b30d711a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134539"
---
# <a name="ws-management-protocol"></a>Протокол WS-Management

Протокол WS-Management разрабатывался группой изготовителей оборудования и программного обеспечения в качестве открытого стандарта для удаленного обмена данными управления между любыми компьютерными устройствами, в которых реализован этот протокол.

## <a name="standards"></a>Стандарты

Дополнительные сведения о протоколе WS-Management см. в статье [спецификации веб-служб для управления (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).

Цель протокола — обеспечить согласованность и совместимость операций управления для различных типов устройств (включая встроенное по) и операционных систем. WS-Management протокол можно расширить по мере того, как в отрасли ИТ будут обнаружены новые операции.

Текущая реализация протокола WS-Management основана на следующих стандартных спецификациях: HTTPS, SOAP по HTTP (WS-I Profile), SOAP 1,2, WS-Addressing, WS-передачи, WS-enumeration и WS-Eventing. Дополнительные сведения о стандартах WS-Management и XML-схемах см. в разделе <https://dmtf.org/standards/wsman>

## <a name="messages"></a>Сообщения

Протокол WS-Management предоставляет стандарт для создания XML- [*сообщений*](windows-remote-management-glossary.md) с использованием различных стандартов веб-служб, таких как [*WS-Addressing*](windows-remote-management-glossary.md) и [*WS-reпередач*](windows-remote-management-glossary.md). Эти стандарты определяют XML-схемы для сообщений веб-службы. Сообщения ссылаются на [*ресурс*](windows-remote-management-glossary.md) с помощью [*URI ресурса*](windows-remote-management-glossary.md). Протокол WS-Management добавляет набор определений для операций управления и значений. Например, WS-Transfer определяет операции получения, размещения, создания и удаления ресурса. WS-Management протокол добавляет переименование, частичный возврат и частичную помещает.

Сообщения следуют правилам [*протокола SOAP*](windows-remote-management-glossary.md) , используемым всеми протоколами веб-служб.

В следующем примере кода показано сообщение с операцией Get. Этот пример показан в качестве вспомогательного средства для понимания того, как выглядят основные сообщения. Вам не нужно знать, как создавать сообщения SOAP. Эти сообщения собираются служба удаленного управления Windows при выполнении команды с помощью программы командной строки **WinRM** или при выполнении скрипта, написанного с помощью [API-интерфейса для сценариев WinRM](winrm-scripting-api.md).

Сообщение является запросом на получение экземпляра [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) со свойством **DeviceID** из "c:" с сервера с именем ремотекомпутер. Запрос использует транспорт HTTP через порт 80. Учетная запись, отправляющей запрос, должна находиться в локальной группе администраторов на удаленном компьютере.

Символы перед двоеточием в начале каждого тега указывают, какой стандарт определяет XML-элемент. Например, ` <wsa:To>` указывает, что элемент to определяется WS-Addressing стандартом и `<s:Header>` указывает начало содержимого заголовка в сообщении SOAP. Имейте в виду, что большая часть сообщения состоит из XML-элементов, определенных SOAP или WS-Addressing. WS-Management протокол добавляет Максенвелопесизе, Selector и Selector.


```XML
<s:Envelope xmlns:s="https://www.w3.org/2003/05/soap-envelope" 
            xmlns:a="https://schemas.xmlsoap.org/ws/2004/08/addressing" 
            xmlns:w="https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd">
  <s:Header>
    <a:To>https://RemoteComputer:80/wsman</a:To> 
    <w:ResourceURI s:mustUnderstand="true">
      http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_logicaldisk
    </w:ResourceURI> 
    <a:ReplyTo>
    <a:Address s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </a:Address> 
    </a:ReplyTo>
    <a:Action s:mustUnderstand="true">
      https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </a:Action> 
    <w:MaxEnvelopeSize s:mustUnderstand="true">153600</w:MaxEnvelopeSize> 
    <a:MessageID>uuid:4ED2993C-4339-4E99-81FC-C2FD3812781A</a:MessageID> 
    <w:Locale xml:lang="en-US" s:mustUnderstand="false"/> 
    <w:SelectorSet>
    <w:Selector Name="DeviceId">c:</w:Selector> 
    </w:SelectorSet>
    <w:OperationTimeout>PT60.000S</w:OperationTimeout> 
  </s:Header>
  <s:Body/> 
</s:Envelope>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Удаленное управление оборудованием](remote-hardware-management.md)
</dt> </dl>

 

 