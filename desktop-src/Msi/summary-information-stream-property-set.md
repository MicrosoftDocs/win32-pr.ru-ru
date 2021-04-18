---
description: В следующей таблице показан набор свойств потока сводных данных, в который входят свойства, соответствующие идентификаторы свойств, PID и типы.
ms.assetid: a5dd014f-21af-41f9-be75-1b139946179d
title: Набор свойств потока сводных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3929e4180a85a8f154c0a0352ddd1f9a052769ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674494"
---
# <a name="summary-information-stream-property-set"></a>Набор свойств потока сводных данных

В следующей таблице показан набор свойств потока сводных данных, в который входят свойства, соответствующие идентификаторы свойств, PID и типы. Дополнительные сведения об использовании этих свойств установщиком см. в разделе [описания свойств сводки](summary-property-descriptions.md). Сведения о функциях установщика окон, которые используются для настройки свойств сводных данных, см. [в разделе использование информационного потока сводки](using-the-summary-information-stream.md).



| Имя свойства                                                | Идентификатор свойства        | ИД процесса | Тип         |
|--------------------------------------------------------------|--------------------|-----|--------------|
| [**Страница**](codepage-summary.md)                         | \_кодовая страница PID      | 1   | VT \_ I2       |
| [**Заголовок**](title-summary.md)                               | \_название PID         | 2   | VT \_ LPSTR    |
| [**Субъект**](subject-summary.md)                           | \_Тема PID       | 3   | VT \_ LPSTR    |
| [**Автор**](author-summary.md)                             | \_Автор PID        | 4   | VT \_ LPSTR    |
| [**Keywords**](keywords-summary.md)                         | \_Ключевые слова PID      | 5   | VT \_ LPSTR    |
| [**Комментарии**](comments-summary.md)                         | \_Комментарии PID      | 6   | VT \_ LPSTR    |
| [**Шаблон**](template-summary.md)                         | \_шаблон PID      | 7   | VT \_ LPSTR    |
| [**Автор последнего сохранения**](last-saved-by-summary.md)               | Идентификатор процесса \_ ластаусор    | 8   | VT \_ LPSTR    |
| [**Номер редакции**](revision-number-summary.md)           | Идентификатор процесса \_ ревнумбер     | 9   | VT \_ LPSTR    |
| [**Последняя печать**](last-printed-summary.md)                 | Идентификатор процесса \_ ластпринтед   | 11  | VT \_ fileTime |
| [**Создать дату и время**](create-time-date-summary.md)         | PID \_ Create \_ DTM   | 12  | VT \_ fileTime |
| [**Время и Дата последнего сохранения**](last-saved-time-date-summary.md)  | PID \_ ластсаве \_ DTM | 13  | VT \_ fileTime |
| [**Число страниц**](page-count-summary.md)                     | Идентификатор процесса \_ PAGECOUNT     | 14  | VT \_ I4       |
| [**Число слов**](word-count-summary.md)                     | номер процесса \_ WORDCOUNT     | 15  | VT \_ I4       |
| [**Число символов**](character-count-summary.md)           | Идентификатор идентификатора \_ CHARCOUNT     | 16  | VT \_ I4       |
| [**Создание приложения**](creating-application-summary.md) | PID \_ APPNAME       | 18  | VT \_ LPSTR    |
| [**Безопасность**](security-summary.md)                         | \_Безопасность PID      | 19  | VT \_ I4       |



 

В настоящее время установщик поддерживает три формата хранения пакетов установки, преобразований и пакетов исправлений. Идентификатору CLSID для хранилища присваивается соответствующий класс формата для конкретного формата, независимо от сводных данных для хранилища.

 

 



