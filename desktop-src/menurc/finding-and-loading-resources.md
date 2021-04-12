---
title: Поиск и загрузка ресурсов
description: В этом разделе описывается загрузка ресурса в память.
ms.assetid: 9e56cfdd-b365-4433-a507-a30220b4a92d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca9590927cad28772a6b4a5b761d74c9ebf101a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487576"
---
# <a name="finding-and-loading-resources"></a>Поиск и загрузка ресурсов

Перед использованием ресурса приложение должно загрузить его в память. Функции [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) и [**финдресаурцеекс**](/windows/desktop/api/Winbase/nf-winbase-findresourceexa) находят ресурс в модуле и возвращают маркер в двоичные данные ресурса. **FindResource** находит ресурс по типу и имени. **Финдресаурцеекс** находит ресурс по типу, имени и языку. Сведения о **FindResource** в этом разделе также применимы к **финдресаурцеекс**.

Функция [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) использует для загрузки ресурса в память маркер ресурса, возвращенный [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) . После того как приложение загрузит ресурс с помощью **лоадресаурце**, система выгрузит связанную память только в том случае, если все ссылки на его модуль освобождаются через [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Приложения, которым требуется многократный доступ к одному или нескольким ресурсам в рамках определенного модуля, могут повлечь за собой снижение производительности из-за того, что сопоставление памяти выполняется в повторяющихся вызовах [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и **FreeLibrary** . Приложения должны хранить один обработчик модуля, пока ресурсы больше не нужны, а затем вызываю **FreeLibrary**. После выгрузки модуля из памяти дескрипторы ресурсов становятся недействительными.

Приложение может использовать [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) и [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) для поиска и загрузки ресурсов любого типа, но эти функции следует использовать только в одной из следующих ситуаций:

-   Если приложение не может получить доступ к ресурсу с помощью существующей функции для конкретного ресурса.
-   Когда приложение должно получить доступ к ресурсу как к двоичным данным для последующих вызовов функций.

По возможности для поиска и загрузки ресурсов в одном вызове приложению следует использовать одну из следующих функций для конкретного ресурса:



| Функция                                     | Действие                                   | Удаление ресурса                                                                                               |
|----------------------------------------------|------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage)      | Загружает и форматирует запись в таблице сообщений. | Никаких действий не требуется.                                                                                                |
| [**лоадакцелераторс**](/windows/desktop/api/Winuser/nf-winuser-loadacceleratorsa) | Загружает таблицу сочетаний клавиш.              | [**дестройакцелератортабле**](/windows/desktop/api/Winuser/nf-winuser-destroyacceleratortable)                                                       |
| [**лоадбитмап**](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)             | Загружает ресурс точечного рисунка.                 | [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject)                                                                             |
| [**лоадкурсор**](/windows/desktop/api/Winuser/nf-winuser-loadcursora)             | Загружает ресурс курсора.                 | [**дестройкурсор**](/windows/desktop/api/Winuser/nf-winuser-destroycursor)                                                                           |
| [**лоадикон**](/windows/desktop/api/Winuser/nf-winuser-loadicona)                 | Загружает ресурс значка.                  | [**дестройикон**](/windows/desktop/api/Winuser/nf-winuser-destroyicon)                                                                               |
| [**лоадимаже**](/windows/desktop/api/Winuser/nf-winuser-loadimagea)               | Загружает значок, курсор или точечный рисунок.        | [**Дестройикон**](/windows/desktop/api/Winuser/nf-winuser-destroyicon), [**дестройкурсор**](/windows/desktop/api/Winuser/nf-winuser-destroycursor), [**DeleteObject**](/windows/desktop/api/wingdi/nf-wingdi-deleteobject) |
| [**лоадмену**](/windows/desktop/api/Winuser/nf-winuser-loadmenua)                 | Загружает ресурс меню.                   | [**дестроймену**](/windows/desktop/api/Winuser/nf-winuser-destroymenu)                                                                               |
| [**лоадстринг**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)             | Загружает запись строки таблицы.              | Никаких действий не требуется.                                                                                                |



 

Обратите внимание на функции выпуска, приведенные в таблице выше. Перед завершением работы приложение должно освободить память, занятую таблицами ускорителя, точечными рисунками, курсорами, значками и меню, с помощью соответствующих функций.

Память, связанная с ресурсами, загруженными с помощью [**FindResource**](/windows/desktop/api/Winbase/nf-winbase-findresourcea) и [**лоадресаурце**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) , будет освобождена после выгрузки модуля с помощью вызова [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary). Все ресурсы, которые остаются Выгруженными при завершении работы приложения, будут автоматически освобождены системой.

 

 