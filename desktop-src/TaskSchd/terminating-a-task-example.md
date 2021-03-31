---
title: Пример завершения задачи
description: Задачу можно завершить во время ее выполнения, вызвав Исчедуледворкитем Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104260956"
---
# <a name="terminating-a-task-example"></a>Пример завершения задачи

Задачу можно завершить во время ее выполнения, вызвав метод [**исчедуледворкитем:: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).

Следующая процедура описывает, как завершить задачу, если она запущена.

**Завершение задачи, если она запущена**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task. (Обратите внимание, что в этом примере возвращается задача "задача тестирования".)
3.  Вызовите **ITask::-Status** , чтобы определить, запущена ли задача. (Обратите [**внимание, что параметром**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) является метод, наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Проверьте состояние задачи, а затем вызовите **ITask:: Terminate** , если задача запущена. (Обратите внимание, что [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) — это метод [**исчедуледворкитем**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Пример кода                | См.                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Проверка состояния известной задачи | [Пример кода C/C++: завершение задачи](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 