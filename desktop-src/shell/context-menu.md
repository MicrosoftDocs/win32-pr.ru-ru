---
description: В этом разделе обсуждается создание контекстных меню (контекстных) и реализация обработчиков контекстного меню (глагола).
title: Контекстное меню (контекст) и обработчики контекстного меню
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 956f3b10-2bc6-4f1f-a6ed-7184f94b545a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 286dd9c860ae79e5124439439da97f206b4aa436
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262916"
---
# <a name="shortcut-context-menus-and-shortcut-menu-handlers"></a>Контекстное меню (контекст) и обработчики контекстного меню

В этом разделе обсуждается создание контекстных меню (контекстных) и реализация обработчиков контекстного меню (глагола).

Этот раздел по типам файлов и сопоставлению файлов организован следующим образом:

-   [Команды и сопоставления файлов](fa-verbs.md)
-   [Выбор метода статического или динамического контекстного меню](shortcut-choose-method.md)
-   [Рекомендации по работе с обработчиками контекстного меню и несколькими командами](verbs-best-practices.md)
-   [Создание обработчиков контекстного меню](context-menu-handlers.md)
-   [Создание статических каскадных меню](creating-static-cascading-menus.md)
-   [Как подавлять и контролировать видимость команд](how-to-suppress-and-control-visibility.md)
-   [Как применить модель выбора глагола](how-to-employ-the-verb-selection-model.md)
-   [Использование атрибутов элементов](how-to-use-item-attributes.md)
-   [Реализация пользовательских команд для папок с помощью Desktop.ini](how-to-implement-custom-verbs-for-folders-through-desktop-ini.md)
-   [Настройка контекстного меню с помощью динамических команд](shortcut-menu-using-dynamic-verbs.md)
-   [Реализация интерфейса IContextMenu](how-to-implement-the-icontextmenu-interface.md)
-   [Справочник по контекстному меню](context-menu-reference.md)

## <a name="additional-resources"></a>Дополнительные ресурсы

Дополнительные сведения о концептуальном плане см. в следующих разделах:

-   [Общие сведения о сопоставлениях файлов](fa-intro.md).
-   Сведения о расширении оболочки с помощью обработчиков типов файлов см. в разделе [Создание обработчиков расширений оболочки](handlers.md).
-   Сведения о создании хранилища данных оболочки см. в разделе [реализация базовых интерфейсов объекта папки](nse-implement.md).

Связанные справочные документации по см. в следующих разделах:

-   Инструкции по выполнению команды для элемента оболочки см. в описании метода [**инвокеверб**](folderitem-invokeverb.md) .
-   Чтобы получить коллекцию команд, которые могут быть выполнены в элементе оболочки, см. метод [**Verbs**](folderitem-verbs.md) .
-   Сведения о выполнении операции с указанным файлом см. в разделе функции [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) или [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) .

 

 



