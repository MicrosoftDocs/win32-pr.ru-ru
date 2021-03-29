---
title: Формат видео
description: Формат видео
ms.assetid: d008bf48-302d-4533-8112-37961ecd40e1
keywords:
- Сообщение WM_CAP_GET_VIDEOFORMAT
- макрос Капжетвидеоформат
- макрос Капжетвидеоформатсизе
- Сообщение WM_CAP_SET_VIDEOFORMAT
- макрос Капсетвидеоформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5efe3c517a45ea44e9f8ab9ebd8fbae6dd95194
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774114"
---
# <a name="video-format"></a><span data-ttu-id="26d32-108">Формат видео</span><span class="sxs-lookup"><span data-stu-id="26d32-108">Video Format</span></span>

<span data-ttu-id="26d32-109">Структуру, указывающую формат видео или размер этой структуры, можно получить, отправив сообщение [**\_ \_ \_ видеоформат с закреплениями WM**](wm-cap-get-videoformat.md) (или макросы [**капжетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) и [**капжетвидеоформатсизе**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="26d32-109">You can retrieve the structure that specifies the video format or the size of that structure by sending the [**WM\_CAP\_GET\_VIDEOFORMAT**](wm-cap-get-videoformat.md) message (or the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros) to a capture window.</span></span> <span data-ttu-id="26d32-110">Вы можете задать формат записанных данных видео, отправив сообщение [**\_ \_ \_ видеоформат с закреплениями WM**](wm-cap-set-videoformat.md) (или макрос [**капсетвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) ) в окно записи.</span><span class="sxs-lookup"><span data-stu-id="26d32-110">You can set the format of captured video data by sending the [**WM\_CAP\_SET\_VIDEOFORMAT**](wm-cap-set-videoformat.md) message (or the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro) to a capture window.</span></span>

 

 




