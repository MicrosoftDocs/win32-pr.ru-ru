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
# <a name="capture-filename"></a><span data-ttu-id="cb584-107">Записать имя файла</span><span class="sxs-lookup"><span data-stu-id="cb584-107">Capture Filename</span></span>

<span data-ttu-id="cb584-108">По умолчанию Авикап перенаправляет данные видео и звукового потока из окна записи в файл с именем CAPTURE.AVI в корневом каталоге текущего диска.</span><span class="sxs-lookup"><span data-stu-id="cb584-108">AVICap, by default, routes video and audio stream data from a capture window to a file named CAPTURE.AVI in the root directory of the current drive.</span></span> <span data-ttu-id="cb584-109">Можно указать альтернативное имя файла, отправив сообщение с [**\_ \_ \_ \_ \_ файлом записи набора файлов закрепления WM**](wm-cap-file-set-capture-file.md) (или макрос [**капфилесеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="cb584-109">You can specify an alternate filename by sending the [**WM\_CAP\_FILE\_SET\_CAPTURE\_FILE**](wm-cap-file-set-capture-file.md) message (or the [**capFileSetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilesetcapturefile) macro) to a capture window.</span></span> <span data-ttu-id="cb584-110">В этом сообщении указывается имя файла; Он не создает, не выделяет или не открывает файл.</span><span class="sxs-lookup"><span data-stu-id="cb584-110">This message specifies the filename; it does not create, allocate, or open the file.</span></span> <span data-ttu-id="cb584-111">Вы можете получить текущее имя файла записи, отправив [**\_ \_ файл закрепления \_ \_ \_ WM**](wm-cap-file-get-capture-file.md) File (или макрос [**капфилежеткаптурефиле**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="cb584-111">You can retrieve the current capture filename by sending the [**WM\_CAP\_FILE\_GET\_CAPTURE\_FILE**](wm-cap-file-get-capture-file.md) message (or the [**capFileGetCaptureFile**](/windows/desktop/api/Vfw/nf-vfw-capfilegetcapturefile) macro) to a capture window.</span></span>

 

 




