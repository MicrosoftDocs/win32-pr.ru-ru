---
title: T (планировщик задач)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d4c6d7ba-7bca-420d-a4dc-4daea816f99c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2730cdbe3a13456aed0e613a614d43a0e56e6673
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104533668"
---
# <a name="t-task-scheduler"></a>T (планировщик задач)

A B C D [E](e.md) F G р [. J K](i.md) L M N O [P](p.md) Q R [S](s.md) T U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_task_objects_gly"></span><span id="_MSB_TASK_OBJECTS_GLY"></span>**объекты Task**
</dt> <dd>

Экземпляры объекта, предоставляющие методы для управления задачами. Сюда входят методы установки и извлечения свойств. выполнение, остановка и удаление задач; и создание новых триггеров и получение старых триггеров.

Объект Task создается вызовами методов [**исчедуледворкитем:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) и [**исчедуледворкитем::**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger)GetObject.

</dd> <dt>

<span id="_msb_task_scheduler_objects_gly"></span><span id="_MSB_TASK_SCHEDULER_OBJECTS_GLY"></span>**объекты планировщика заданий**
</dt> <dd>

Экземпляры объекта, представляющие службу планировщик задач. Этот объект поддерживает два интерфейса: **IUnknown** и [**итасксчедулер**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) (в настоящее время это только рабочие элементы, поддерживаемые службой планировщик задач).

Объекты планировщика задач создаются вызовами метода **CoCreateInstance**.

</dd> <dt>

<span id="_msb_task_trigger_objects_gly"></span><span id="_MSB_TASK_TRIGGER_OBJECTS_GLY"></span>**объекты триггеров задач**
</dt> <dd>

Экземпляры объекта предоставляет методы для установки и извлечения триггеров задач. Этот объект поддерживает два интерфейса: **IUnknown** и [**итасктригжер**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger).

Объекты триггеров задач создаются вызовами методов [**исчедуледворкитем:: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) и [**Исчедуледворкитем:: Trigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettrigger).

См. также: *триггеры*.

</dd> <dt>

<span id="_msb_tasks_gly"></span><span id="_MSB_TASKS_GLY"></span>**операции**
</dt> <dd>

Любой элемент, который может выполняться планировщик задач. Эти элементы могут включать любое из следующих элементов (как поддерживается операционной системой, в которой будет выполняться задача): Win32® приложениями, приложениями Win16, приложениями OS/2, приложениями MS-DOS®, пакетными файлами ( \* bat), командными файлами ( \* cmd) или любым надлежащим образом зарегистрированным типом файлов.

</dd> <dt>

<span id="_msb_tasks_folder_gly"></span><span id="_MSB_TASKS_FOLDER_GLY"></span>**Папка Tasks**
</dt> <dd>

Папка, в которой перечислены все файлы задач (в настоящее время задачи являются единственными доступными рабочими элементами). Эти файлы содержат сведения о задаче. Имена этих файлов отражают имя задачи.

Расположение папки Tasks можно извлечь из реестра, получая данные следующего значения:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         SchedulingAgent
            TasksFolder
```

</dd> <dt>

<span id="_msb_triggers_gly"></span><span id="_MSB_TRIGGERS_GLY"></span>**план**
</dt> <dd>

Набор критериев, которые при выполнении приведут к выполнению задачи. Планировщик задач предоставляет триггеры на основе времени и событий, которые могут указывать время запуска задачи, критерии повторения и другие параметры.

</dd> <dt>

<span id="_msb_trigger_strings_gly"></span><span id="_MSB_TRIGGER_STRINGS_GLY"></span>**строки триггера**
</dt> <dd>

Строка, описывающая триггер. Эта строка создается службой планировщик задач и отображается в пользовательском интерфейсе планировщик задач в форме, подобной "at 2PM каждый день, начиная с 5/11/97".

</dd> <dt>

<span id="_msb_trigger_structures_gly"></span><span id="_MSB_TRIGGER_STRUCTURES_GLY"></span>**структуры триггеров**
</dt> <dd>

Структура [**\_ триггера задачи**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) , используемая при задании или извлечении критериев, определяющих триггер. Критерий включает срабатывание триггера и тип триггера.

</dd> </dl>

 

 




