---
title: Записать имя файла
description: Записать имя файла
ms.assetid: b17ecdd4-899e-4e94-98f2-496f93491e06
keywords:
- Сообщение WM_CAP_FILE_SET_CAPTURE_FILE
- макрос Капфилесеткаптурефиле
- Сообщение WM_CAP_FILE_GET_CAPTURE_FILE
- макрос Капфилежеткаптурефиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4856649906e09f212d2f8992c9d4fb9b8f4c37d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672065"
---
# <a name="capture-filename"></a>Записать имя файла

По умолчанию Авикап перенаправляет данные видео и звукового потока из окна записи в файл с именем CAPTURE.AVI в корневом каталоге текущего диска. Можно указать альтернативное имя файла, отправив сообщение с [**\_ \_ \_ \_ \_ файлом записи набора файлов закрепления WM**](wm-cap-file-set-capture-file.md) (или макрос [**капфилесеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) в окно записи. В этом сообщении указывается имя файла; Он не создает, не выделяет или не открывает файл. Вы можете получить текущее имя файла записи, отправив [**\_ \_ файл закрепления \_ \_ \_ WM**](wm-cap-file-get-capture-file.md) File (или макрос [**капфилежеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) в окно записи.

 

 




