---
description: Описывает соглашения о документе для чтения разделов API сценариев WMI.
ms.assetid: 889e6322-96f6-4a24-a084-e3b7bfa94a40
ms.tgt_platform: multiple
title: Соглашения о документе для API скриптов
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 33335982672472fa9924a6e250305a3630628b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346742"
---
# <a name="document-conventions-for-the-scripting-api"></a>Соглашения о документе для API скриптов

[API скриптов для WMI](scripting-api-for-wmi.md) Reference использует следующие соглашения о документе:

-   Типы параметров определяются с помощью префикса: b (логическое значение), str (строка), I (целое число), obj (объект автоматизации), var (Variant).
-   Необязательные параметры помещаются в квадратные скобки со значениями по умолчанию, которые отображаются по назначению.
-   В случае с параметрами объекта символы после префикса "obj" указывают тип ожидаемого объекта.



| Параметр объекта      | Тип объекта                                          |
|-----------------------|------------------------------------------------------|
| *вбемдатетиме*        | [**SWbemDateTime**](swbemdatetime.md)               |
| *вбемевентсаурце*     | [**свбемевентсаурце**](swbemeventsource.md)         |
| *вбемлокатор*         | [**SWbemLocator**](swbemlocator.md)                 |
| *вбеммесод*          | [**свбеммесод**](swbemmethod.md)                   |
| *вбеммесодсет*       | [**свбеммесодсет**](swbemmethodset.md)             |
| *вбемнамедвалуесет*   | [**свбемнамедвалуесет**](swbemnamedvalueset.md)     |
| *вбемобжект*          | [**SWbemObject**](swbemobject.md)                   |
| *вбемобжектекс*        | [**свбемобжектекс**](swbemobjectex.md)               |
| *вбемобжектпас*      | [**свбемобжектпас**](swbemobjectpath.md)           |
| *вбемобжектсет*       | [**SWbemObjectSet**](swbemobjectset.md)             |
| *вбемпривилеже*       | [**свбемпривилеже**](swbemprivilege.md)             |
| *вбемпривилежесет*    | [**свбемпривилежесет**](swbemprivilegeset.md)       |
| *вбемпроперти*        | [**SWbemProperty**](swbemproperty.md)               |
| *вбемпропертисет*     | [**SWbemPropertySet**](swbempropertyset.md)         |
| *вбемкуалифиер*       | [**свбемкуалифиер**](swbemqualifier.md)             |
| *вбемкуалифиерсет*    | [**свбемкуалифиерсет**](swbemqualifierset.md)       |
| *вбемрефрешаблеитем* | [**свбемрефрешаблеитем**](swbemrefreshableitem.md) |
| *вбемрефрешер*       | [**свбемрефрешер**](swbemrefresher.md)             |
| *вбемсервицес*        | [**SWbemServices**](swbemservices.md)               |
| *вбемсервицесекс*      | [**свбемсервицесекс**](swbemservicesex.md)           |



 

Например, в следующем коде показано, как можно присвоить имена переменным для различных типов объектов:


```VB
strComputerName  ' a string value for a computer name
bStatusFlag  ' a boolean value used for a status
objServices  ' an object value used to store an SWbemServices value
```



 

 



