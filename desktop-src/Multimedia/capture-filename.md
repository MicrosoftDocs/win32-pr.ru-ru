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
ms.openlocfilehash: 47e48ecd727accccb868d0f78c68a833ac6ec6655bada23db8a56f2a9aeaffd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118941599"
---
# <a name="capture-filename"></a>Записать имя файла

По умолчанию Авикап перенаправляет данные видео и звукового потока из окна записи в файл с именем CAPTURE.AVI в корневом каталоге текущего диска. Можно указать альтернативное имя файла, отправив сообщение с [**\_ \_ \_ \_ \_ файлом записи набора файлов закрепления WM**](wm-cap-file-set-capture-file.md) (или макрос [**капфилесеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) в окно записи. В этом сообщении указывается имя файла; Он не создает, не выделяет или не открывает файл. Вы можете получить текущее имя файла записи, отправив [**\_ \_ файл закрепления \_ \_ \_ WM**](wm-cap-file-get-capture-file.md) File (или макрос [**капфилежеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) в окно записи.

 

 




