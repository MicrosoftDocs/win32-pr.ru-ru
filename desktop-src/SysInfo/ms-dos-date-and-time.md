---
description: Дата и время MS-DOS — это Упакованные 16-разрядные значения, указывающие месяц, день, год и время суток последней записи в файл MS-DOS.
ms.assetid: 948e6d77-dd01-4c90-9ef0-af143972c3fa
title: Дата и время MS-DOS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84d401c731c9a3f5127511e28adf846c929a89a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662544"
---
# <a name="ms-dos-date-and-time"></a>Дата и время MS-DOS

**Дата** и **время** MS-DOS — это Упакованные 16-разрядные значения, указывающие месяц, день, год и время суток последней записи в файл MS-DOS. MS-DOS записывает дату и время, когда приложение MS-DOS создает или записывает в файл. Приложения MS-DOS извлекают эту дату и время с помощью функций MS-DOS. При использовании функции [**функции getFileTime**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletime) для извлечения времени файла для файлов, созданных MS-DOS, **функции getFileTime** автоматически преобразует даты и время MS-DOS в время в формате UTC.

При возникновении даты и времени MS-DOS, которые не были преобразованы, можно преобразовать ее в время на основе времени в формате UTC с помощью функции [**досдатетиметофилетиме**](/windows/desktop/api/Winbase/nf-winbase-dosdatetimetofiletime) . Эта функция копирует преобразованные дату и время в структуру [**fileTime**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) . Значение можно преобразовать обратно в дату и время MS-DOS с помощью функции [**филетиметодосдатетиме**](/windows/desktop/api/Winbase/nf-winbase-filetimetodosdatetime) .

 

 
