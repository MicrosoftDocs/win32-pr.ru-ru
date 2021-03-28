---
description: По умолчанию элементы панели управления Windows Vista не отображаются при работе Windows в защищенном режиме.
title: Доступ к панели управления в защищенном режиме
ms.topic: article
ms.date: 05/31/2018
ms.assetid: f37bcb0f-9417-4cc4-a57d-4f67a9ccda19
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 0f7a401bbc22a7f8de3618f844bfe463fa3baa50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984368"
---
# <a name="accessing-the-control-panel-in-safe-mode"></a>Доступ к панели управления в защищенном режиме

По умолчанию элементы панели управления Windows Vista не отображаются при работе Windows в защищенном режиме. Чтобы разрешить просмотр нового элемента панели управления в защищенном режиме, можно задать значения реестра, соответствующие типу элемента. Значения интерпретируется следующим образом:



| Значение | Значение                                                            |
|-------|--------------------------------------------------------------------|
| 1     | Элемент должен отображаться только в режиме минимального безопасного режима.                  |
| 2     | Элемент должен отображаться в защищенном режиме только при включенной сети. |
| 3     | Элемент всегда должен отображаться в любом формате безопасного режима.            |



 

В этом примере показаны записи, необходимые для элемента, реализованного в виде файла. cpl или. dll. Он указывает, что элемент должен отображаться в защищенном режиме с сетевыми подключениями.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.EnableInSafeMode
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 2
```

В этом примере показаны записи, необходимые для элемента, реализованного в виде EXE-файла. Он указывает, что элемент должен отображаться в любой форме безопасного режима.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         System.ControlPanel.EnableInSafeMode = [REG_DWORD] 3
```

## <a name="related-topics"></a>См. также

<dl> <dt>

[Элементы панели управления](control-panel-applications.md)
</dt> <dt>

[Руководство по работе пользователей](user-experience-guidelines.md)
</dt> <dt>

[Регистрация элементов панели управления](registering-control-panel-items.md)
</dt> <dt>

[Использование Кплапплет](using-cplapplet.md)
</dt> <dt>

[Обработка сообщений в панели управления](message-processing.md)
</dt> <dt>

[Исполнение элементов панели управления](executing-control-panel-items.md)
</dt> <dt>

[Расширение элементов панели управления "система"](extending-system-control-panel-items.md)
</dt> <dt>

[Назначение категорий панели управления](assigning-control-panel-categories.md)
</dt> <dt>

[Создание ссылок на задачи с возможностью поиска для элемента панели управления](creating-searchable-task-links.md)
</dt> </dl>

 

 



