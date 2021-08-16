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
ms.openlocfilehash: daa86bfd9975df5cd057dd3e577f443bafa6c363061e267e67adad69b590e678
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661084"
---
# <a name="registering-control-panel-items"></a>Регистрация элементов панели управления

Элементы панели управления должны быть зарегистрированы, чтобы они отображались в окне панели управления. Если элемент панели управления реализуется как часть файла .exe, то он регистрируется как объект команды. Регистрация отличается, если элемент реализуется как файл .dll, который экспортирует функцию [**кплапплет**](/windows/win32/api/cpl/nc-cpl-applet_proc) .

Конкретные требования обсуждаются в следующих разделах:

-   [Регистрация исполняемых элементов панели управления](how-to-register-an-executable-control-panel-item-registration-.md)
-   [Регистрация элементов панели управления DLL](how-to-register-dll-control-panel-item-registration-.md)

## <a name="related-topics"></a>Связанные темы

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

[доступ к панели управления в режиме Сейф в разделе Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
