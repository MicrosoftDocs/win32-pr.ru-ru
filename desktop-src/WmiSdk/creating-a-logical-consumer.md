---
description: Логический потребитель — это экземпляр класса постоянного потребителя событий.
ms.assetid: fd984de8-0fe6-4b32-8e8c-4e2db84b4cc0
ms.tgt_platform: multiple
title: Создание логического потребителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dcbd62f2eee57a9e254d5700344d7b8da414469
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712773"
---
# <a name="creating-a-logical-consumer"></a>Создание логического потребителя

Логический потребитель — это экземпляр класса постоянного потребителя событий. Основное назначение логического потребителя — предоставить физическому потребителю параметры для действий, выполняемых физическим потребителем. Дополнительные сведения см. [в разделе Создание нового класса постоянного потребителя событий](creating-a-new-permanent-event-consumer-class.md). Постоянный потребитель должен иметь тот же [**креаторсид**](--eventconsumer.md) в экземплярах объекта-получателя, фильтра и привязки. Дополнительные сведения см. в статье [безопасное получение событий](receiving-events-securely.md). Пример использования логического потребителя см. в разделе [выполнение скрипта на основе события](running-a-script-based-on-an-event.md), в котором показано использование стандартного класса потребителя [**активескриптевентконсумер**](activescripteventconsumer.md) для настройки постоянного потребителя.

В следующей процедуре описывается создание логического потребителя.

**Создание логического потребителя**

1.  Создайте экземпляр класса постоянного потребителя.
2.  Заполните свойства экземпляра параметрами действия, которое должен выполнить физический потребитель.

В следующем примере кода MOF описывается логический потребитель, содержащий скрипт.

``` syntax
#pragma namespace("\\\\.\\root\\subscription")

instance of ActiveScriptEventConsumer as $CONSUMER
{
    Name = "MyConsumerName";
    ScriptingEngine = "VBScript";
    ScriptText = 

        "Set objFS = CreateObject(\"Scripting.FileSystemObject\")\n"
        "Set objFile = objFS.OpenTextFile(\"C:\\\\ASEC.log\", 8, true);\n"
        "objFile.WriteLine \"Time: \" + new Date() + \";\n"
        "objFile.WriteLine \"Entry made by: \\\"ActiveScript\\\"\";\n"
        "objFile.Close\n";
    
    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

После создания логического потребителя необходимо связать каждый фильтр с фильтром событий, чтобы назначить действие конкретному событию. Дополнительные сведения см. в разделе [Создание фильтра событий](creating-an-event-filter.md).

 

 



