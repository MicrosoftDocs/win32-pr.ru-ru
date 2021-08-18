---
description: вы можете создать объект для WMI в Visual Basic scripting Edition (VBScript), подключившись к инструментарию wmi и вызывая CreateObject. В следующей таблице перечислены методы в API скриптов для WMI, которые поддерживают создание объектов.
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
ms.openlocfilehash: e86dbc649d5feab471485dbdf536cde911c139aeab3b6eb3323b24199438d1d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244574"
---
# <a name="creating-an-object-using-vbscript"></a>Создание объекта с помощью VBScript

вы можете создать объект для WMI в Visual Basic scripting Edition (VBScript), подключившись к инструментарию wmi и вызывая [CreateObject](/previous-versions//xzysf6hc(v=vs.85)). В следующей таблице перечислены методы в API скриптов для WMI, которые поддерживают создание объектов.



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

1.  Подключение WMI с помощью моникера или объекта [**SWbemLocator**](swbemlocator.md) .

    Дополнительные сведения см. [в разделе Создание скрипта WMI](creating-a-wmi-script.md).

2.  Выполните вызов метода [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

    В следующем примере кода показано, как создать объект.

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    Если вы используете моникер на шаге 1, вам не нужно повторно вызывать функцию [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

 

 
