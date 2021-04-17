---
description: Приложение может усечь или расширить файл путем вызова SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Усечение или расширение файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684190"
---
# <a name="truncating-or-extending-files"></a><span data-ttu-id="59d1f-103">Усечение или расширение файлов</span><span class="sxs-lookup"><span data-stu-id="59d1f-103">Truncating or Extending Files</span></span>

<span data-ttu-id="59d1f-104">Приложение может усечь или расширить файл путем вызова [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="59d1f-104">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span> <span data-ttu-id="59d1f-105">Эта функция задает маркер конца файла для текущей позиции указателя файла.</span><span class="sxs-lookup"><span data-stu-id="59d1f-105">This function sets the end-of-file marker to the current position of the file pointer.</span></span>

<span data-ttu-id="59d1f-106">Обратите внимание, что при расширении файла содержимое между старым и новым расположениями в конце файла не определяется.</span><span class="sxs-lookup"><span data-stu-id="59d1f-106">Note that when a file is extended, the contents between the old and new end-of-file locations are not defined.</span></span>

 

 



