---
description: Приложение может искать в текущем каталоге все имена файлов, соответствующие заданному шаблону, с помощью функций FindFirstFile, Финдфирстфиликс, FindNextFile и Финдклосе.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Поиск одного или нескольких файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682916"
---
# <a name="searching-for-one-or-more-files"></a>Поиск одного или нескольких файлов

Приложение может искать в текущем каталоге все имена файлов, соответствующие заданному шаблону, с помощью функций [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)и [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) . Шаблон должен быть допустимым именем файла и может содержать подстановочные знаки.

Функции [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) создают дескрипторы, которые **финдфирстфиликс** использует для поиска других файлов с тем же шаблоном. Все функции возвращают сведения о найденном файле. Эти сведения включают имя файла, его размер, атрибуты и время.

Функция [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) также позволяет приложению искать файлы на основе дополнительных условий поиска. Функция может ограничить поиск именами устройств или каталогов.

Функция [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) уничтожает дескрипторы, созданные с помощью [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).

Приложение может выполнять поиск одного файла по указанному пути с помощью функции [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .

 

 
