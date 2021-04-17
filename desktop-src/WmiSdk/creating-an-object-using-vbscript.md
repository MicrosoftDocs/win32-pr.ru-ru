---
description: Вы можете создать объект для WMI в Visual Basic Scripting Edition (VBScript), подключившись к инструментарию WMI и вызывая CreateObject. В следующей таблице перечислены методы в API скриптов для WMI, которые поддерживают создание объектов.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Создание объекта с помощью VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497769"
---
# <a name="creating-an-object-using-vbscript"></a>Создание объекта с помощью VBScript

Вы можете создать объект для WMI в Visual Basic Scripting Edition (VBScript), подключившись к инструментарию WMI и вызывая [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). В следующей таблице перечислены методы в API скриптов для WMI, которые поддерживают создание объектов.



| Интерфейс                                        | ProgID:                             |
|--------------------------------------------------|------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)           | "Вбемскриптинг. SwbemDateTime"      |
| [**SWbemLocator**](swbemlocator.md)             | "Вбемскриптинг. SWbemLocator"       |
| [**свбемластеррор**](swbemlasterror.md)         | "Вбемскриптинг. SWbem. LastError"    |
| [**свбемобжектпас**](swbemobjectpath.md)       | "Вбемскриптинг. Свбемобжектпас"    |
| [**свбемнамедвалуесет**](swbemnamedvalueset.md) | "Вбемскриптинг. Свбемнамедвалуесет" |
| [**свбемрефрешер**](swbemrefresher.md)         | "Вбемскриптинг. Свбемрефрешер"     |
| [**свбемсинк**](swbemsink.md)                   | "Вбемскриптинг. Свбемсинк"          |



 

В следующей процедуре описывается создание объекта WMI с помощью VBScript.

**Создание объекта WMI с помощью VBScript**

1.  Подключитесь к инструментарию WMI с помощью моникера или объекта [**SWbemLocator**](swbemlocator.md) .

    Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md).

2.  Выполните вызов метода [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

    В следующем примере кода показано, как создать объект.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Если вы используете моникер на шаге 1, вам не нужно повторно вызывать функцию [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

 

 
