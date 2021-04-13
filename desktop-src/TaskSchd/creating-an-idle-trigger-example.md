---
title: Пример создания триггера Idle
description: Чтобы создать триггер простоя, необходимо указать триггер простоя при создании триггера, а также задать время простоя для задачи. Сведения об условиях простоя см. в разделе условия простоя задачи.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a7f8333c79d05dfade609f028f93a816e61adf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338529"
---
# <a name="creating-an-idle-trigger-example"></a>Пример создания триггера Idle

Чтобы создать триггер простоя, необходимо указать триггер простоя при создании триггера, а также задать время простоя для задачи. Сведения об условиях простоя см. в разделе [условия простоя задачи](task-idle-conditions.md).

После создания триггера просто вызовите [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) , чтобы сохранить новый триггер на диск.

В следующей процедуре описывается создание триггера Idle для известной задачи.

**Создание триггера Idle для известной задачи**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task. (Обратите внимание, что в этом примере возвращается задача "задача тестирования".)
3.  Вызовите [**сетидлеваит**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) , чтобы указать, как долго система должна оставаться в состоянии простоя, прежде чем будет срабатывать триггер. (Обратите внимание, что **сетидлеваит** наследуется от [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Определите структуру [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) и вызовите [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) , чтобы создать триггер Idle. (Обратите внимание, что **CreateTrigger** наследуется от [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
5.  Сохраните задачу с новым триггером бездействия на диск с помощью [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
6.  Вызовите метод **ITask:: Release** , чтобы освободить все ресурсы. (Обратите внимание, что [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Пример кода                         | См.                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Создание триггера Idle для существующей задачи | [Пример кода C/C++. Создание триггера Idle](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 