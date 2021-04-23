---
description: Приложение может распаковать сжатый файл в части за раз с помощью функций Лзсик и Лзреад.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Чтение из сжатых файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684030"
---
# <a name="reading-from-compressed-files"></a><span data-ttu-id="4b425-103">Чтение из сжатых файлов</span><span class="sxs-lookup"><span data-stu-id="4b425-103">Reading from Compressed Files</span></span>

<span data-ttu-id="4b425-104">Помимо распаковки полного файла в одной операции, приложение может распаковать сжатый файл в одну часть за раз с помощью функций [**лзсик**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) и [**лзреад**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) .</span><span class="sxs-lookup"><span data-stu-id="4b425-104">In addition to decompressing a complete file in a single operation, an application can decompress a compressed file a portion at a time by using the [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) and [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) functions.</span></span> <span data-ttu-id="4b425-105">Эти функции особенно полезны, когда необходимо извлечь части больших файлов.</span><span class="sxs-lookup"><span data-stu-id="4b425-105">These functions are particularly useful when it is necessary to extract parts of large files.</span></span> <span data-ttu-id="4b425-106">Например, производители шрифтов могут иметь сжатые файлы, содержащие метрики шрифтов, помимо символьных данных.</span><span class="sxs-lookup"><span data-stu-id="4b425-106">For example, a font manufacturer may have compressed files containing font metrics in addition to character data.</span></span> <span data-ttu-id="4b425-107">Чтобы использовать сведения из этих файлов, приложению потребуется распаковать файл. Однако большинство приложений будет использовать только часть файла в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="4b425-107">To use the information in these files, an application would need to decompress the file; however, most applications would use only part of the file at any particular time.</span></span> <span data-ttu-id="4b425-108">Чтобы получить сведения о метриках шрифта, приложение будет извлекать данные из заголовка.</span><span class="sxs-lookup"><span data-stu-id="4b425-108">To get information about font metrics, the application would extract data from the header.</span></span> <span data-ttu-id="4b425-109">Чтобы получить сведения из текста, приложение перемещает указатель файла, вызывая **лзсик** и извлекая символьные данные путем вызова **лзреад**.</span><span class="sxs-lookup"><span data-stu-id="4b425-109">To get information from the text, the application would reposition the file pointer by calling **LZSeek** and extract character data by calling **LZRead**.</span></span>

 

 



