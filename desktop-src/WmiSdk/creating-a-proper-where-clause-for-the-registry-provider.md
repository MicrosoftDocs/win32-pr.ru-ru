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
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="ebc86-104">Создание предложения WHERE для поставщика реестра</span><span class="sxs-lookup"><span data-stu-id="ebc86-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="ebc86-105">Основные моменты, которые следует учитывать при создании правильного предложения WHERE для поставщика системного реестра, заключается в том, что каждый запрос события должен быть завершен и явным образом.</span><span class="sxs-lookup"><span data-stu-id="ebc86-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="ebc86-106">Сбой не завершен, а Explicit приведет к появлению сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ebc86-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="ebc86-107">Для завершения каждый запрос события в параметре *бстркуери* объекта [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) должен содержать предложение WHERE, включающее каждое из свойств в указанном классе событий.</span><span class="sxs-lookup"><span data-stu-id="ebc86-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="ebc86-108">В следующем примере показано, как задать *бстркуери* для регистрации событий изменения дерева в \_ \_ дереве " \\ программное обеспечение локального компьютера" hKey.</span><span class="sxs-lookup"><span data-stu-id="ebc86-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="ebc86-109">Чтобы быть явным, поставщик должен иметь возможность определить из запроса список возможных значений для каждого свойства в классе событий.</span><span class="sxs-lookup"><span data-stu-id="ebc86-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="ebc86-110">В следующем примере показан запрос события, который правильно регистрирует события изменения дерева.</span><span class="sxs-lookup"><span data-stu-id="ebc86-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="ebc86-111">Ниже приведен пример неправильной регистрации.</span><span class="sxs-lookup"><span data-stu-id="ebc86-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="ebc86-112">Поскольку невозможно оценить возможные значения для каждого свойства, WMI отклоняется с ошибкой WBEM \_ E \_ слишком \_ широким любым запросом, у которого нет предложения WHERE или если предложение WHERE слишком широко используется.</span><span class="sxs-lookup"><span data-stu-id="ebc86-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



