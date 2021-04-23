---
title: Сохранение захваченных данных в новый файл
description: Сохранение захваченных данных в новый файл
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Сообщение WM_CAP_FILE_SAVEAS
- макрос Капфилесавеас
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775986"
---
# <a name="saving-captured-data-to-a-new-file"></a><span data-ttu-id="6c431-105">Сохранение захваченных данных в новый файл</span><span class="sxs-lookup"><span data-stu-id="6c431-105">Saving Captured Data to a New File</span></span>

<span data-ttu-id="6c431-106">Если пользователь хочет сохранить захваченные данные, приложение должно сохранить содержимое файла записи в другой файл с помощью сообщения о сохранении [**\_ \_ файла \_ WM**](wm-cap-file-saveas.md) (или макроса [**капфилесавеас**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ).</span><span class="sxs-lookup"><span data-stu-id="6c431-106">If the user wants to save captured data, the application should save the contents of the capture file to another file by using the [**WM\_CAP\_FILE\_SAVEAS**](wm-cap-file-saveas.md) message (or the [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) macro).</span></span> <span data-ttu-id="6c431-107">Это сообщение не изменяет имя или содержимое файла записи.</span><span class="sxs-lookup"><span data-stu-id="6c431-107">This message does not change the name or contents of the capture file.</span></span> <span data-ttu-id="6c431-108">Приложение должно указать имя для нового файла, так как файл записи сохраняет свое исходное имя файла.</span><span class="sxs-lookup"><span data-stu-id="6c431-108">Your application must specify a name for the new file because the capture file retains its original filename.</span></span>

<span data-ttu-id="6c431-109">Как правило, файл записи предварительно выделяется для самого крупного сегмента записи, и только его часть может использоваться для сбора данных.</span><span class="sxs-lookup"><span data-stu-id="6c431-109">Typically, a capture file is preallocated for the largest capture segment anticipated, and only a portion of it might be used to capture data.</span></span> <span data-ttu-id="6c431-110">В этом сообщении копируется только часть файла записи, содержащая данные записи.</span><span class="sxs-lookup"><span data-stu-id="6c431-110">This message copies only the portion of the capture file containing the capture data.</span></span>

 

 




