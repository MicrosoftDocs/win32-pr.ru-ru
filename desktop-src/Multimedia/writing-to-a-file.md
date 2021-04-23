---
title: Запись в файл
description: Запись в файл
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- Функция Авифилевритедата
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105672111"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="1b7b4-104">Запись в файл</span><span class="sxs-lookup"><span data-stu-id="1b7b4-104">Writing to a File</span></span>

<span data-ttu-id="1b7b4-105">Дополнительные сведения можно записать в файл, Открытый с правами на запись, с помощью функции [**авифилевритедата**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) .</span><span class="sxs-lookup"><span data-stu-id="1b7b4-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="1b7b4-106">Эта функция копирует сведения из буфера, предоставляемого приложением, и помещает их в один или несколько фрагментов файла.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="1b7b4-107">Фрагмент «INFO» — это общий тип фрагмента Metallica, в котором функция хранит дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="1b7b4-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="1b7b4-108">Описание файлов Metallica и их фрагментов данных см. в разделе [ресурс обмена ресурсами службы форматов](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="1b7b4-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




