---
title: Чтение из файла
description: Чтение из файла
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- Функция Авифилеинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068391"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="62b38-104">Чтение из файла</span><span class="sxs-lookup"><span data-stu-id="62b38-104">Reading from a File</span></span>

<span data-ttu-id="62b38-105">Сведения о открытом файле можно получить с помощью функции [**авифилеинфо**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) .</span><span class="sxs-lookup"><span data-stu-id="62b38-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="62b38-106">Эта функция заполняет структуру [**авифилеинфо**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) такими сведениями, как максимальная скорость передачи данных, число потоков в файле, независимо от того, использует ли файл индекс, а также указывает, что файл защищен.</span><span class="sxs-lookup"><span data-stu-id="62b38-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="62b38-107">Чтобы получить дополнительные сведения в файле AVI, используйте функцию [**авифилереаддата**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) .</span><span class="sxs-lookup"><span data-stu-id="62b38-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="62b38-108">Дополнительные сведения применимы ко всему файлу и не включаются в обычные заголовки файлов.</span><span class="sxs-lookup"><span data-stu-id="62b38-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="62b38-109">Например, имя компании или лица, которые содержат авторские права на файл, могут быть дополнительными сведениями.</span><span class="sxs-lookup"><span data-stu-id="62b38-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="62b38-110">Дополнительная информация не соответствует конкретному формату. Это может быть отдельный файл.</span><span class="sxs-lookup"><span data-stu-id="62b38-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="62b38-111">**Авифилереаддата** Возвращает дополнительные сведения в буфер, предоставляемый приложением.</span><span class="sxs-lookup"><span data-stu-id="62b38-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 




