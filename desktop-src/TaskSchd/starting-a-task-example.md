---
title: Пример запуска задачи
description: Чтобы запустить задачу, вызовите метод Run интерфейса ITask. Запуск — это асинхронный метод, который пытается выполнить задачу и возвращает значение сразу после запуска задачи. Для выполнения этого метода должна быть запущена служба планировщик задач.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4176bf793e72acd3930d6e1e5cbc3d73e91c1d558e342a5a9804aa8f87526cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139337"
---
# <a name="starting-a-task-example"></a>Пример запуска задачи

Чтобы запустить задачу, вызовите метод [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) интерфейса [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . **Запуск** — это асинхронный метод, который пытается выполнить задачу и возвращает значение сразу после запуска задачи. Для выполнения этого метода должна быть запущена служба планировщик задач.

В следующей процедуре описывается, как запустить задачу.

**Запуск задачи**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите метод [**итасксчедулер:: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) , чтобы получить интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) объекта Task. (Обратите внимание, что в этом примере возвращается задача "задача тестирования".)
3.  [**Выполните**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) вызов, чтобы запустить задачу. Обратите внимание, что этот метод наследуется интерфейсом [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Продолжайте обработку по мере необходимости.
5.  Вызовите метод **ITask:: Release** для освобождения ресурсов и [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) , чтобы отменить инициализацию COM. В этом примере вызывается [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) для освобождения указателя на интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Обратите внимание, что **выпуск** — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый **ITask**.)



| Пример кода    | См.                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Выполнение существующей задачи | [Пример кода C/C++: запуск задачи](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 