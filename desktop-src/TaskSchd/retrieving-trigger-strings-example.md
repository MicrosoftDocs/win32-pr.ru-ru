---
title: Пример получения строк триггера
description: Вы можете получить строки триггера известного триггера, используя интерфейс Исчедуледворкитем или Итасктригжер, в зависимости от типа объекта, с которым вы работаете.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- Получение строк триггера планировщик задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68a05f95f19aaa68927059c87f7a73f162266454137fbe088923b25dce7ed3ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002382"
---
# <a name="retrieving-trigger-strings-example"></a>Пример получения строк триггера

Вы можете получить строки триггера известного триггера, используя интерфейс [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) или [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , в зависимости от типа объекта, с которым вы работаете.

При работе с [*объектом Task*](t.md)используйте методы интерфейса [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) для получения строк триггера рабочего элемента.

При работе с [*объектом триггера задачи*](t.md)используйте методы интерфейса [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , чтобы получить строку триггера триггера.

В следующем примере показано, как использовать [**исчедуледворкитем:: жеттригжерстринг**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) для отображения строк всех триггеров, связанных с известной задачей.

В следующей процедуре описывается получение строк триггера задачи.

**Получение строк триггера задачи**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task. (Обратите внимание, что в этом примере возвращается задача "задача тестирования".)
3.  Вызовите метод **ITask:: жеттригжеркаунт** , чтобы узнать, сколько триггеров связано с задачей. (Обратите внимание, что [**жеттригжеркаунт**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) — это метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Отобразить строки триггера, вызвав **ITask:: жеттригжерстринг** для каждого триггера, связанного с задачей. (Обратите внимание, что [**жеттригжерстринг**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) — это метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
5.  Освободите все ресурсы. Вызовите [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) , чтобы освободить строки триггера и **ITask:: Release** , чтобы освободить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Обратите внимание, что [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый **ITask**.)



| Пример кода                                                         | См.                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Получение строки триггера для всех триггеров, связанных с известной задачей | [Пример кода. Получение строк триггера](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 