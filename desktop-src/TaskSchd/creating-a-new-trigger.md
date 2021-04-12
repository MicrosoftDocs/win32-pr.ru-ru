---
title: Создание нового триггера
description: Для создания триггера необходимо использовать три интерфейса.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f48ecb7b06e5bade6d5ad80e4c9a82794f6a17e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413324"
---
# <a name="creating-a-new-trigger"></a>Создание нового триггера

Для создания триггера необходимо использовать три интерфейса. [**Исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) предоставляет метод [**Исчедуледворкитем:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) для создания объекта Trigger, [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) предоставляет метод [**итасктригжер:: сеттригжер**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) для установки критериев триггера, а COM-интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) предоставляет метод **Save** для сохранения нового триггера на диск.

В следующей процедуре описывается создание нового триггера.

**Создание нового триггера**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task. (Обратите внимание, что в этом примере возвращается задача "задача тестирования".)
3.  Вызовите [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) , чтобы создать объект триггера. (Обратите внимание, что [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) наследуется от [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Определите структуру [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Обратите внимание, что для членов **\_ триггера задачи** вбегиндай, вбегинмонс и вбегинеар должен быть задан допустимый день, месяц и год соответственно.
5.  Вызовите [**итасктригжер:: сеттригжер**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) , чтобы задать критерии триггера.
6.  Сохраните задачу с новым триггером на диск с помощью [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
7.  Вызовите [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) , чтобы освободить все ресурсы. (Обратите внимание, что **выпуск** — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Пример кода                       | См.                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Создание нового триггера для существующей задачи | [Пример кода C/C++: Создание триггера задачи](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 