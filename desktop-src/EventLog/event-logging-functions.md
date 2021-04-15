---
description: Для ведения журнала событий используются следующие функции.
ms.assetid: fd5c12ec-3a3d-4b75-a573-0b27ae7a890b
title: Функции ведения журнала событий
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437899684861c5fc7ddbfe98c2499dc07bd9da8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683286"
---
# <a name="event-logging-functions"></a>Функции ведения журнала событий

Для ведения журнала событий используются следующие функции.



| Функция                                                         | Описание                                                                                         |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**баккупевентлог**](/windows/desktop/api/Winbase/nf-winbase-backupeventloga)                         | Сохраняет указанный журнал событий в файл резервной копии.                                                     |
| [**клеаревентлог**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga)                           | Очищает указанный журнал событий и при необходимости сохраняет текущую копию журнала в файл резервной копии.  |
| [**клосивентлог**](/windows/desktop/api/Winbase/nf-winbase-closeeventlog)                           | Закрывает маркер чтения для указанного журнала событий.                                                    |
| [**дерегистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-deregistereventsource)           | Закрывает маркер записи в указанный журнал событий.                                                   |
| [**жетевентлогинформатион**](/windows/desktop/api/Winbase/nf-winbase-geteventloginformation)         | Извлекает сведения о указанном журнале событий.                                                |
| [**жетнумберофевентлогрекордс**](/windows/desktop/api/Winbase/nf-winbase-getnumberofeventlogrecords) | Возвращает количество записей в указанном журнале событий.                                         |
| [**жетолдестевентлогрекорд**](/windows/desktop/api/Winbase/nf-winbase-getoldesteventlogrecord)       | Возвращает абсолютный номер записи самой старой записи в указанном журнале событий.               |
| [**нотифичанжеевентлог**](/windows/desktop/api/Winbase/nf-winbase-notifychangeeventlog)             | Позволяет приложению принимать уведомления при записи события в указанный журнал событий. |
| [**опенбаккупевентлог**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga)                 | Открывает обработчик для журнала событий резервного копирования.                                                               |
| [**опеневентлог**](/windows/desktop/api/Winbase/nf-winbase-openeventloga)                             | Открывает обработчик для указанного журнала событий.                                                          |
| [**реадевентлог**](/windows/desktop/api/Winbase/nf-winbase-readeventloga)                             | Считывает целое число записей из указанного журнала событий.                                       |
| [**регистеревентсаурце**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea)               | Извлекает зарегистрированный обработчик в указанный журнал событий.                                           |
| [**репортевент**](/windows/desktop/api/Winbase/nf-winbase-reporteventa)                               | Записывает запись в конец указанного журнала событий.                                              |



 

 

 



