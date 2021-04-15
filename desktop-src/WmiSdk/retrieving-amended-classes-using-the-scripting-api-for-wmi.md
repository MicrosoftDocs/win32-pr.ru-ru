---
description: Если вы используете API скриптов для инструментария WMI для получения или хранения сведений о локализованном классе, укажите языковой стандарт как часть моникера.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Получение измененных классов с помощью API скриптов для WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701998"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a>Получение измененных классов с помощью API скриптов для WMI

Если вы используете API скриптов для инструментария WMI для получения или хранения сведений о локализованном классе, укажите языковой стандарт как часть моникера. Также можно указать имя локали в параметре *стрлокале* для метода [**SWbemLocator. коннектсервер**](swbemlocator-connectserver.md) . При чтении или записи измененных классов укажите, что необходимо использовать локализованные определения классов, указав [вбемфлагусеамендедкуалифиерс](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) в качестве флага для параметра *ифлагс* вызываемого метода. Для указания языкового стандарта PowerShell можно использовать параметр *-locale* в командлете [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) .

В следующем примере кода показано, как получить локализованный класс с помощью моникера скрипта WMI или параметра-Locale.


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





В следующем примере кода показано, как задать параметр locale и использовать флаг [вбемфлагусеамендедкуалифиерс](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> Поскольку обратный вызов приемника может не возвращаться на том же уровне проверки подлинности, что и клиент, рекомендуется использовать семисинчронаус вместо асинхронного взаимодействия. Дополнительные сведения см. [в разделе вызов метода](calling-a-method.md).

 

В следующей таблице перечислены методы, принимающие флаг [вбемфлагусеамендедкуалифиерс](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) .



| Синхронный метод                                                 | Асинхронный метод                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SWbemServices. Субклассесоф**](swbemservices-subclassesof.md)   | [**SWbemServices. Субклассесофасинк**](swbemservices-subclassesofasync.md)   |
| [**SWbemObject. подклассы\_**](swbemobject-subclasses-.md)        | [**SWbemObject. Субклассесасинк\_**](swbemobject-subclassesasync-.md)        |
| [**SWbemServices. Инстанцесоф**](swbemservices-instancesof.md)     | [**SWbemServices. Инстанцесофасинк**](swbemservices-instancesofasync.md)     |
| [**SWbemObject. Instances\_**](swbemobject-instances-.md)          | [**SWbemObject. Инстанцесасинк\_**](swbemobject-instancesasync-.md)          |
| [**SWbemServices.ExeКкуери**](swbemservices-execquery.md)         | [**SWbemServices.ExeКкуерясинк**](swbemservices-execqueryasync.md)         |
| [**SWbemServices. Get**](swbemservices-get.md)                     | [**SWbemServices. Async**](swbemservices-getasync.md)                     |
| [**SWbemObject. размещение\_**](swbemobject-put-.md)                      | [**SWbemObject. Путасинк\_**](swbemobject-putasync-.md)                      |
| [**SWbemServices. Референцесто**](swbemservices-referencesto.md)   | [**SWbemServices. Референцестоасинк**](swbemservices-referencestoasync.md)   |
| [**SWbemObject. References\_**](swbemobject-references-.md)        | [**SWbemObject. Референцесасинк\_**](swbemobject-referencesasync-.md)        |
| [**SWbemServices. АссоЦиаторсоф**](swbemservices-associatorsof.md) | [**SWbemServices. АссоЦиаторсофасинк**](swbemservices-associatorsofasync.md) |
| [**SWbemObject. соединители\_**](swbemobject-associators-.md)      | [**SWbemObject. АссоЦиаторсасинк\_**](swbemobject-associatorsasync-.md)      |



 

 

 
