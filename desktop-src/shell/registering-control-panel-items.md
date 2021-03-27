---
description: Элементы панели управления должны быть зарегистрированы, чтобы они отображались в окне панели управления.
title: Регистрация элементов панели управления
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6f21f223-a293-47b5-95e9-06b7a4ff1652
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 05c2a652314babc212e17b48198e9441f4d3465d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156690"
---
# <a name="registering-control-panel-items"></a>Регистрация элементов панели управления

Элементы панели управления должны быть зарегистрированы, чтобы они отображались в окне панели управления. Если элемент панели управления реализуется как часть exe-файла, то он регистрируется как объект команды. Регистрация различается, если элемент реализован как DLL-файл, который экспортирует функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

Конкретные требования обсуждаются в следующих разделах:

-   [Регистрация исполняемых элементов панели управления](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Регистрация элементов панели управления DLL](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>См. также

<dl> <dt>

[Элементы панели управления](control-panel-applications.md)
</dt> <dt>

[Руководство по работе пользователей](user-experience-guidelines.md)
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
</dt> <dt>

[Доступ к панели управления в защищенном режиме в Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
