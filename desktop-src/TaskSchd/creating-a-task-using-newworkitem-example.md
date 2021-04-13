---
title: Создание задачи с помощью примера Невворкитем
description: При создании задачи вы будете использовать два интерфейса планировщик задач Итасксчедулер и ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- создание рабочих элементов планировщик задач
- планировщик задач рабочих элементов, создание задач
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b4e0f05e76ea54b57a101e31515fe089c5f445c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338388"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Создание задачи с помощью примера Невворкитем

При создании задачи вы будете использовать два интерфейса планировщик задач: [**итасксчедулер**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) и [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Необходимо указать уникальное имя для задачи, идентификатор класса для объекта задачи и идентификатор интерфейса **ITask**. Идентификатор класса и идентификатор интерфейса показаны в примере кода, приведенном в этом разделе.

> [!Note]  
> Вы также можете создать задачу, вызвав [**итасксчедулер:: аддворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). При использовании этого маршрута вы обязаны создавать экземпляр объекта **Task** (который поддерживает интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ), а затем добавлять задачу с предоставленным именем.

 

> [!Note]  
> По умолчанию только члены группы «Администраторы», «операторы архива» или «операторы сервера» могут создавать задачи в Windows Server 2003. Член группы "Администраторы" может изменить дескриптор безопасности \\ папки задач Windows, чтобы разрешить другим пользователям создавать задачи.

 

Имя, указываемое для задачи, должно быть уникальным в папке запланированных задач. Если задача с таким именем уже существует, [**итасксчедулер:: невворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ВОЗВРАЩАЕТ \_ файл ошибки \_ . При получении этого возвращаемого значения следует указать другое имя и попытаться создать задачу еще раз.

В следующей процедуре описывается создание новой задачи рабочего элемента.

**Создание новой задачи рабочего элемента**

1.  Вызовите функцию [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) , чтобы инициализировать библиотеку COM и [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) для получения объекта планировщик задач. (В этом примере предполагается, что служба планировщик задач запущена).
2.  Вызовите [**итасксчедулер:: невворкитем**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) , чтобы создать новую задачу. (Этот метод возвращает указатель на интерфейс [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
3.  Сохраните новую задачу на диск, вызвав [**IPersistFile:: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (Интерфейс [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) является СТАНДАРТНЫМ COM-интерфейсом, поддерживаемым интерфейсом **ITask** .)
4.  Вызовите метод **ITask:: Release** , чтобы освободить все ресурсы. (Обратите внимание, что [**выпуск**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) — это метод [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) , наследуемый [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Пример кода  | См.                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Создание одной задачи | [Пример кода C/C++. Создание задачи с помощью Невворкитем](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Примеры планировщик задач 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 