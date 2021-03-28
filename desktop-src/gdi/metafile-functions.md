---
description: Для метафайлов с улучшенными форматами используются следующие функции.
ms.assetid: 93a17a8c-308b-4442-933e-fedc8b9a84b0
title: Функции Metafile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd137095fe0659871291ec4e8670054cc2899d10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544447"
---
# <a name="metafile-functions"></a>Функции Metafile

Для метафайлов с улучшенными форматами используются следующие функции.



| Функция                                                             | Описание                                                                                                            |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| [**клосинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-closeenhmetafile)                         | Закрывает контекст устройства расширенного метафайла.                                                                            |
| [**копенхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-copyenhmetafilea)                           | Копирует содержимое метафайла расширенного формата в указанный файл.                                                |
| [**креатинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-createenhmetafilea)                       | Создает контекст устройства для расширенного формата метафайла.                                                              |
| [**делетинхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-deleteenhmetafile)                       | Удаляет метафайл с расширенным форматом или расширенный формат метафайлов.                                             |
| [**енхметафилепрок**](/windows/win32/api/wingdi/nc-wingdi-enhmfenumproc)                           | Определяемая приложением функция обратного вызова, используемая с функцией Енуменхметафиле.                                       |
| [**енуменхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-enumenhmetafile)                           | Перечисляет записи в метафайле с расширенным форматом.                                                             |
| [**гдикоммент**](/windows/desktop/api/Wingdi/nf-wingdi-gdicomment)                                     | Копирует комментарий из буфера в заданный метафайл расширенного формата.                                              |
| [**жетенхметафиле**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea)                             | Создает маркер, который определяет метафайл в формате EMF, хранящийся в указанном файле.                            |
| [**жетенхметафилебитс**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilebits)                     | Извлекает содержимое указанного метафайла расширенного формата и копирует их в буфер.                        |
| [**жетенхметафиледескриптион**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafiledescriptiona)       | Извлекает необязательное текстовое описание из метафайла расширенного формата и копирует строку в указанный буфер. |
| [**жетенхметафилехеадер**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafileheader)                 | Извлекает запись, содержащую заголовок для указанного метафайла расширенного формата.                                 |
| [**жетенхметафилепалеттинтриес**](/windows/desktop/api/Wingdi/nf-wingdi-getenhmetafilepaletteentries) | Извлекает необязательные записи палитры из указанного расширенного метафайла.                                               |
| [**Метафайл**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilea)                                   | Параметр "EMF" больше не доступен для использования в Windows 2000. Вместо этого используйте [**жетенхметафиле**](/windows/desktop/api/WinGdi/nf-wingdi-getenhmetafilea).  |
| [**жетвинметафилебитс**](/windows/desktop/api/Wingdi/nf-wingdi-getwinmetafilebits)                     | Преобразует записи расширенного формата из метафайла в записи формата Windows.                                      |
| [**плайенхметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafile)                           | Отображает изображение, хранящееся в указанном метафайле Enhanced-Format.                                                 |
| [**плайенхметафилерекорд**](/windows/desktop/api/Wingdi/nf-wingdi-playenhmetafilerecord)               | Воспроизводит запись расширенного метафайла, выполняя функции интерфейса графических устройств (GDI), определяемые записью. |
| [**сетенхметафилебитс**](/windows/desktop/api/Wingdi/nf-wingdi-setenhmetafilebits)                     | Создает метафайл с расширенным форматом на основе памяти из указанных данных.                                               |
| [**сетвинметафилебитс**](/windows/desktop/api/Wingdi/nf-wingdi-setwinmetafilebits)                     | Преобразует метафайл из старого формата Windows в новый расширенный формат.                                          |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Следующие функции являются устаревшими. Предоставляются для совместимости с метафайлами Windows-Format.

-   [**клосеметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-closemetafile)
-   [**копиметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-copymetafilea)
-   [**креатеметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-createmetafilea)
-   [**делетеметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-deletemetafile)
-   [**енумметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-enummetafile)
-   [**енумметафилепрок**](/windows/win32/api/wingdi/nc-wingdi-mfenumproc)
-   [**жетметафилебитсекс**](/windows/desktop/api/Wingdi/nf-wingdi-getmetafilebitsex)
-   [**плайметафиле**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafile)
-   [**плайметафилерекорд**](/windows/desktop/api/Wingdi/nf-wingdi-playmetafilerecord)
-   [**сетметафилебитсекс**](/windows/desktop/api/Wingdi/nf-wingdi-setmetafilebitsex)

 

 
