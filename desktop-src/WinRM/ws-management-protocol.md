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
# <a name="ws-management-protocol"></a><span data-ttu-id="e77c7-103">Протокол WS-Management</span><span class="sxs-lookup"><span data-stu-id="e77c7-103">WS-Management Protocol</span></span>

<span data-ttu-id="e77c7-104">Протокол WS-Management разрабатывался группой изготовителей оборудования и программного обеспечения в качестве открытого стандарта для удаленного обмена данными управления между любыми компьютерными устройствами, в которых реализован этот протокол.</span><span class="sxs-lookup"><span data-stu-id="e77c7-104">The WS-Management protocol was developed by a group of hardware and software manufacturers as a public standard for remotely exchanging management data with any computer device that implements the protocol.</span></span>

## <a name="standards"></a><span data-ttu-id="e77c7-105">Стандарты</span><span class="sxs-lookup"><span data-stu-id="e77c7-105">Standards</span></span>

<span data-ttu-id="e77c7-106">Дополнительные сведения о протоколе WS-Management см. в статье [спецификации веб-служб для управления (WS-Management)](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span><span class="sxs-lookup"><span data-stu-id="e77c7-106">For more information about WS-Management protocol, see [Web Services for Management (WS-Management) Specification](https://dmtf.org/sites/default/files/standards/documents/DSP0226_1.2.0.pdf).</span></span>

<span data-ttu-id="e77c7-107">Цель протокола — обеспечить согласованность и совместимость операций управления для различных типов устройств (включая встроенное по) и операционных систем.</span><span class="sxs-lookup"><span data-stu-id="e77c7-107">The intent of the protocol is to provide consistency and interoperability for management operations across many types of devices (including firmware) and operating systems.</span></span> <span data-ttu-id="e77c7-108">WS-Management протокол можно расширить по мере того, как в отрасли ИТ будут обнаружены новые операции.</span><span class="sxs-lookup"><span data-stu-id="e77c7-108">WS-Management protocol can be extended as new operations are identified by the IT industry.</span></span>

<span data-ttu-id="e77c7-109">Текущая реализация протокола WS-Management основана на следующих стандартных спецификациях: HTTPS, SOAP по HTTP (WS-I Profile), SOAP 1,2, WS-Addressing, WS-передачи, WS-enumeration и WS-Eventing.</span><span class="sxs-lookup"><span data-stu-id="e77c7-109">The current implementation of the WS-Management protocol is based on the following standard specifications: HTTPS, SOAP over HTTP (WS-I profile), SOAP 1.2, WS-Addressing, WS-Transfer, WS-Enumeration, and WS-Eventing.</span></span> <span data-ttu-id="e77c7-110">Дополнительные сведения о стандартах WS-Management и XML-схемах см. в разделе <https://dmtf.org/standards/wsman></span><span class="sxs-lookup"><span data-stu-id="e77c7-110">For more information about the WS-Management standards and XML schemas see <https://dmtf.org/standards/wsman></span></span>

## <a name="messages"></a><span data-ttu-id="e77c7-111">Сообщения</span><span class="sxs-lookup"><span data-stu-id="e77c7-111">Messages</span></span>

<span data-ttu-id="e77c7-112">Протокол WS-Management предоставляет стандарт для создания XML- [*сообщений*](windows-remote-management-glossary.md) с использованием различных стандартов веб-служб, таких как [*WS-Addressing*](windows-remote-management-glossary.md) и [*WS-reпередач*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="e77c7-112">The WS-Management protocol provides a standard for constructing XML [*messages*](windows-remote-management-glossary.md) using various web service standards such as [*WS-Addressing*](windows-remote-management-glossary.md) and [*WS-Transfer*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e77c7-113">Эти стандарты определяют XML-схемы для сообщений веб-службы.</span><span class="sxs-lookup"><span data-stu-id="e77c7-113">These standards define XML schemas for web service messages.</span></span> <span data-ttu-id="e77c7-114">Сообщения ссылаются на [*ресурс*](windows-remote-management-glossary.md) с помощью [*URI ресурса*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="e77c7-114">The messages refer to a [*resource*](windows-remote-management-glossary.md) using a [*resource URI*](windows-remote-management-glossary.md).</span></span> <span data-ttu-id="e77c7-115">Протокол WS-Management добавляет набор определений для операций управления и значений.</span><span class="sxs-lookup"><span data-stu-id="e77c7-115">The WS-Management protocol adds a set of definitions for management operations and values.</span></span> <span data-ttu-id="e77c7-116">Например, WS-Transfer определяет операции получения, размещения, создания и удаления ресурса.</span><span class="sxs-lookup"><span data-stu-id="e77c7-116">For example, WS-Transfer defines the Get, Put, Create, and Delete operations for a resource.</span></span> <span data-ttu-id="e77c7-117">WS-Management протокол добавляет переименование, частичный возврат и частичную помещает.</span><span class="sxs-lookup"><span data-stu-id="e77c7-117">WS-Management protocol adds Rename, Partial Get, and Partial Put.</span></span>

<span data-ttu-id="e77c7-118">Сообщения следуют правилам [*протокола SOAP*](windows-remote-management-glossary.md) , используемым всеми протоколами веб-служб.</span><span class="sxs-lookup"><span data-stu-id="e77c7-118">The messages follow the conventions of [*Simple Object Access Protocol (SOAP)*](windows-remote-management-glossary.md) which is used by all web service protocols.</span></span>

<span data-ttu-id="e77c7-119">В следующем примере кода показано сообщение с операцией Get.</span><span class="sxs-lookup"><span data-stu-id="e77c7-119">The following code example shows a message with a Get operation.</span></span> <span data-ttu-id="e77c7-120">Этот пример показан в качестве вспомогательного средства для понимания того, как выглядят основные сообщения.</span><span class="sxs-lookup"><span data-stu-id="e77c7-120">This example is shown as an aid to understanding what the underlying messages look like.</span></span> <span data-ttu-id="e77c7-121">Вам не нужно знать, как создавать сообщения SOAP.</span><span class="sxs-lookup"><span data-stu-id="e77c7-121">You do not need to know how to produce SOAP messages.</span></span> <span data-ttu-id="e77c7-122">Эти сообщения собираются служба удаленного управления Windows при выполнении команды с помощью программы командной строки **WinRM** или при выполнении скрипта, написанного с помощью [API-интерфейса для сценариев WinRM](winrm-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e77c7-122">The messages are assembled by Windows Remote Management when you execute a command using the **Winrm** command-line tool or run a script written with the [WinRM Scripting API](winrm-scripting-api.md).</span></span>

<span data-ttu-id="e77c7-123">Сообщение является запросом на получение экземпляра [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) со свойством **DeviceID** из "c:" с сервера с именем ремотекомпутер.</span><span class="sxs-lookup"><span data-stu-id="e77c7-123">The message is a request to get the instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) with a **DeviceID** property of "c:" from a server named RemoteComputer.</span></span> <span data-ttu-id="e77c7-124">Запрос использует транспорт HTTP через порт 80.</span><span class="sxs-lookup"><span data-stu-id="e77c7-124">The request uses the HTTP transport through port 80.</span></span> <span data-ttu-id="e77c7-125">Учетная запись, отправляющей запрос, должна находиться в локальной группе администраторов на удаленном компьютере.</span><span class="sxs-lookup"><span data-stu-id="e77c7-125">The account sending the request must be in the local administrators group on the remote computer.</span></span>

<span data-ttu-id="e77c7-126">Символы перед двоеточием в начале каждого тега указывают, какой стандарт определяет XML-элемент.</span><span class="sxs-lookup"><span data-stu-id="e77c7-126">The characters before the colon at the beginning of each tag indicate which standard defines the XML element.</span></span> <span data-ttu-id="e77c7-127">Например, ` <wsa:To>` указывает, что элемент to определяется WS-Addressing стандартом и `<s:Header>` указывает начало содержимого заголовка в сообщении SOAP.</span><span class="sxs-lookup"><span data-stu-id="e77c7-127">For example, ` <wsa:To>` indicates that the To element is defined by the WS-Addressing standard and `<s:Header>` indicates the beginning of the header content in a SOAP message.</span></span> <span data-ttu-id="e77c7-128">Имейте в виду, что большая часть сообщения состоит из XML-элементов, определенных SOAP или WS-Addressing.</span><span class="sxs-lookup"><span data-stu-id="e77c7-128">Be aware that the majority of the message is composed of XML elements defined by SOAP or WS-Addressing.</span></span> <span data-ttu-id="e77c7-129">WS-Management протокол добавляет Максенвелопесизе, Selector и Selector.</span><span class="sxs-lookup"><span data-stu-id="e77c7-129">WS-Management protocol adds MaxEnvelopeSize, Selector, and SelectorSet.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e77c7-130">См. также</span><span class="sxs-lookup"><span data-stu-id="e77c7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e77c7-131">О служба удаленного управления Windows</span><span class="sxs-lookup"><span data-stu-id="e77c7-131">About Windows Remote Management</span></span>](about-windows-remote-management.md)
</dt> <dt>

[<span data-ttu-id="e77c7-132">Удаленное управление оборудованием</span><span class="sxs-lookup"><span data-stu-id="e77c7-132">Remote Hardware Management</span></span>](remote-hardware-management.md)
</dt> </dl>

 

 