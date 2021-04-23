---
title: Сохранение записанного содержимого
description: Сохранение записанного содержимого
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- Макрос МЦивндсаве
- Макрос МЦивндсаведиалог
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775983"
---
# <a name="saving-recorded-content"></a><span data-ttu-id="698a1-105">Сохранение записанного содержимого</span><span class="sxs-lookup"><span data-stu-id="698a1-105">Saving Recorded Content</span></span>

<span data-ttu-id="698a1-106">После завершения записи можно сохранить содержимое с помощью макроса [**мЦивндсаве**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) или [**мЦивндсаведиалог**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) или с помощью функции [**жетсавефиленамепревиев**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) с **мЦивндсаве**.</span><span class="sxs-lookup"><span data-stu-id="698a1-106">After completing the recording, you can save the content by using the [**MCIWndSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) or [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro, or by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function with **MCIWndSave**.</span></span> <span data-ttu-id="698a1-107">Макрос **мЦивндсаве** сохраняет данные в файле, связанном с окном мЦивнд.</span><span class="sxs-lookup"><span data-stu-id="698a1-107">The **MCIWndSave** macro saves data in the file associated with the MCIWnd window.</span></span> <span data-ttu-id="698a1-108">Макрос **мЦивндсаведиалог** позволяет пользователю указать имя файла и сохранить записанные данные в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="698a1-108">The **MCIWndSaveDialog** macro lets the user specify a filename and save the recorded data in the specified file.</span></span> <span data-ttu-id="698a1-109">Функция **жетсавефиленамепревиев** отображает диалоговое окно **сохранить** для выбора файла и позволяет пользователю просмотреть его (воспроизвести).</span><span class="sxs-lookup"><span data-stu-id="698a1-109">The **GetSaveFileNamePreview** function displays the **SaveAs** dialog box for choosing a file and lets the user preview (play) the file.</span></span> <span data-ttu-id="698a1-110">Если имя существующего файла указано в диалоговом окне **SaveAs** , **жетсавефиленамепревиев** предоставляет небольшой элемент управления в диалоговом окне, позволяющий пользователю просмотреть содержимое файла.</span><span class="sxs-lookup"><span data-stu-id="698a1-110">When the name of an existing file is specified in the **SaveAs** dialog box, **GetSaveFileNamePreview** provides a small control in the dialog box to let the user preview the contents of the file.</span></span> <span data-ttu-id="698a1-111">Записанные данные можно сохранить в файле, выбранном с помощью **жетсавефиленамепревиев** , используя **мЦивндсаве**.</span><span class="sxs-lookup"><span data-stu-id="698a1-111">You can save the recorded data in a file selected with **GetSaveFileNamePreview** by using **MCIWndSave**.</span></span>

 

 




