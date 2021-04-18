---
title: Определение того, поддерживает ли удаленный компьютер протокол WS-Management
description: Можно использовать сеанс. Identify или IWSManSession. Определите методы, чтобы определить, имеет ли удаленный компьютер службу, поддерживающую протокол WS-Management.
ms.assetid: 4d11ac02-fa8b-45d7-bceb-a18f561bc928
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af82284b38b2a101c767766d44eb975ff7e1dadc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700565"
---
# <a name="detecting-whether-a-remote-computer-supports-ws-management-protocol"></a>Определение того, поддерживает ли удаленный компьютер протокол WS-Management

Можно использовать [**сеанс. Identify**](session-identify.md) или [**IWSManSession. Определите**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmansession-identify) методы, чтобы определить, имеет ли удаленный компьютер службу, поддерживающую протокол WS-Management.

Если служба протокола WS-Management настроена на удаленном компьютере и ожидает передачи запросов, служба может обнаружить запрос на выявление в заголовке с помощью следующего XML-кода.


```XML
xmlns:wsmid="https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity"
```



Служба протокола WS-Management, которая получает запрос, возвращает сведения, содержащиеся в следующем списке, в тексте сообщения:

-   Версия протокола WS-Management. Например, https://schemas.dmtf.org/wbem/wsman/1/wsman.
-   Поставщик продукта, например «корпорация Майкрософт».
-   Версия продукта. Если запрос отправляется с помощью **всманфлагусеноаусентикатион** в параметре *flags* , сведения о версии продукта не возвращаются. Если запрос отправляется либо с проверкой подлинности по умолчанию, либо с помощью указанного другого режима проверки подлинности, то могут возвращаться сведения о версии продукта.

Запрос на обнаружение того, имеется ли на удаленном компьютере настроенная и слушающая WS-Management Служба протокола может быть выполнена в начале скрипта с другими операциями. Это позволит проверить, что конечный компьютер или компьютеры могут отвечать на дальнейшие запросы WS-Management протоколов. Проверку также можно выполнить в отдельном сценарии.

**Обнаружение службы протокола WS-Management**

1.  Создайте объект [**WSMan**](wsman.md) .

    ```VB
    Set objWsman = CreateObject("Wsman.Automation")
    ```

    

2.  Определите, должен ли запрос отправляться с проверкой подлинности или без проверки подлинности и соответствующим образом установите параметр *flags* в вызове [**WSMan. CreateSession**](wsman-createsession.md).

    ```VB
    set objSession = objWsman.CreateSession("Remote1", _
       objWsman.SessionFlagUseNoAuthentication)
    ```

    

3.  Вызовите [**сеанс. Identify**](session-identify.md).

    ```VB
    objSession.Identify
    ```

    

## <a name="examples"></a>Примеры

Следующий пример кода VBScript отправляет на удаленный компьютер с именем "Remote1" запрос на выявление без проверки подлинности в том же домене.


```VB
set objWsman = CreateObject("Wsman.Automation")
set objSession = objWsman.CreateSession("Remote1", _
  objWsman.SessionFlagUseNoAuthentication)
WScript.Echo objSession.Identify
```



Следующий ответ показывает код XML, возвращаемый удаленным компьютером. Версия протокола WS-Management (" https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd ") и поставщик операционной системы ("Корпорация Майкрософт") указаны в возвращенном XML. Так как сообщение отправляется без проверки подлинности, версия продукта не возвращается службой служба удаленного управления Windows.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 0.0.0 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



Следующий пример кода VBScript отправляет на удаленный компьютер запрос на выявление проверки подлинности.


```VB
set ObjWSMan = CreateObject("Wsman.Automation")
set objSession = WSMan.CreateSession("Remote1", _
  objWSMan.SessionFlagUseKerberos)
WScript.Echo objSession.Identify
```



Поскольку запрос был отправлен с проверкой подлинности, возвращаются сведения о версии.


```XML
<wsmid:IdentifyResponse xmlns:wsmid=
    "https://schemas.dmtf.org/wbem/wsman/identity/1/wsmanidentity.xsd">
<wsmid:ProtocolVersion>https://schemas.dmtf.org/wbem/wsman/1/wsman.xsd
    </wsmid:ProtocolVersion>
<wsmid:ProductVendor>Microsoft Corporation</wsmid:ProductVendor>
<wsmid:ProductVersion>OS: 6.0.5384 SP: 0.0 Stack:1.0</wsmid:ProductVersion>
</wsmid:IdentifyResponse>
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[О служба удаленного управления Windows](about-windows-remote-management.md)
</dt> <dt>

[Использование служба удаленного управления Windows](using-windows-remote-management.md)
</dt> <dt>

[Справочник по служба удаленного управления Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




