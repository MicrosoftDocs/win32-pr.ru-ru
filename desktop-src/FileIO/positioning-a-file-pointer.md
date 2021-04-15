---
description: Windows использует указатель на файл для хранения прочитанных или записанных байтов.
ms.assetid: 21c75d96-0357-422d-b12b-74c56f64ecf1
title: Размещение указателя на файл
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6588a3d65e71c2180c4e9753e65cd94ed070d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683444"
---
# <a name="positioning-a-file-pointer"></a><span data-ttu-id="1e7f8-103">Размещение указателя на файл</span><span class="sxs-lookup"><span data-stu-id="1e7f8-103">Positioning a File Pointer</span></span>

<span data-ttu-id="1e7f8-104">Когда приложение вызывает [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) для открытия файла в первый раз, Windows помещает [указатель файла](file-pointers.md) в начало файла.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-104">When an application calls [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) to open a file for the first time, Windows places the [file pointer](file-pointers.md) at the beginning of the file.</span></span> <span data-ttu-id="1e7f8-105">Так как байты считываются из файла или записываются в файл, Windows увеличивает указатель файла на число считанных или записанных байтов.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-105">As bytes are read from or written to the file, Windows advances the file pointer the number of bytes read or written.</span></span>

<span data-ttu-id="1e7f8-106">Приложение может поместить указатель файла в указанное смещение, вызвав [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span><span class="sxs-lookup"><span data-stu-id="1e7f8-106">An application can position the file pointer to a specified offset by calling [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer).</span></span>

<span data-ttu-id="1e7f8-107">Функция [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) может также использоваться для запроса текущей позиции указателя файла путем указания метода Move **файла \_ Current** и расстояния от нуля.</span><span class="sxs-lookup"><span data-stu-id="1e7f8-107">The [**SetFilePointer**](/windows/desktop/api/FileAPI/nf-fileapi-setfilepointer) function can also be used to query the current file pointer position by specifying a move method of **FILE\_CURRENT** and a distance of zero.</span></span>

 

 



