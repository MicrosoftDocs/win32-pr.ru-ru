---
title: Внедрение фрагментов сведений в файл AVI
description: Внедрение фрагментов сведений в файл AVI
ms.assetid: 010c7b15-131a-47c8-9444-ee148bd351b0
keywords:
- Сообщение WM_CAP_FILE_SET_INFOCHUNK
- макрос Капфилесетинфочунк
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fdcf601b51c7fd825a6e6ca2d592a2ad566c6f1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650282"
---
# <a name="embedding-information-chunks-in-an-avi-file"></a><span data-ttu-id="0daaa-105">Внедрение фрагментов сведений в файл AVI</span><span class="sxs-lookup"><span data-stu-id="0daaa-105">Embedding Information Chunks in an AVI File</span></span>

<span data-ttu-id="0daaa-106">В AVI-файл можно вставлять фрагменты информации, такие как текст или пользовательские данные, с помощью сообщения [**\_ \_ \_ \_ Инфочунк с закреплениями WM**](wm-cap-file-set-infochunk.md) (или макроса [**капфилесетинфочунк**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) ).</span><span class="sxs-lookup"><span data-stu-id="0daaa-106">You can insert information chunks, such as text or custom data, in an AVI file by using the [**WM\_CAP\_FILE\_SET\_INFOCHUNK**](wm-cap-file-set-infochunk.md) message (or the [**capFileSetInfoChunk**](/windows/desktop/api/Vfw/nf-vfw-capfilesetinfochunk) macro).</span></span> <span data-ttu-id="0daaa-107">Это сообщение также можно использовать для очистки фрагментов данных из файла AVI.</span><span class="sxs-lookup"><span data-stu-id="0daaa-107">You can also use this message to clear information chunks from an AVI file.</span></span>

 

 




