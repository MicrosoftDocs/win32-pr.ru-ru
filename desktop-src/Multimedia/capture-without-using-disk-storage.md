---
title: Захват без использования Хранилище дисков
description: Захват без использования Хранилище дисков
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Сообщение WM_CAP_SEQUENCE_NOFILE
- макрос Капкаптуресекуенценофиле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650272"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="621ab-105">Захват без использования Хранилище дисков</span><span class="sxs-lookup"><span data-stu-id="621ab-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="621ab-106">Вы можете использовать службы захвата, не записывая данные в файл на диске с помощью сообщения о том, что вы используете для этого сообщение о некотором, или в макросе [**капкаптуресекуенценофиле**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) . [**\_ \_ \_**](wm-cap-sequence-nofile.md)</span><span class="sxs-lookup"><span data-stu-id="621ab-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="621ab-107">Это сообщение полезно только в сочетании с функциями обратного вызова, которые позволяют приложению напрямую использовать видео и аудио-данные.</span><span class="sxs-lookup"><span data-stu-id="621ab-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="621ab-108">Например, приложения для видеоконференций могут использовать это сообщение для получения потоковых кадров видео.</span><span class="sxs-lookup"><span data-stu-id="621ab-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="621ab-109">Функции обратного вызова переносят захваченные образы на удаленный компьютер.</span><span class="sxs-lookup"><span data-stu-id="621ab-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




