---
title: Интерфейсы триггера
description: API-интерфейсы, используемые для управления триггерами, зависят от версии планировщик задач. Однако в обоих случаях эти API позволяют создавать новые триггеры, получать и обновлять существующие триггеры, а также удалять триггеры, которые больше не требуются.
ms.assetid: 94c11f11-72e2-404f-b396-ab7b1be71942
keywords:
- триггеры планировщик задач, интерфейсы
- триггеры планировщик задач, интерфейсы, описание
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5515f2b1e2f5b4a7694dec28bb8831c690da0d303cda53338714c1b0e03ddaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002195"
---
# <a name="trigger-interfaces"></a>Интерфейсы триггера

API-интерфейсы, используемые для управления триггерами, зависят от версии планировщик задач. Однако в обоих случаях эти API позволяют создавать новые триггеры, получать и обновлять существующие триггеры, а также удалять триггеры, которые больше не требуются.


Приложения, разработанные с помощью планировщик задач 2,0, могут использовать объекты и интерфейсы для создания, извлечения, изменения и удаления триггеров для задачи.

На следующем рисунке задача указывает коллекцию триггеров с помощью свойства Triggers. Эта коллекция содержит один или несколько отдельных API-интерфейсов триггеров с каждым API, указывающим конкретный тип триггера. Например, на рисунке ниже в коллекции триггеров содержится триггер загрузки, триггер входа и ежедневный триггер.

![интерфейсы триггера планировщика заданий 2,0](images/tsktri4.png)

### <a name="object-apis-for-scripting-development"></a>API объектов для разработки сценариев

Дополнительные сведения о методах и свойствах объектов, используемых для указания триггеров, см. в следующих статьях:

-   [**таскдефинитион**](taskdefinition.md)
-   [**тригжерколлектион**](triggercollection.md)
-   [**Триггер**](trigger.md)
-   [**буттригжер**](boottrigger.md)
-   [**даилитригжер**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**идлетригжер**](idletrigger.md)
-   [**логонтригжер**](logontrigger.md)
-   [**монслидовтригжер**](monthlydowtrigger.md)
-   [**монслитригжер**](monthlytrigger.md)
-   [**регистратионтригжер**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**виклитригжер**](weeklytrigger.md)

### <a name="interfaces-apis-for-c-development"></a>API интерфейсов для разработки на C++

Дополнительные сведения о методах и свойствах интерфейсов, используемых для указания триггеров, см. в следующих статьях:

-   [**итаскдефинитион**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
-   [**ITriggerCollection**](/windows/desktop/api/taskschd/nn-taskschd-itriggercollection)
-   [**итригжер**](/windows/desktop/api/taskschd/nn-taskschd-itrigger)
-   [**ибуттригжер**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)
-   [**идаилитригжер**](/windows/desktop/api/taskschd/nn-taskschd-idailytrigger)
-   [**иевенттригжер**](/windows/desktop/api/taskschd/nn-taskschd-ieventtrigger)
-   [**иидлетригжер**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger)
-   [**илогонтригжер**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)
-   [**имонслидовтригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlydowtrigger)
-   [**имонслитригжер**](/windows/desktop/api/taskschd/nn-taskschd-imonthlytrigger)
-   [**ирегистратионтригжер**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)
-   [**итиметригжер**](/windows/desktop/api/taskschd/nn-taskschd-itimetrigger)
-   [**ивиклитригжер**](/windows/desktop/api/taskschd/nn-taskschd-iweeklytrigger)

## <a name="task-scheduler-10-trigger-interfaces"></a>Интерфейсы триггеров планировщик задач 1,0

Существующие приложения, разработанные с помощью планировщик задач 1,0, могут использовать методы, доступные в интерфейсах планировщик задач 1,0 для создания, извлечения, изменения и удаления триггеров для [*рабочего элемента*](w.md). Однако обратите внимание, что все интерфейсы планировщик задач 1,0, перечисления и структуры устарели и не должны использоваться для разработки новых приложений.

На следующем рисунке показаны два интерфейса, которые используются для этого. Интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) используется для управления всеми триггерами, связанными с рабочим элементом (такое управление включает создание нового триггера для рабочего элемента). Интерфейс [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) используется для управления конкретным триггером.

![интерфейсы триггера планировщика заданий 1,0](images/tsktri2.png)

Интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) предоставляет методы для создания нового триггера для рабочего элемента, получения числа триггеров, связанных с рабочим элементом, получения [*структур триггеров*](t.md) , связанных с рабочим элементом, получения [*строк триггера*](t.md) , связанных с рабочим элементом, и для удаления триггеров.

После того как объект триггера будет доступен, можно использовать интерфейс [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) для получения структуры триггера и строки триггера, а также для установки критериев срабатывания триггера. Этот интерфейс используется только при работе с [*объектом триггера задачи*](t.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Триггеры задач](task-triggers.md)
</dt> <dt>

[Типы триггеров](trigger-types.md)
</dt> <dt>

[Структуры триггеров](trigger-structures.md)
</dt> </dl>

 

 