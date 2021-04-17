---
title: Создание предложения WHERE для поставщика реестра
description: Основные моменты, которые следует учитывать при создании правильного предложения WHERE для поставщика системного реестра, заключается в том, что каждый запрос события должен быть завершен и явным образом. Сбой не завершен, а Explicit приведет к появлению сообщения об ошибке.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104498057"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Создание предложения WHERE для поставщика реестра

Основные моменты, которые следует учитывать при создании правильного предложения WHERE для поставщика системного реестра, заключается в том, что каждый запрос события должен быть завершен и явным образом. Сбой не завершен, а Explicit приведет к появлению сообщения об ошибке.

Для завершения каждый запрос события в параметре *бстркуери* объекта [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) должен содержать предложение WHERE, включающее каждое из свойств в указанном классе событий.

В следующем примере показано, как задать *бстркуери* для регистрации событий изменения дерева в \_ \_ дереве " \\ программное обеспечение локального компьютера" hKey.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Чтобы быть явным, поставщик должен иметь возможность определить из запроса список возможных значений для каждого свойства в классе событий.

В следующем примере показан запрос события, который правильно регистрирует события изменения дерева.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Ниже приведен пример неправильной регистрации.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Поскольку невозможно оценить возможные значения для каждого свойства, WMI отклоняется с ошибкой WBEM \_ E \_ слишком \_ широким любым запросом, у которого нет предложения WHERE или если предложение WHERE слишком широко используется.

 

 



